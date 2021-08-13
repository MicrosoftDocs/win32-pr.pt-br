---
title: Windows Funções de cliente dos Serviços de Implantação
description: As funções a seguir são usadas com a API do cliente Windows Deployment Services.
ms.assetid: 4cedd8a8-7f46-4229-9d96-58965b751e43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c213822323405e030ba9907f692d6fcaa370356fb395a390dfa0f1fc0818244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118566381"
---
# <a name="windows-deployment-services-client-functions"></a>Windows Funções de cliente dos Serviços de Implantação

As funções a seguir são usadas com a API do cliente Windows Deployment Services.



| Função                                                                                 | Descrição                                                                                                                            |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [*PFN \_ WdsCliCallback*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclicallback)                                          | Mensagens de erro e notificação de progresso durante uma transferência de arquivo ou imagem.                                                              |
| [*PFN \_ WdsCliTraceFunction*](/windows/desktop/api/WdsClientAPI/nc-wdsclientapi-pfn_wdsclitracefunction)                                | Recebe mensagens de depuração do cliente WDS.                                                                                       |
| [**WdsCliAuthorizeSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession)                                 | Converte uma sessão anônima em uma sessão autenticada.                                                                           |
| [**WdsCliCancelTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicanceltransfer)                                     | Cancela uma operação de transferência do WDS.                                                                                                      |
| [**WdsCliClose**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliclose)                                                       | Fecha um handle para uma sessão ou imagem do WDS e libera recursos.                                                                      |
| [**WdsCliCreateSession**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession)                                       | Inicia uma nova sessão com um servidor WDS.                                                                                                |
| [**WdsCliFindFirstImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage)                                     | Inicia a enumeração de imagens armazenadas em um servidor WDS e retorna um alça de local que faz referência à primeira imagem.                     |
| [**WdsCliFindNextImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage)                                       | Avança a referência de um alça de local para a próxima imagem armazenada em um servidor WDS.                                                      |
| [**WdsCliFreeStringArray**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclifreestringarray)                                   | Libera a matriz de valores de cadeia de caracteres que é alocada pela [**função WdsCliObtainDriverPackages.**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages) |
| [**WdsCliGetEnumerationFlags**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags)                           | Retorna o sinalizador de enumeração de imagem para o alçamento de imagem atual.                                                                       |
| [**WdsCliGetImageArchitecture**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture)                         | Retorna a arquitetura do processador para a imagem atual.                                                                              |
| [**WdsCliGetImageDescription**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription)                           | Retorna a descrição da imagem atual.                                                                                          |
| [**WdsCliGetImageGroup**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup)                                       | Retorna o nome do grupo de imagens para a imagem atual.                                                                                    |
| [**WdsCliGetImageHalName**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname)                                   | Retorna o nome DAL (Camada de Abstração de Hardware) para a imagem atual.                                                               |
| [**WdsCliGetImageHandleFromFindHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromfindhandle)         | Retorna um alça de imagem para a imagem atual.                                                                                         |
| [**WdsCliGetImageHandleFromTransferHandle**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehandlefromtransferhandle) | Retorna um alça de imagem de um alça de transferência concluído.                                                                              |
| [**WdsCliGetImageIndex**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex)                                       | Retorna o índice de imagem para a imagem atual.                                                                                         |
| [**WdsCliGetImageLanguage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage)                                 | Retorna o idioma padrão da imagem atual.                                                                                     |
| [**WdsCliGetImageLanguages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages)                               | Retorna uma matriz de idiomas com suporte na imagem atual.                                                                          |
| [**WdsCliGetImageLastModifiedTime**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime)                 | Retorna a hora da última modificação para a imagem atual.                                                                                  |
| [**WdsCliGetImageName**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename)                                         | Retorna o nome da imagem atual.                                                                                                 |
| [**WdsCliGetImageNamespace**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligetimagenamespace)                               | Retorna o nome da imagem atual.                                                                                                 |
| [**WdsCliGetImagePath**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath)                                         | Retorna o caminho para o arquivo de imagem que contém a imagem atual.                                                                    |
| [**WdsCliGetImageSize**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize)                                         | Retorna o tamanho da imagem atual.                                                                                                 |
| [**WdsCliGetImageVersion**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion)                                   | Retorna a versão da imagem atual.                                                                                              |
| [**WdsCliGetTransferSize**](/windows/desktop/api/WdsClientApi/nf-wdsclientapi-wdscligettransfersize)                                   | Retorna o tamanho da transferência atual.                                                                                              |
| [**WdsCliInitializeLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog)                                       | Inicializa o log do cliente.                                                                                                    |
| [**WdsCliLog**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclilog)                                                           | Envia um evento de log para o servidor WDS.                                                                                                   |
| [**WdsCliObtainDriverPackages**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackages)                         | Obtém de uma imagem do WDS, os pacotes de driver (arquivos INF) que podem ser usados neste computador.                                           |
| [**WdsCliRegisterTrace**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliregistertrace)                                       | Registra uma função de retorno de chamada que receberá mensagens de depuração.                                                                    |
| [**WdsCliTransferFile**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferfile)                                         | Transfere um arquivo de um servidor WDS para o cliente WDS usando um protocolo de transferência multicast.                                              |
| [**WdsCliTransferImage**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdsclitransferimage)                                       | Transfere uma imagem de um servidor WDS.                                                                                                  |
| [**WdsCliWaitForTransfer**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliwaitfortransfer)                                   | Aguarda a conclusão de uma transferência.                                                                                                      |



 



| Função                                                             | Descrição                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WdsCliGetDriverQueryXml**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscligetdriverqueryxml)           | Gera uma cadeia de caracteres XML que pode ser usada para consultar um servidor WDS para pacotes de driver. Disponível a partir do Windows 8 e Windows Server 2012.               |
| [**WdsCliObtainDriverPackagesEx**](/windows/desktop/api/WdsClientAPI/nf-wdsclientapi-wdscliobtaindriverpackagesex) | Obtém os pacotes de driver (arquivos INF) aplicáveis ao XML de consulta de driver WDS especificado. Disponível a partir do Windows 8 e Windows Server 2012. |



 

 

 




