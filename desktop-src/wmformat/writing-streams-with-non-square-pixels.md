---
title: gravando Fluxos com Pixels não quadrados
description: gravando Fluxos com Pixels não quadrados
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows SDK de formato de mídia, gravando fluxos de vídeo
- Windows SDK do formato de mídia, fluxos de vídeo
- Windows SDK de formato de mídia, pixels não quadrados
- Windows SDK do formato de mídia, pixels (não quadrado)
- ASF (Advanced Systems Format), gravando fluxos de vídeo
- ASF (formato de sistemas avançados), gravando fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (formato de sistemas avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (formato de sistemas avançados), pixels (não quadrado)
- gravando fluxos de vídeo
- fluxos de vídeo, gravando
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b44df1e4b4ce3f2bf2cb0e1d795b4caf396b6396e3e70b68b9040ad9a5456f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657946"
---
# <a name="writing-streams-with-non-square-pixels"></a>gravando Fluxos com Pixels não quadrados

Há duas maneiras de criar fluxos de vídeo com pixels não quadrados que serão exibidos corretamente no Windows Media Player. A primeira técnica envolve a definição de atributos de nível de fluxo no cabeçalho do arquivo. A segunda técnica envolve adicionar uma extensão de unidade de dados a um fluxo no perfil e, em seguida, definir um valor para ela em cada exemplo que é gravada.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>Para usar atributos de cabeçalho no nível de fluxo para definir a taxa de proporção de pixel

1.  Configure o objeto gravador. Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).
2.  Crie ou carregue um perfil com um ou mais fluxos de vídeo. Para obter mais informações, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).
3.  Chame [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). (Sempre Chame esse método antes de definir qualquer atributo de cabeçalho.)
4.  Chame **QueryInterface** para obter a interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) e chame [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) duas vezes para adicionar [**AspectRatioX**](aspectratiox.md) e [**AspectRatioY**](aspectratioy.md) como atributos de nível de fluxo do fluxo de vídeo. Esses atributos são valores **DWORD** .
5.  Grave o arquivo.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>Para usar extensões de unidade de dados para definir a taxa de proporção de pixel

**Antes de escrever:**

1.  Configure o objeto gravador. Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).
2.  Crie ou carregue um perfil com um ou mais fluxos de vídeo. Para obter mais informações, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).
3.  Para cada fluxo (de qualquer tipo de mídia) no perfil, chame [**IWMStreamConfig:: Setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) para especificar um nome exclusivo de sua escolha. Não dê ao mesmo nome dois fluxos.
4.  Use [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) no fluxo de vídeo para adicionar uma extensão de unidade de dados para taxa de proporção de pixel.
5.  Chame [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Grave o arquivo.

**Durante a gravação:**

-   Para cada exemplo, chame [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) e especifique a \_ Propriedade PixelAspectRatio do WM SampleExtensionGUID \_ juntamente com o valor correto. Os valores de taxa de proporção são gravados como dois valores de dois dígitos concatenados. Por exemplo, 16:9 é escrito como 1609 ou 0x0649. Esse é sempre um valor de 2 bytes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**para ler e gravar Fluxos de vídeo com Pixels não quadrados**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




