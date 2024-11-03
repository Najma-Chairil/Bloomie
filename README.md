<section data-bs-version="5.1" class="contacts01" group="Contacts" data-bg-video="{{bg.type == 'video' && bg.value.url}}" mbr-class="{'mbr-parallax-background': bg.parallax}">
    <mbr-parameters>
        <header>Size</header>
        <input type="checkbox" title="Full Width" name="fullWidth">
        <input type="range" inline title="Top" name="paddingTop" min="0" max="10" step="1" value="6">
        <input type="range" inline title="Bottom" name="paddingBottom" min="0" max="10" step="1" value="6">
        <select title="Columns" name="cardsWidth">
			<option value="6" selected>2</option>
			<option value="4">3</option>
			<option value="3">4</option>
		</select>
        <header>Show/Hide</header>
        <input type="checkbox" title="Title" name="showTitle" checked>
        <input type="checkbox" title="Subtitle" name="showSubtitle">
        <header>Cards</header>
        <input type="checkbox" title="Title" name="showTitleCards" checked>
        <input type="checkbox" title="Text" name="showText" checked>
        <input type="color" title="BG" name="cardsBg" value="#faf4f4">
        <header>Background</header>
        <fieldset type="background" name="bg" parallax>
            <input type="image" title="Image" value="https://r.mobirisesite.com/856035/assets/images/background1-h_m318kuuy.jpg" parallax selected>
            <input type="color" title="Color" value="#edefeb">
            <input type="video" title="Video" value="https://vimeo.com/428046504">
        </fieldset>
        <header condition="bg.type === 'video'">Fallback Image</header>
        <input type="image" title="Fallback Image" value="../_images/background1.jpg" name="fallBackImage" condition="bg.type === 'video'">
        <input type="checkbox" title="Overlay" name="overlay" checked condition="bg.type !== 'color'">
        <input type="color" title="Overlay Color" name="overlayColor" value="#ffffff" condition="overlay && bg.type !== 'color'">
        <input type="range" inline title="Opacity" name="overlayOpacity" min="0" max="1" step="0.1" value="0.2" condition="overlay && bg.type !== 'color'">
    </mbr-parameters>

    <div class="mbr-fallback-image disabled" mbr-if="bg.type == 'video'"></div>
    <div class="mbr-overlay" mbr-if="overlay && bg.type!== 'color'" mbr-style="{'opacity': overlayOpacity, 'background-color': overlayColor}">
    </div>
    <div mbr-class="{'container': !fullWidth, 'container-fluid': fullWidth}">
        <div class="row justify-content-center">
            <div class="col-12 content-head">
                <div class="mbr-section-head mb-5" mbr-if="showTitle || showSubtitle">
                    <h3 class="mbr-section-title mbr-fonts-style align-center mb-0" mbr-theme-style="display-2" mbr-if="showTitle" data-app-selector=".mbr-section-title">
                        <b>Contacts</b>
                    </h3>
                    <h4 class="mbr-section-subtitle mbr-fonts-style align-center mb-0 mt-4" mbr-theme-style="display-7" mbr-if="showSubtitle" data-app-selector=".mbr-section-subtitle">
                        Contacts Subtitle
                    </h4>
                </div>
            </div>
        </div>
        <div class="row">
            <div class="item features-without-image col-12 col-md-{{cardsWidth}} active">
                <div class="item-wrapper">
                    <div class="text-wrapper">
                        <h6 class="card-title mbr-fonts-style mb-3" mbr-theme-style="display-5" data-app-selector=".card-title" mbr-if="showTitleCards">
                            <b>Phone</b>
                        </h6>
                        <p class="mbr-text mbr-fonts-style" mbr-theme-style="display-7" mbr-if="showText">0896-3760-2469</p>
                    </div>
                </div>
            </div>
            <div class="item features-without-image col-12 col-md-{{cardsWidth}}">
                <div class="item-wrapper">
                    <div class="text-wrapper">
                        <h6 class="card-title mbr-fonts-style mb-3" mbr-theme-style="display-5" data-app-selector=".card-title" mbr-if="showTitleCards">
                            <b>Email</b>
                        </h6>
                        <p class="mbr-text mbr-fonts-style" mbr-theme-style="display-7" mbr-if="showText">Bloomie.id@gmail.com</p>
                    </div>
                </div>
            </div>
            <div class="item features-without-image col-12 col-md-{{cardsWidth}}">
                <div class="item-wrapper">
                    <div class="text-wrapper">
                        <h6 class="card-title mbr-fonts-style mb-3" mbr-theme-style="display-5" data-app-selector=".card-title" mbr-if="showTitleCards">
                            <b>Address</b>
                        </h6>
                        <p class="mbr-text mbr-fonts-style" mbr-theme-style="display-7" mbr-if="showText">&nbsp;Jl. Swadarma Raya No.58, Ulujami, Kec. Pesanggrahan, Kota Jakarta Selatan, Daerah Khusus Ibukota Jakarta 12250</p>
                    </div>
                </div>
            </div>
            <div class="item features-without-image col-12 col-md-{{cardsWidth}}">
                <div class="item-wrapper">
                    <div class="text-wrapper">
                        <h6 class="card-title mbr-fonts-style mb-3" mbr-theme-style="display-5" data-app-selector=".card-title" mbr-if="showTitleCards">
                            <b>Working Hours</b>
                        </h6>
                        <p class="mbr-text mbr-fonts-style" mbr-theme-style="display-7" mbr-if="showText">8 AM-5 PM</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</section>
