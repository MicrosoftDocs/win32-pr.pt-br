---
description: o decodificador Windows media Video 9 decodifica fluxos de vídeo que foram codificados pelo codificador de vídeo de mídia Windows.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Decodificador de vídeo de mídia 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b251b46c94ef88283577dbd8268c3275d8ed6aab9321c98e115a42501e2729ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237258"
---
# <a name="windows-media-video-9-decoder"></a>Windows Decodificador de vídeo de mídia 9

o decodificador Windows media Video 9 decodifica fluxos de vídeo que foram codificados pelo [**codificador de vídeo de mídia Windows**](windowsmediavideo9encoder.md). O codificador e o decodificador dão suporte às quatro categorias de vídeo codificadas a seguir.

-   Windows Perfil simples de vídeo de mídia 9
-   Windows Perfil principal do vídeo de mídia 9
-   Windows Perfil avançado de vídeo de mídia 9
-   Windows Imagem de vídeo de mídia 9,1

## <a name="class-identifier"></a>Identificador de classe

o identificador de classe (CLSID) para o decodificador de vídeo de mídia Windows é representado pela constante **CLSID \_ CWMVDecMediaObject**. Você pode criar uma instância do decodificador de vídeo chamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfaces

um objeto de decodificador de vídeo expõe a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que o objeto possa ser usado como um objeto de mídia DirectX (DMO) e expõe a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que o objeto possa ser usado como uma Media Foundation transformação (MFT).

um decodificador de vídeo se comporta como um DMO ou um MFT dependendo de quais interfaces você obtém e qual versão do Windows está sendo executada. a tabela a seguir mostra as condições sob as quais um decodificador de vídeo se comporta como um DMO ou um MFT.



| Sistema operacional            | Comportamento do decodificador                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | um decodificador de vídeo de mídia Windows sempre se comporta como um DMO.                                                                                                                |
| Windows Vista e Windows 7 | por padrão, um decodificador de vídeo de mídia Windows se comporta como um DMO. Se você obtiver uma interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) em um decodificador de vídeo, ele se comporta como um MFT. |



 

a partir do Windows 7, o decodificador de vídeo de mídia Windows implementa a interface [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Formatos de entrada

a tabela a seguir mostra os códigos de quatro caracteres (fourcc) que correspondem às categorias de entrada codificada que são suportadas pelo decodificador de vídeo de mídia Windows.



| Categoria                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Perfil simples de vídeo de mídia 9   | "WMV3"                                   |
| Windows Perfil principal do vídeo de mídia 9     | "WMV3"                                   |
| Windows Perfil avançado de vídeo de mídia 9 | "WVC1"                                   |
| Windows Imagem de vídeo de mídia 9,1          | "WMVP" para 9,1, "WVP2" para 9,1 versão 2 |



 

## <a name="output-formats"></a>Formatos de saída

o decodificador de vídeo de mídia Windows dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como um DMO.

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

o decodificador de vídeo de mídia Windows dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um MFT.

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

o decodificador de vídeo de mídia Windows dá suporte às propriedades a seguir.



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
</dl> essa propriedade é usada pelo tempo de execução do Windows Media format. O tipo de propriedade é <strong>VARIANT_BOOL</strong>. Se o valor for <strong>VARIANT_TRUE</strong>, o decodificador deverá ser esgotado após uma descontinuidade. Para obter mais informações sobre como descarregar uma MFT, consulte <a href="basic-mft-processing-model.md">modelo básico de processamento de MFT</a>.<br/>
<blockquote>
[!Note]<br />
Para consultar essa propriedade, use a interface <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

a resolução máxima permitida pelo decodificador Windows Media Video 9 é 4096x4096.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Implementação de codec](codecimplementation.md)
</dt> </dl>

 

 
