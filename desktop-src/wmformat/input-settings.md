---
title: Entrada Configurações
description: Entrada Configurações
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows SDK de Formato de Mídia, constantes globais
- ASF (Advanced Systems Format), constantes globais
- ASF (Formato de Sistemas Avançados), constantes globais
- constantes globais, lista de
- Windows SDK de Formato de Mídia, constantes
- ASF (Advanced Systems Format), constantes
- ASF (Formato de Sistemas Avançados), constantes
- constantes, lista de
- Windows SDK de Formato de Mídia, configurações de entrada
- ASF (Advanced Systems Format), configurações de entrada
- ASF (Formato de Sistemas Avançados), configurações de entrada
- configurações de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad72a8a5cc70dc28dcaa7be1e24b721e0b3f644e7694ea5c00d87ba2418846a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701801"
---
# <a name="input-settings"></a>Entrada Configurações

As constantes globais a seguir são usadas para identificar as configurações de entrada para o autor.



| Constante global                        | WMT \_ ATTR \_ DATATYPE                                                                                                                       | Descrição *de pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeintermodMode                  | **WMT \_ DIGITE \_ DWORD** definido como um dos valores na tabela de modo no tópico [Para Desinteressar Vídeo](to-deinterlace-video.md).            | Quando definido, especifica o tipo de conteúdo entrelaçado da entrada. Para obter mais informações, consulte [Para desinteressar vídeo](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **TIPO WMT \_ \_ BOOL**                                                                                                                       | Quando definido como True, instrui o codec a não soltar quadros durante a codificação. Isso fará com que [*a taxa de quadros*](wmformat-glossary.md) do fluxo de vídeo de saída seja constante. A taxa de quadros do fluxo de entrada não precisa ser constante. |
| g \_ wszInitialPatternForInverseTelelore | **WMT \_ TYPE \_ DWORD** definido como um dos valores na tabela de padrão inicial no tópico [Para Desinteressar Vídeo](to-deinterlace-video.md). | Quando o modo de desinterversão é definido como WM \_ DM DEINTER LTDA, isso pode ser definido para especificar o padrão da \_ \_ entrada [*telegráfica.*](wmformat-glossary.md) Para obter mais informações, consulte [Para desinteressar vídeo](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **TIPO WMT \_ \_ BOOL**                                                                                                                       | Quando definido como True, especifica que o codec deve codificar o fluxo como conteúdo entrelaçado. Para obter mais informações, [consulte Para usar vídeo entrelaçados](to-use-interlaced-video.md).                                                                                       |
| g \_ wszJPEGCompressionQuality           | **WMT \_ TYPE \_ DWORD**                                                                                                                      | Especifica o nível de qualidade JPEG (de 1 a 100) a ser usado na entrada.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **GUID DE \_ TIPO \_ WMT**                                                                                                                       | O valor é definido como o GUID da marca-d'água.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **CADEIA DE CARACTERES DE \_ TIPO \_ WMT**                                                                                                                     | O valor é definido como a configuração de marca-d'água. Esse valor variará dependendo da marca d'água DMO. Consulte a documentação do sistema de marca d'água para obter mais informações.                                                                                   |



 

> [!Note]  
> As configurações de entrada configuradas para um fluxo não são persistentes no arquivo gravado. Se você quiser que o leitor personalizado tenha acesso a esses parâmetros de codificação, crie atributos personalizados para armazená-los no header do arquivo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




