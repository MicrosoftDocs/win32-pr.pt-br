---
title: Funções de cliente dos serviços de implantação do Windows
description: As funções a seguir são usadas com a API de cliente dos serviços de implantação do Windows.
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe124c6f02d12943d40fbc98af4a687d5b892f86
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105797895"
---
# <a name="windows-deployment-services-client-functions"></a>Funções de cliente dos serviços de implantação do Windows

As funções a seguir são usadas com a API de cliente dos serviços de implantação do Windows.



| Função                                                                                 | Descrição                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsCliCallback*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | Notificação de progresso e mensagens de erro durante uma transferência de arquivo ou imagem.                                                              |
| [*PFN \_ WdsCliTraceFunction*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | Recebe mensagens de depuração do cliente WDS.                                                                                       |
| [**WdsCliAuthorizeSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | Converte uma sessão anônima em uma sessão autenticada.                                                                           |
| [**WdsCliCancelTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | Cancela uma operação de transferência do WDS.                                                                                                      |
| [**WdsCliClose**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | Fecha um identificador para uma sessão ou imagem do WDS e libera recursos.                                                                      |
| [**WdsCliCreateSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | Inicia uma nova sessão com um servidor WDS.                                                                                                |
| [**WdsCliFindFirstImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | Inicia a enumeração de imagens armazenadas em um servidor WDS e retorna um identificador de localização que faz referência à primeira imagem.                     |
| [**WdsCliFindNextImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | Avança a referência de um identificador de localização para a próxima imagem armazenada em um servidor WDS.                                                      |
| [**WdsCliFreeStringArray**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | Libera a matriz de valores de cadeia de caracteres que é alocada pela função [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) . |
| [**WdsCliGetEnumerationFlags**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | Retorna o sinalizador de enumeração de imagem para o identificador de imagem atual.                                                                       |
| [**WdsCliGetImageArchitecture**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | Retorna a arquitetura do processador para a imagem atual.                                                                              |
| [**WdsCliGetImageDescription**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | Retorna a descrição da imagem atual.                                                                                          |
| [**WdsCliGetImageGroup**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | Retorna o nome do grupo de imagens da imagem atual.                                                                                    |
| [**WdsCliGetImageHalName**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | Retorna o nome da camada de abstração de hardware (HAL) para a imagem atual.                                                               |
| [**WdsCliGetImageHandleFromFindHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | Retorna um identificador de imagem para a imagem atual.                                                                                         |
| [**WdsCliGetImageHandleFromTransferHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | Retorna um identificador de imagem de um identificador de transferência concluído.                                                                              |
| [**WdsCliGetImageIndex**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | Retorna o índice de imagem para a imagem atual.                                                                                         |
| [**WdsCliGetImageLanguage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | Retorna o idioma padrão da imagem atual.                                                                                     |
| [**WdsCliGetImageLanguages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | Retorna uma matriz de idiomas com suporte pela imagem atual.                                                                          |
| [**WdsCliGetImageLastModifiedTime**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | Retorna a hora da última modificação da imagem atual.                                                                                  |
| [**WdsCliGetImageName**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | Retorna o nome da imagem atual.                                                                                                 |
| [**WdsCliGetImageNamespace**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | Retorna o nome da imagem atual.                                                                                                 |
| [**WdsCliGetImagePath**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | Retorna o caminho para o arquivo de imagem que contém a imagem atual.                                                                    |
| [**WdsCliGetImageSize**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | Retorna o tamanho da imagem atual.                                                                                                 |
| [**WdsCliGetImageVersion**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | Retorna a versão da imagem atual.                                                                                              |
| [**WdsCliGetTransferSize**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | Retorna o tamanho da transferência atual.                                                                                              |
| [**WdsCliInitializeLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | Inicializa o log para o cliente.                                                                                                    |
| [**WdsCliLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | Envia um evento de log para o servidor WDS.                                                                                                   |
| [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | Obtém-se de uma imagem do WDS, os pacotes de driver (arquivos INF) que podem ser usados neste computador.                                           |
| [**WdsCliRegisterTrace**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | Registra uma função de retorno de chamada que receberá mensagens de depuração.                                                                    |
| [**WdsCliTransferFile**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | Transfere um arquivo de um servidor WDS para o cliente do WDS usando um protocolo de transferência multicast.                                              |
| [**WdsCliTransferImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | Transfere uma imagem de um servidor WDS.                                                                                                  |
| [**WdsCliWaitForTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | Aguarda a conclusão de uma transferência.                                                                                                      |



 



| Função                                                             | Descrição                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WdsCliGetDriverQueryXml**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | Gera uma cadeia de caracteres XML que pode ser usada para consultar um servidor WDS para pacotes de driver. Disponível a partir do Windows 8 e do Windows Server 2012.               |
| [**WdsCliObtainDriverPackagesEx**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | Obtém os pacotes de driver (arquivos INF) que são aplicáveis ao XML de consulta do driver do WDS especificado. Disponível a partir do Windows 8 e do Windows Server 2012. |



 

 

 




