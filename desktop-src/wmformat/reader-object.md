---
title: Objeto de leitor
description: Objeto de leitor
ms.assetid: b5edbf8b-820f-4e09-a482-8efc2283360e
keywords:
- Windows SDK de Formato de Mídia, objetos de leitor
- FORMATO DE SISTEMAS Avançados (ASF), objetos de leitor
- ASF (Formato de Sistemas Avançados), objetos de leitor
- objetos, objetos de leitor
- objetos de leitor, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc1c01b824bbe278991f1512e963a6dde1727c00e73b3c17f5ab4c5556534b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089704"
---
# <a name="reader-object"></a>Objeto de leitor

O objeto leitor lê exemplos de dados de arquivos de mídia. Atualmente, o objeto de leitor dá suporte a arquivos usando a estrutura de arquivo ASF (formato de sistemas avançados), bem como arquivos MP3. Os dados entregues pelo objeto leitor são descompactados e prontos para renderização por padrão, embora os exemplos possam ser entregues sem serem descompactados, se desejado. Os exemplos são entregues de forma assíncrona do objeto de leitor; você deve configurar uma função de retorno de chamada para recebê-las. Para reprodução síncrona de arquivos ASF, use o objeto de leitor síncrono. Nem o leitor nem o leitor síncrono renderiza dados. Você deve fornecer suas próprias rotinas de renderização para exibir a mídia recuperada de um arquivo.

Quando um arquivo contém uma mídia codificada que pode ser decodificada com um codec com suporte pelo objeto de leitor, você pode controlar o formato da saída descompactada. Para alterar o formato de saída descompactada para um fluxo, você deve recuperar o objeto de propriedades de mídia de saída padrão para esse fluxo, fazer alterações nele e reatribuí-lo ao fluxo no leitor. Os objetos de propriedades de mídia de saída são subordinados ao objeto de leitor e só devem ser criados usando o [**método IWMReader::GetOutputProps.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops)

O objeto de leitor é criado pela [**função WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader), que define um ponteiro para uma interface **IWMReader.** As outras interfaces do objeto de leitor podem ser obtidas chamando o **método QueryInterface.**

As interfaces a seguir são suportadas pelo objeto de leitor.



| Interface                                                    | Descrição                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ireferenceclock**](ireferenceclock.md)                   | Fornece acesso ao relógio do sistema usado pelo leitor.                                                                                                                         |
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)                         | Gerencia a aquisição de licença, [*as propriedades drm*](wmformat-glossary.md) e a individualização do cliente.                                  |
| [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)                       | Fornece acesso a licenças que usam OPL (níveis de proteção de saída) para especificar direitos.                                                                                          |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)                       | Define e recupera informações de header, incluindo metadados, [*marcadores*](wmformat-glossary.md)e dados de script.                                                 |
| [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)                     | Recupera informações sobre os codecs que foram usados para codificar o conteúdo no arquivo. Herda todos os métodos de **IWMHeaderInfo**.                                      |
| [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)                     | Dá suporte a tamanhos de atributo grandes, nomes de atributo duplicados e suporte a vários idiomas. Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.              |
| [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)                       | Recupera o tamanho do maior pacote no arquivo carregado no leitor.                                                                                                      |
| [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)                     | Recupera o tamanho do menor pacote no arquivo carregado no leitor.                                                                                                     |
| [**IWMProfile**](iwmprofile.md)                             | Fornece acesso às informações de perfil do arquivo carregado no leitor.                                                                                                    |
| [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)                           | Recupera o GUID (identificador global exclusivo), se for o caso, associado ao perfil. Herda todos os métodos de **IWMProfile.**                                            |
| [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)                           | Dá suporte ao compartilhamento de largura de banda e informações de priorização de fluxo no perfil. Herda todos os métodos de **IWMProfile** e **IWMProfile2.**                             |
| [**IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)                               | Fornece recursos básicos de leitura de arquivo, incluindo operações como abrir, fechar, iniciar, pausar, retomar, parar e obter e definir as propriedades de saída.                  |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)         | Comunica-se com a aceleração de vídeo do DirectX.                                                                                                                                   |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)               | Fornece recursos avançados do leitor, como um relógio fornecido pelo usuário, alocação de buffer, estatísticas de retorno e notificações de seleção de fluxo.                              |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)             | Fornece um intervalo adicional de métodos avançados para um objeto de leitor existente. Herda todos os métodos de **IWMReaderAdvanced.**                                           |
| [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)             | Fornece controle avançado de busca e streaming. Herda todos os métodos de **IWMReaderAdvanced** e **IWMReaderAdvanced2**.                                               |
| [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)             | Fornece opções avançadas de leitor, incluindo suporte a vários idiomas. Herda todos os métodos de **IWMReaderAdvanced,** **IWMReaderAdvanced2** e **IWMReaderAdvanced3**. |
| [**IWMReaderNetworkConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)     | Controla as definições de configuração de rede.                                                                                                                                        |
| [**IWMReaderNetworkConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2)   | Fornece acesso a definições avançadas de configuração de rede. Herda todos os métodos de **IWMReaderNetworkConfig**.                                                          |
| [**IWMReaderStreamClock**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderstreamclock)         | Define e cancela temporizadores em relógios de fluxo e recupera o valor atual de um relógio de fluxo especificado.                                                                          |
| [**IWMReaderTimecode**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertimecode)               | Fornece informações sobre intervalos de código de tempo SMPTE no arquivo carregado no leitor.                                                                                             |
| [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation) | Testa se as alterações nas propriedades de saída de um fluxo estão funcionando corretamente.                                                                                                |



 

As interfaces de retorno de chamada a seguir podem ser implementadas no aplicativo para acompanhar o progresso de um objeto de leitor.



| Interface                                                      | Descrição                                                                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)         | Adquire as credenciais dos usuários e verifica se eles têm permissão para acessar um site remoto.                                               |
| [**IWMReaderAllocatorEx**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderallocatorex)           | Fornece alternativas expandidas para os **métodos AllocateForOutput** e **AllocateForStream** da interface **IWMReaderCallbackAdvanced.** |
| [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)                 | Fornece métodos de retorno de chamada para os **métodos Start** e **Open** de **IWMReader**.                                                            |
| [**IWMReaderCallbackAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced) | Fornece métodos de retorno de chamada para os métodos da interface [**IWMReaderAdvanced.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)                                    |
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)                 | Necessário quando as informações de status devem ser comunicadas ao aplicativo host.                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objetos**](objects.md)
</dt> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Objeto de leitor síncrono**](synchronous-reader-object.md)
</dt> </dl>

 

 




