<script setup lang="ts">
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'
</script>

<template>
  <div class="cover-site">
        <div id="bgCover"></div>
        <div class="bg-mask"></div>
    </div>
    <main>
        <section id="player">
            <div class="container">
                <div class="row web-player">
                    <div class="col-12 col-lg-10">
                        <div class="row">
                            <div class="col-12 col-md-5">
                                <div class="cover-album">
                                    <div id="currentCoverArt"></div>
                                    <div class="watermark"></div>
                                </div>
                            </div>
                            <div class="col-12 ml-md-auto col-md-6">
                                <div class="row">
                                    <div class="col-12">
                                        <div class="info-current-song">
                                            <h2 id="currentSong" class="current-song text-uppercase">HITS RADIO</h2>
                                            <h3 id="currentArtist" class="current-artist text-captalize">Más Música</h3>
                                        </div>
                                    </div>
                                    <div class="col-12">
                                        <!--
                                       <div class="row">
                                            <div class="play-pause col-12 col-md-2 text-center">
                                                <i id="playerButton" class="fa fa-play-circle" onclick="togglePlay()"></i>
                                            </div>
                                            <div class="col-12 col-md-10 text-center">
                                                <div class="row volume-control">
                                                    <div class="volume-icon col-1"><i class="fa fa-volume-up"></i></div>
                                                    <div class="volume-slide col-10 text-center"><input type="range" id="volume"
                                                            step="1" min="0" max="100" value="80"></div>
                                                    <div class="percentual-volume col-12">Volume <span id="volIndicator">...</span>%</div>
                                                </div>
                                            </div>
                                            <div class="col-12 text-center call-lyrics">
                                                <a href="#" class="lyrics" style="" data-target="#modalLyrics">VER LETRA</a>
                                            </div>
                                        </div>-->
                                        
                                        <div class="row">
                                            <div class="play-pause col-12 col-md-6 text-center">
                                                <button  class="btn-play" onclick="togglePlay()"><i id="playerButton" class="fa fa-play"></i> <span id="buttonPlay">PLAY</span></button>
                
                                            </div>
                                        </div>
                                        <div class="row">
                                            <div class="col-12 col-md-6 text-center">
                                                <div class="row volume-control">
                                                    <div class="volume-icon col-1"><i class="fa fa-volume-up"></i></div>
                                                    <div class="volume-slide col-10 text-center"><input type="range" id="volume"
                                                            step="1" min="0" max="100" value="80"></div>
                                                    <div class="percentual-volume col-12">Volume <span id="volIndicator">...</span>%</div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="row">
                                            <div class="col-12 col-md-6 text-center call-lyrics">
                                                <a href="#" class="lyrics" style="" data-target="#modalLyrics">VER LETRA</a>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="row historic">
                    <div class="col-12">
                        <h2>RECIENTEMENTE</h2>
                        <div class="row" id="historicSong">
                            <article class="col-12 col-md-6">
                                <div class="cover-historic"></div>
                                <div class="music-info">
                                    <div class="song">NO INFORMACIÓN</div>
                                    <div class="artist">NOT INFO</div>
                                </div>
                                
                            </article>
                            <article class="col-12 col-md-6">
                                <div class="cover-historic"></div>
                                <div class="music-info">
                                    <div class="song">NO INFORMACIÓN</div>
                                    <div class="artist">NOT INFO</div>
                                </div>
                                
                                
                            </article>
                            
                            
                        </div>
                        //next song
                            

                    </div>
                </div>
            </div>
        </section>
    </main>
    <div class="modal fade" id="modalLyrics" tabindex="-1" role="dialog" aria-labelledby="lyricsSong" aria-hidden="true">
        <div class="modal-dialog" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title" id="lyricsSong">LETRA</h5>
                    <button type="button" style="color: #fff" class="close" data-dismiss="modal" aria-label="Fechar">
                        <span aria-hidden="true">&times;</span>
                    </button>
                </div>
                <div class="vagalume text-center"><a href="https://www.creaticoagencia.com/" target="_blank" rel="noopener"><img
                            src="src/img/logo_retinablack-2-2.png" class="" /></a><br />Derechos Reservados <a href="https://www.creativoagencia.com/"
                        target="_blank" rel="noopener">Creativo Agencia</a></div>
                <div class="modal-body" id="lyric"></div>
                <div class="modal-footer">
                    <button type="button" class="btn btn-success" data-dismiss="modal">Cerrar</button>
                </div>
            </div>
        </div>
    </div>
</template>
