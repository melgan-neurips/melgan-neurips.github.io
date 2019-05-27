---
layout: default
title: {{ site.name }}
---

---

# Table of contents

* [Abstract](#abstract)
<!-- * [Model Description](#model) -->
* [Results](#results)
  * [Spectrogram Inversion on Unseen speakers](#spectrogram-inversion)
  * [TTS examples](#tts-examples)
  * [Unconditional Music Synthesis](#unconditional-music)
  * [Music Translation](#music-translation)
  * [Samples along Training](#samples-along-training)
  * [Ablation](#ablation)

---

<a name="abstract"></a>
# Abstract
Previous works have found that generating coherent raw audio waveforms with GANs is challenging. In this paper, we show that it is possible to train GANs reliably to generate high quality coherent waveforms by introducing a set of architectural changes and simple training techniques. Two subjective evaluation metrics (Mean Opinion Score and MUSHRA) suggest that our model is state-of-the-art for mel-spectrogram inversion. We show qualitative results of our model on speech synthesis, music domain translation and unconditional music synthesis, to establish the generality of the proposed techniques. We also evaluate different components of the model, proposing a set of guidelines for designing general purpose discriminators and generators for conditional sequence synthesis tasks. Our model is non-autoregressive, fully convolutional, with significantly fewer parameters as compared to competing models and generalizes to unseen speakers for mel-spectrogram inversion. Our pytorch implementation runs at more than 100x faster than realtime on GTX 1080Ti GPU and more than 2x faster than realtime on CPU, without any hardware specific optimization tricks.

<!-- <a name="model"></a>
# Model Description -->

<a name="results"></a>
# Results

<a name="spectrogram-inversion"></a>
## Spectrogram Inversion on Unseen Speakers
Original
<audio controls>
  <source src="assets/inversion/original/0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/original/7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

Reconstructed
<audio controls>
  <source src="assets/inversion/reconstructed/0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/inversion/reconstructed/7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>


<a name="tts-examples"></a>
## End-to-end text-to-speech examples
<audio controls>
  <source src="assets/tts_samples/cheryl/0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/cheryl/1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/cheryl/2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/cheryl/3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/cheryl/4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<br>

<audio controls>
  <source src="assets/tts_samples/jb/0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/jb/1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/jb/2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/jb/3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/jb/4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<br>

<audio controls>
  <source src="assets/tts_samples/linda/0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/linda/1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/linda/2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/linda/3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/tts_samples/linda/4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<a name="unconditional-music"></a>
## Unconditional Music Synthesis

Original
<audio controls>
  <source src="assets/vqgan/original/original_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/original/original_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/original/original_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/original/original_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

Reconstructed
<audio controls>
  <source src="assets/vqgan/reconstructed/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/reconstructed/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/reconstructed/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/reconstructed/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

Sampled
<audio controls>
  <source src="assets/vqgan/sampled/sampled_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/vqgan/sampled/sampled_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<a name="music-translation"></a>
## Music Translation

Example for source domain: Bach Solo Cello

<table>
<col width="50">
<col width="50">
<col width="50">
<col width="50">
<col width="50">
<col width="50">
<tr>
<th/>
<th/>
<th colspan="2">Beethoven accompanied violin</th>
<th colspan="2">Beethoven solo piano</th>
</tr>
<tr>
 <th/>
 <th>Original</th>
 <th>Mor et al. 2019</th>
 <th>Ours</th>
 <th>Mor et al. 2019</th>
 <th>Ours</th>
</tr>

<tr>
<th> 1 </th>
<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/original/0.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_accompanied_violin_decoder/0.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_accompanied_violin_decoder/0.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>


<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_solo_piano_decoder/0.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_solo_piano_decoder/0.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>
</tr>

<tr>
<th> 2 </th>
<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/original/1.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_accompanied_violin_decoder/1.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_accompanied_violin_decoder/1.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>


<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_solo_piano_decoder/1.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_solo_piano_decoder/1.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>
</tr>

<tr>
<th> 3 </th>
<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/original/2.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_accompanied_violin_decoder/2.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_accompanied_violin_decoder/2.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>


<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_solo_piano_decoder/2.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_solo_piano_decoder/2.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>
</tr>

<tr>
<th> 4 </th>
<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/original/3.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_accompanied_violin_decoder/3.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_accompanied_violin_decoder/3.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>


<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_solo_piano_decoder/3.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_solo_piano_decoder/3.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>
</tr>

<tr>
<th> 5 </th>
<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/original/4.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_accompanied_violin_decoder/4.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_accompanied_violin_decoder/4.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>


<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/fb_beethoven_solo_piano_decoder/4.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>

<td>
 <audio controls style="width: 120px;">
   <source src="assets/music_translation/source_bach_solo_cello/our_beethoven_solo_piano_decoder/4.wav" type="audio/wav">
   Your browser does not support the audio element.
 </audio>
</td>
</tr>

</table>

<a name="samples-along-training"></a>
## Samples along Training

50 epochs - 1.35 hours
<audio controls>
  <source src="assets/timeline/generated_4_50.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

100 epochs - 2.71 hours
<audio controls>
  <source src="assets/timeline/generated_4_100.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

200 epochs - 5.42 hours
<audio controls>
  <source src="assets/timeline/generated_4_200.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

400 epochs - 10.84 hours
<audio controls>
  <source src="assets/timeline/generated_4_400.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

800 epochs - 21.68 hours
<audio controls>
  <source src="assets/timeline/generated_4_800.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

1600 epochs - 43.36 hours
<audio controls>
  <source src="assets/timeline/generated_4_1600.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

3200 epochs - 86.72 hours
<audio controls>
  <source src="assets/timeline/generated_4_3200.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>


<a name="ablation"></a>
## Ablation

original
<audio controls>
  <source src="assets/ablation/original/original_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/original/original_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/original/original_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/original/original_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/original/original_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/original/original_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/original/original_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/original/original_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

Baseline
<audio controls>
  <source src="assets/ablation/baseline/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/baseline/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/baseline/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/baseline/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/baseline/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/baseline/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/baseline/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/baseline/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

l1_observed_no_feat_match
<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_no_feat_match/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->


l1_observed_space
<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/l1_observed_space/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/l1_observed_space/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

no_dilations
<audio controls>
  <source src="assets/ablation/no_dilations/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_dilations/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/no_dilations/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_dilations/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_dilations/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_dilations/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_dilations/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_dilations/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

no_group_disc
<audio controls>
  <source src="assets/ablation/no_group_disc/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_group_disc/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/no_group_disc/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_group_disc/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_group_disc/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_group_disc/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_group_disc/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_group_disc/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

no_multiscale_disc
<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_multiscale_disc/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

no_patch_gan
<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/no_patch_gan/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_patch_gan/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

no_weight_norm
<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/no_weight_norm/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/no_weight_norm/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->

spectral_norm
<audio controls>
  <source src="assets/ablation/spectral_norm/generated_0.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/spectral_norm/generated_1.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<!-- <audio controls>
  <source src="assets/ablation/spectral_norm/generated_2.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/spectral_norm/generated_3.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/spectral_norm/generated_4.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/spectral_norm/generated_5.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/spectral_norm/generated_6.wav" type="audio/wav">
Your browser does not support the audio element.
</audio>

<audio controls>
  <source src="assets/ablation/spectral_norm/generated_7.wav" type="audio/wav">
Your browser does not support the audio element.
</audio> -->
