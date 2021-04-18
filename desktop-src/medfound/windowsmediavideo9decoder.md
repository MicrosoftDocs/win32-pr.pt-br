---
description: O decodificador Windows Media Video 9 decodifica fluxos de vídeo que foram codificados pelo codificador de vídeo do Windows Media.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Decodificador do Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798232"
---
# <a name="windows-media-video-9-decoder"></a>Decodificador do Windows Media Video 9

O decodificador Windows Media Video 9 decodifica fluxos de vídeo que foram codificados pelo [**codificador de vídeo do Windows Media**](windowsmediavideo9encoder.md). O codificador e o decodificador dão suporte às quatro categorias de vídeo codificadas a seguir.

-   Perfil simples do Windows Media Video 9
-   Perfil principal do Windows Media Video 9
-   Perfil avançado do Windows Media Video 9
-   Imagem do vídeo 9,1 do Windows Media

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) para o decodificador de vídeo do Windows Media é representado pela constante **CLSID \_ CWMVDecMediaObject**. Você pode criar uma instância do decodificador de vídeo chamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

Um objeto de decodificador de vídeo expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

Um decodificador de vídeo se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. A tabela a seguir mostra as condições sob as quais um decodificador de vídeo se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Um decodificador de vídeo do Windows Media sempre se comporta como DMO.                                                                                                                |
| Windows Vista e Windows 7 | Por padrão, um decodificador de vídeo do Windows Media se comporta como DMO. Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um decodificador de vídeo, ele se comporta como um MFT. |



 

A partir do Windows 7, o decodificador de vídeo do Windows Media implementa a interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Formatos de entrada

A tabela a seguir mostra os códigos de quatro caracteres (FOURCC) que correspondem às categorias de entrada codificada que são suportadas pelo decodificador de vídeo do Windows Media.



| Categoria                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Perfil simples do Windows Media Video 9   | "WMV3"                                   |
| Perfil principal do Windows Media Video 9     | "WMV3"                                   |
| Perfil avançado do Windows Media Video 9 | "WVC1"                                   |
| Imagem do vídeo 9,1 do Windows Media          | "WMVP" para 9,1, "WVP2" para 9,1 versão 2 |



 

## <a name="output-formats"></a>Formatos de saída

O decodificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um DMO.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

O decodificador de vídeo do Windows Media dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um MFT.

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="properties"></a>Propriedades

O decodificador de vídeo do Windows Media dá suporte às propriedades a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></td>
<td>Especifica se o codec decodifica quadros de vídeo entrelaçados do fluxo compactado como quadros progressivos.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Especifica se o decodificador usará o hardware de aceleração de vídeo do DirectX, se disponível.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Especifica o nível de energia para o decodificador.<br/> <dl> Windows 7.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Especifica se o decodificador deve usar a interpolação de quadros.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Especifica se o decodificador dá suporte à interpolação de quadros.<br/> <dl> Windows XP e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem<br />
Somente leitura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Especifica o número de threads que o decodificador usará.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Especifica o modo de pós-processamento do decodificador.<br/> <dl> Windows Vista e posterior.<br />
Perfil simples, perfil principal, perfil avançado, imagem.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Especifica se o decodificador deve ser drenado.<br/> <dl> Windows 8<br />
Somente leitura.<br />
</dl> Essa propriedade é usada pelo tempo de execução do Windows Media Format. O tipo de propriedade é <strong>VARIANT_BOOL</strong>. Se o valor for <strong>VARIANT_TRUE</strong>, o decodificador deverá ser esgotado após uma descontinuidade. Para obter mais informações sobre como descarregar uma MFT, consulte <a href="basic-mft-processing-model.md">modelo básico de processamento de MFT</a>.<br/>
<blockquote>
[!Note]<br />
Para consultar essa propriedade, use a interface <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

A resolução máxima permitida pelo decodificador do Windows Media Video 9 é 4096x4096.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 
