---
title: Configurações de entrada
description: Configurações de entrada
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- SDK do Windows Media Format, constantes globais
- ASF (Advanced Systems Format), constantes globais
- ASF (formato de sistemas avançados), constantes globais
- constantes globais, lista de
- SDK do Windows Media Format, constantes
- ASF (Advanced Systems Format), constantes
- ASF (formato de sistemas avançados), constantes
- constantes, lista de
- SDK do Windows Media Format, configurações de entrada
- ASF (Advanced Systems Format), configurações de entrada
- ASF (formato de sistemas avançados), configurações de entrada
- configurações de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007079"
---
# <a name="input-settings"></a>Configurações de entrada

As constantes globais a seguir são usadas para identificar as configurações de entrada para o gravador.



| Constante global                        | \_tipo de \_ dados attr WMT                                                                                                                       | Descrição de *uma* era                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_ Digite \_ DWORD** definido como um dos valores na tabela modo no tópico [como desentrelaçar vídeo](to-deinterlace-video.md).            | Quando definido, especifica o tipo de conteúdo entrelaçado da entrada. Para obter mais informações, consulte [para desentrelaçar vídeo](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **WMT \_ tipo \_ bool**                                                                                                                       | Quando definido como true, instrui o codec para não descartar nenhum quadro durante a codificação. Isso fará com que a [*taxa de quadros*](wmformat-glossary.md) do fluxo de vídeo de saída seja constante. A taxa de quadros do fluxo de entrada não precisa ser constante. |
| g \_ wszInitialPatternForInverseTelecine | **WMT \_ Digite \_ DWORD** definido como um dos valores na tabela padrão inicial no tópico [para desentrelaçar o vídeo](to-deinterlace-video.md). | Quando o modo de desentrelaçamento é definido como WM \_ DM \_ desentrelaçar \_ INVERSETELECINE, isso pode ser definido para especificar o padrão da entrada de [*telecineon*](wmformat-glossary.md) . Para obter mais informações, consulte [para desentrelaçar vídeo](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **WMT \_ tipo \_ bool**                                                                                                                       | Quando definido como true, especifica que o codec deve codificar o fluxo como conteúdo entrelaçado. Para obter mais informações, consulte [para usar vídeo entrelaçado](to-use-interlaced-video.md).                                                                                       |
| g \_ wszJPEGCompressionQuality           | **WMT \_ tipo \_ DWORD**                                                                                                                      | Especifica o nível de qualidade JPEG (de 1 a 100) a ser usado na entrada.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **\_GUID do tipo WMT \_**                                                                                                                       | O valor é definido como o GUID de marca d' água.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **Cadeia de caracteres do \_ tipo WMT \_**                                                                                                                     | O valor é definido como a configuração da marca d' água. Esse valor variará dependendo da marca d' água do DMO. Consulte a documentação do sistema de marca d' água para obter mais informações.                                                                                   |



 

> [!Note]  
> As configurações de entrada configuradas para um fluxo não são mantidas no arquivo gravado. Se desejar que seu leitor personalizado tenha acesso a esses parâmetros de codificação, você deverá criar atributos personalizados para armazená-los no cabeçalho do arquivo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




