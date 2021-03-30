---
title: Objeto do gravador
description: Objeto do gravador
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- SDK do Windows Media Format, objetos do Writer
- Formato de sistema avançado (ASF), objetos de gravador
- ASF (formato de sistemas avançados), objetos de gravador
- objetos, objetos de gravador
- objetos do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640304"
---
# <a name="writer-object"></a>Objeto do gravador

O objeto Writer é usado para gravar arquivos de mídia digital usando a estrutura de arquivos ASF (Advanced Systems Format). O processo de gravação de um arquivo de mídia digital envolve muitas etapas internas ao gravador, que coordenam a compactação, o pacote e a multiplexação.

O objeto gravador inclui interfaces para saída para arquivos ou uma rede, dá suporte a uma interface de retorno de chamada e pode criar um ou mais objetos de propriedades de mídia de entrada.

O objeto Writer é criado pela função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), que define um ponteiro para uma interface **IWMWriter** . As outras interfaces do objeto gravador podem ser obtidas chamando o método **QueryInterface** .

As interfaces a seguir são suportadas pelo objeto gravador.



| Interface                                          | Descrição                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | Fornece métodos para gerar chaves [*DRM*](wmformat-glossary.md) .                                                                                                |
| [**IWMDRMWriter2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | Configura o objeto gravador para gravar um arquivo que contém um fluxo previamente criptografado que está em conformidade com o protocolo Windows Media DRM 10 para dispositivos de rede.                                                    |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | Gerencia a especificação e a recuperação de informações de cabeçalho, como metadados, [*marcadores*](wmformat-glossary.md)e assim por diante.                                                           |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | Gerencia a enumeração por meio das informações de codec disponíveis. Herda todos os métodos de **IWMHeaderInfo**.                                                                                            |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | Gerencia a enumeração por meio das informações de codec disponíveis. Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.                                                                     |
| [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | Fornece acesso a informações sobre os sistemas de marca d' água presentes no sistema.                                                                                                                          |
| [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | Inicia e interrompe a gravação de arquivos ASF; Ele inclui métodos para alocar buffers, configurar e recuperar propriedades de entrada, definir perfis e nomes de arquivos de saída e desbloquear o gravador.         |
| [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | Adiciona, obtém e remove objetos de coletor especificados; Recupera estatísticas, número de coletores e a hora do relógio para o qual o gravador está trabalhando; e executa outras funções avançadas.                                |
| [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | Fornece algumas funcionalidades avançadas, especialmente para lidar com vídeo desentrelaçado. Herda todos os métodos de **IWMWriterAdvanced**.                                                                 |
| [**IWMWriterAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | Fornece funcionalidade de gravador adicional, incluindo a capacidade de obter estatísticas de gravador detalhadas. Herda todos os métodos de **IWMWriterAdvanced** e **IWMWriterAdvanced2**.                       |
| [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | Gerencia algumas funcionalidades de gravação avançadas relacionadas a exemplos de visualização. A visualização está exibindo a saída, geralmente de um codificador, para verificar se o processo de codificação/decodificação está funcionando corretamente. |
| [**IWMWriterPreprocess**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | Gerencia passagens de pré-processamento feitas pelo gravador. Os passos de pré-processamento são usados para melhorar a qualidade da saída codificada.                                                                                  |



 

A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para acompanhar o progresso da visualização.



| Interface                                                      | Descrição                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IWMWriterPostViewCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | Gerencia como exemplos não compactados são recebidos do objeto gravador para visualizar o que o codec está fazendo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




