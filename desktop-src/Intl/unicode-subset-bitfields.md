---
description: Os subconjuntos Unicode bitfields (USBs) são usados nas estruturas FONTSIGNATURE e LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Subconjunto Unicode bitfields
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f0fa4791e62f397e62a99a78d41dbcdc67c55299a650b1bc78bea685205399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787986"
---
# <a name="unicode-subset-bitfields"></a>Subconjunto Unicode bitfields

Os subconjuntos Unicode bitfields (USBs) são usados nas estruturas [**fontSignature**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) e [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Subintervalo Unicode</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>Latim básico</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>Suplemento latino-1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>Latim estendido-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>Latim estendido-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4 $ {REMOVER} $<br />
</td>
<td>0250 - 02AF</td>
<td>Extensões IPA</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>Extensões fonéticas</td>

</tr>
<tr class="odd">
<td>1D80 - 1DBF</td>
<td>Suplementos de extensões fonéticas</td>

</tr>
<tr class="even">
<td rowspan="2">5 $ {REMOVER} $<br />
</td>
<td>02B0 - 02FF</td>
<td>Letras do modificador de espaçamento</td>
</tr>
<tr class="odd">
<td>A700 - A71F</td>
<td>Letras de Tom modificadores</td>

</tr>
<tr class="even">
<td rowspan="2">6 $ {REMOVER} $<br />
</td>
<td>0300 - 036F</td>
<td>Combinando marcas de sinais diacríticos</td>
</tr>
<tr class="odd">
<td>1DC0 - 1DFF</td>
<td>Complemento de sinais diacríticos combináveis</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>Grego e cóptico</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>Copta</td>
</tr>
<tr class="even">
<td rowspan="4">9 $ {REMOVER} $<br />
</td>
<td>0400 - 04FF</td>
<td>Cirílico</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>Suplementar cirílico</td>

</tr>
<tr class="even">
<td>2DE0 - 2DFF</td>
<td>Cirílico estendido-A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>Cirílico estendido-B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>Armênia</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Hebraico</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500 - A63F</td>
<td>Vai</td>
</tr>
<tr class="odd">
<td rowspan="2">13 $ {REMOVER} $<br />
</td>
<td>0600 - 06FF</td>
<td>Árabe</td>
</tr>
<tr class="even">
<td>0750-077F</td>
<td>Suplementar árabe</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
<td>NKo</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>Devanagari</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>Bangla</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>Gurmukhi</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>Guzerate</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>Oriá</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>Tâmil</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>Télugo</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>canarim</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>Malaiala</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>Tailandês</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>Lao</td>
</tr>
<tr class="odd">
<td rowspan="2">26${REMOVE}$<br />
</td>
<td>10A0 - 10FF</td>
<td>Georgiano</td>
</tr>
<tr class="even">
<td>2D00 – 2D2F</td>
<td>Suplemento DeMenter</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 – 1B7F</td>
<td>Balinês</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>Hangul Jamo</td>
</tr>
<tr class="odd">
<td rowspan="3">29${REMOVE}$<br />
</td>
<td>1E00 - 1EFF</td>
<td>Latin Extended Additional</td>
</tr>
<tr class="even">
<td>2C60 – 2C7F</td>
<td>Latin Extended-C</td>

</tr>
<tr class="odd">
<td>A720 – A7FF</td>
<td>Latin Extended-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>Grego Estendido</td>
</tr>
<tr class="odd">
<td rowspan="2">31${REMOVE}$<br />
</td>
<td>2000 - 206F</td>
<td>Pontuação geral</td>
</tr>
<tr class="even">
<td>2E00 – 2E7F</td>
<td>Pontuação suplementar</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>Subscritos e subscritos</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>Conversor de Moedas Símbolos</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>Combinando marcas diacríticas para símbolos</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>Símbolos letterlike</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>Formulários de número</td>
</tr>
<tr class="even">
<td rowspan="4">37${REMOVE}$<br />
</td>
<td>2190 - 21FF</td>
<td>Setas</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>Setas complementares -A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>Setas complementares -B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>Símbolos e setas diversos</td>

</tr>
<tr class="even">
<td rowspan="4">38${REMOVE}$<br />
</td>
<td>2200 - 22FF</td>
<td>Operadores matemáticos</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>Símbolos matemáticos diversos – A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>Símbolos matemáticos diversos -B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>Operadores matemáticos complementares</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>Diversos técnicos</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>Imagens de controle</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>Reconhecimento óptico de caracteres</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>Alfanuméricos delimitados</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>Desenho de caixa</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Elementos de bloco</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>Formas geométricas</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>Símbolos diversos</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>Símbolos CJK e pontuação</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>Hiragana</td>
</tr>
<tr class="odd">
<td rowspan="2">50${REMOVE}$<br />
</td>
<td>30A0 - 30FF</td>
<td>Katakana</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>Extensões phoneáticas katakana</td>

</tr>
<tr class="odd">
<td rowspan="2">51${REMOVE}$<br />
</td>
<td>3100 - 312F</td>
<td>Bopomofo</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>Bopomofo Estendido</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>Hangul Compatibility Jamo</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 – A87F</td>
<td>Phags-pa</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>Letras CJK e meses incluídos</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>Compatibilidade do CJK</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>Hangul Syllables</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800 – DFFF</td>
<td>Não Plano 0. Observe que definir esse bit implica que há pelo menos um ponto de código suplementar além do BMP (Plano Multilíngue Básico) que é suportado por essa fonte. Consulte <a href="surrogates-and-supplementary-characters.md">Substitutos e caracteres suplementares.</a></td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900 – 1091F</td>
<td>Fenício</td>
</tr>
<tr class="even">
<td rowspan="7">59${REMOVE}$<br />
</td>
<td>2E80 - 2EFF</td>
<td>Suplemento de CJK Radicals</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>Radicales Demáxi</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>Caracteres de descrição idegráfica</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>Kanbun</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>Extensão A de Ideographs Unificados do CJK</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>Ideographs unificados do CJK</td>

</tr>
<tr class="even">
<td>20000 – 2A6DF</td>
<td>Extensão B de Ideographs Unificados do CJK</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>Área de uso privado</td>
</tr>
<tr class="even">
<td rowspan="3">61${REMOVE}$<br />
</td>
<td>31C0 – 31EF</td>
<td>Traços CJK</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>Ideographs de compatibilidade do CJK</td>

</tr>
<tr class="even">
<td>2F800 – 2FA1F</td>
<td>Suplemento de Ideographs de compatibilidade do CJK</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>Formulários de apresentação alfabética</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>Formulários de apresentação árabe -A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>Combinando marcas de metade</td>
</tr>
<tr class="even">
<td rowspan="2">65${REMOVE}$<br />
</td>
<td>FE10 – FE1F</td>
<td>Formulários verticais</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>Formulários de compatibilidade do CJK</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>Variantes de formulário pequeno</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>Formulários de apresentação árabe -B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>Halfwidth e Fullwidth Forms</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>Especiais</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>Tibetano</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>Siríaco</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>Thaana</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>Sinhala</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>Myanmar</td>
</tr>
<tr class="odd">
<td rowspan="3">75${REMOVE}$<br />
</td>
<td>1200 - 137F</td>
<td>Etíope</td>
</tr>
<tr class="even">
<td>1380 - 139F</td>
<td>Suplemento Ethiopic</td>

</tr>
<tr class="odd">
<td>2D80 – 2DDF</td>
<td>Ethiopic Estendido</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>Cherokee</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>Silábico Aboriginal canadense unificado</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>Ogham</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>Rúnica</td>
</tr>
<tr class="even">
<td rowspan="2">80 $ {REMOVER} $<br />
</td>
<td>1780 - 17FF</td>
<td>Khmer</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>Símbolos Khmer</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>Mongol</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>Padrões de braille</td>
</tr>
<tr class="even">
<td rowspan="2">83 $ {REMOVER} $<br />
</td>
<td>A000 - A48F</td>
<td>Sílabas Yi</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Radicais Yi</td>

</tr>
<tr class="even">
<td rowspan="4">84 $ {REMOVER} $<br />
</td>
<td>1700 - 171F</td>
<td>Tagalo</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>Hanunoo</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>Buhid</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>Tagbanwa</td>

</tr>
<tr class="even">
<td>85</td>
<td>10300-1032F</td>
<td>Itálico antigo</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330-1034F</td>
<td>Gothic</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400-1044F</td>
<td>Deseret</td>
</tr>
<tr class="odd">
<td rowspan="3">88 $ {REMOVER} $<br />
</td>
<td>1D000 - 1D0FF</td>
<td>Símbolos símbolos musicais</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>Símbolos musicais</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>Notação musical grega antiga</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>Símbolos alfanuméricos matemáticos</td>
</tr>
<tr class="odd">
<td rowspan="2">90 $ {REMOVER} $<br />
</td>
<td>FF000-FFFF</td>
<td>Uso privado (plano 15)</td>
</tr>
<tr class="even">
<td>100000-10FFFD</td>
<td>Uso privado (plano 16)</td>

</tr>
<tr class="odd">
<td rowspan="2">91 $ {REMOVER} $<br />
</td>
<td>FE00 - FE0F</td>
<td>Seletores de variação</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>Suplemento seletores de variação</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>Marcas</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>Limbu</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>Tai Le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980-19DF</td>
<td>Tai Lue Novo</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00 - 1A1F</td>
<td>Bugi</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>Letra</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>Tifinagh</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>Símbolos de Hexagrama do Yijing</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>Syloti Nagri</td>
</tr>
<tr class="even">
<td rowspan="3">101 $ {REMOVER} $<br />
</td>
<td>10000-1007F</td>
<td>Syllabary linear B</td>
</tr>
<tr class="odd">
<td>10080-100FF</td>
<td>Ideograms linear B</td>

</tr>
<tr class="even">
<td>10100-1013F</td>
<td>Números de Aegean</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140 – 1018F</td>
<td>Números gregos gregos in gregos</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380 – 1039F</td>
<td>Ugarítico</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 – 103DF</td>
<td>Antigo wiki</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450 – 1047F</td>
<td>Sha xiiano</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480 – 104AF</td>
<td>Osmanya</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800 – 1083F</td>
<td>Syllabary DeIaot</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 – 10A5F</td>
<td>Rossroshthi</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 – 1D35F</td>
<td>Símbolos de Jing do Tai X tai X tai</td>
</tr>
<tr class="odd">
<td rowspan="2">110${REMOVE}$<br />
</td>
<td>12000 – 123FF</td>
<td>Cuneiforme</td>
</tr>
<tr class="even">
<td>12400 - 1247F</td>
<td>Pontuação e números de Mioeiform</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 – 1D37F</td>
<td>Numerais de rod de contagem</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 – 1BBF</td>
<td>Sundanês</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 – 1C4F</td>
<td>Lepcha</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 – 1C7F</td>
<td>Ol Chiki</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 – A8DF</td>
<td>Saurashtra</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 – A92F</td>
<td>Kayah Li</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 – A95F</td>
<td>Rejang</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 – AA5F</td>
<td>Cham</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190 – 101CF</td>
<td>Símbolos de símbolos de símbolo de símbolo</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 – 101FF</td>
<td>Disco De Phaistos</td>
</tr>
<tr class="odd">
<td rowspan="3">121${REMOVE}$<br />
</td>
<td>10280 – 1029F</td>
<td>Lício</td>
</tr>
<tr class="even">
<td>102A0 – 102DF</td>
<td>Cariano</td>

</tr>
<tr class="odd">
<td>10920 – 1093F</td>
<td>Lídio</td>

</tr>
<tr class="even">
<td rowspan="2">122${REMOVE}$<br />
</td>
<td>1F000 – 1F02F</td>
<td>Blocos do Mahjong</td>
</tr>
<tr class="odd">
<td>1F030 – 1F09F</td>
<td>Blocos Domino</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 e posteriores:</strong> Progresso do layout, horizontal da direita para a esquerda</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 e posteriores:</strong> Progresso do layout, vertical antes da horizontal</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 e posteriores:</strong> Progresso do layout, vertical de baixo para cima</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>Reservado para uso interno do processo</td>
</tr>
</tbody>
</table>



 

 

 



