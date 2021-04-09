---
title: Uso da API de cliente de Serviços de Implantação do Windows
description: Em ambientes em que uma solução padrão de WDS (serviços de implantação do Windows) não pode ser usada para instalar o Windows, a API do cliente WDS permite que os desenvolvedores gravem aplicativos de implantação personalizados.
ms.assetid: abe2a7c7-989a-456e-80df-90d5b816db38
keywords:
- Serviços de implantação do Windows serviços de implantação do Windows, usando a API do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 872422a5c84bf1d8ea7c3688b122ba2389c1e968
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007693"
---
# <a name="using-the-windows-deployment-services-client-api"></a>Uso da API de cliente de Serviços de Implantação do Windows

Em ambientes em que uma solução padrão de WDS (serviços de implantação do Windows) não pode ser usada para instalar o Windows, a API do cliente WDS permite que os desenvolvedores gravem aplicativos de implantação personalizados. Os aplicativos podem usar essa API para se comunicar com o servidor WDS para obter informações sobre as imagens do sistema disponíveis no servidor. Os aplicativos cliente do WDS personalizados devem aderir às diretrizes a seguir.

## <a name="install-the-wds-role-on-the-server"></a>Instalar a função do WDS no servidor

-   O WDS (serviços de implantação do Windows) é a versão revisada do RIS (serviços de instalação remota), você precisará da função de servidor do WDS no servidor para implementar soluções personalizadas de cliente do WDS.
-   O WDS substitui o RIS como o componente padrão a partir do Windows Server 2008 e do Windows Server 2003 com Service Pack 2 (SP2).
-   Você deve atualizar o servidor RIS para o WDS no Windows Server 2003 com Service Pack 1 (SP1). Você pode instalar a função de servidor do WDS com o [WAIK (Kit de instalação automatizada do Windows)](https://www.microsoft.com/download/details.aspx?id=10333).

## <a name="start-windows-pe-20"></a>Iniciar o Windows PE 2,0

O Windows PE 2,0 deve ser iniciado, se ainda não tiver iniciado. O cliente do WDS e as DLLs de suporte são carregados somente pelo setup.exe quando está na fase do Microsoft Ambiente de Pré-Instalação do Windows (Windows PE 2,0) do processamento da instalação.

-   Quando um novo computador está conectado à rede, a tecnologia de PXE (Preboot Execution Environment) interna pode ser usada para baixar o programa de inicialização de rede. Para obter mais informações sobre a inicialização PXE de um computador para instalar o Windows, consulte [o guia passo a passo de atualização dos serviços de implantação do Windows](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)).
-   Uma imagem inicializável de RAMDISK do Windows PE 2,0 pode ser armazenada no. Formato WIM e baixado como parte do processo de inicialização de rede. O Windows PE pode ser carregado e executado diretamente dessa mídia.

## <a name="open-a-session-with-the-wds-server"></a>Abrir uma sessão com o servidor WDS

O cliente do WDS deve abrir uma sessão com um servidor WDS.

-   Use a função [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) para abrir uma sessão com um servidor WDS. Essa função usa o nome ou o endereço IP do servidor e recebe o endereço do identificador para a sessão de cliente do WDS.
-   Se a abertura da sessão com o servidor exigir autenticação do cliente WDS, o aplicativo deverá fornecer o endereço de uma estrutura de [**\_ \_ credenciais da CLI do WDS**](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred) que contém as credenciais do cliente ao chamar a função [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) . O aplicativo pode usar a função [**WdsCliAuthorizeSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliauthorizesession) para converter uma sessão anônima em uma sessão autenticada.
-   Quando a sessão aberta com a função [**WdsCliCreateSession**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclicreatesession) não for mais necessária, o aplicativo deverá usar a função [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) para fechar a alça e liberar os recursos mantidos pela sessão.

## <a name="enumerate-system-images-on-the-wds-server"></a>Enumerar imagens do sistema no servidor WDS

O cliente do WDS pode usar a API para enumerar as imagens do sistema no servidor do WDS.

-   Use a função [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) para obter um identificador para a primeira imagem e para inicializar a enumeração de imagens no servidor WDS.
-   Use a função [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) para incrementar a enumeração iniciada pela função [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) . A função **WdsCliFindNextImage** Obtém o identificador para a próxima imagem.
-   Use a função [**WdsCliGetImageIndex**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageindex) para obter o índice de imagem para a imagem atual. Esse valor é válido somente até que as funções [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) ou [**WdsCliClose**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliclose) sejam usadas novamente.
-   Use a função [**WdsCliGetEnumerationFlags**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetenumerationflags) para obter sinalizadores informativos sobre filtragem de imagem.

## <a name="get-information-about-images"></a>Obter informações sobre imagens

O cliente WDS pode usar a API para obter informações sobre as imagens em um servidor WDS. As funções a seguir obtêm informações sobre a imagem atual. Como as funções [**WdsCliFindFirstImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindfirstimage) e [**WdsCliFindNextImage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclifindnextimage) alteram o valor do identificador da imagem atual, o aplicativo deve armazenar todas as informações obtidas e serão necessárias no futuro antes de chamar as funções **WdsCliFindFirstImage** ou **WdsCliFindNextImage** novamente.

-   Use a função [**WdsCliGetImageArchitecture**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagearchitecture) para obter a arquitetura do processador da imagem atual.
-   Use a função [**WdsCliGetImagePath**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagepath) para obter o caminho relativo para o arquivo de imagem que contém a imagem atual.
-   Use a função [**WdsCliGetImageSize**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagesize) para obter o tamanho da imagem.
-   Use a função [**WdsCliGetImageVersion**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimageversion) para obter a versão da imagem.
-   Use a função [**WdsCliGetImageLanguage**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguage) para obter o idioma padrão da imagem atual.
-   Use a função [**WdsCliGetImageLanguages**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelanguages) para obter uma matriz de idiomas com suporte pela imagem atual.
-   Use o [**WdsCliGetImageLastModifiedTime**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagelastmodifiedtime) retorna a hora da última modificação da imagem atual.
-   Use a função [**WdsCliGetImageName**](/windows/win32/api/WdsClientApi/nf-wdsclientapi-wdscligetimagename) para obter o nome da imagem atual.
-   Use a função [**WdsCliGetImageDescription**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagedescription) para obter a descrição da imagem atual.
-   Use a função [**WdsCliGetImageGroup**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagegroup) para obter o nome do grupo de imagens para a imagem atual.
-   Use a função [**WdsCliGetImageHalName**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscligetimagehalname) para obter o nome da camada de abstração de hardware (Hal) para a imagem atual.

## <a name="log-wds-client-events"></a>Registrar eventos do cliente do WDS

A funcionalidade de log da biblioteca de cliente do WDS permite que os eventos de progresso da instalação sejam enviados do cliente para o servidor do WDS.

-   Use a função [**WdsCliInitializeLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdscliinitializelog) para inicializar o log para a sessão de cliente do WDS.
-   Use a função [**WdsCliLog**](/windows/win32/api/WdsClientAPI/nf-wdsclientapi-wdsclilog) para gravar mensagens de evento no log do servidor WDS.
-   No Windows Server 2008, o servidor WDS grava eventos do cliente em um log de eventos específico do aplicativo que é visível por meio de eventvwr.exe, bem como o log de rastreamento de depuração. No Windows Server 2003 com log de depuração habilitado, o servidor WDS gravará eventos de cliente no arquivo de log localizado em% windir% \\ Tracing \\ wdsserver. log. O registro em log do cliente do WDS deve estar habilitado no servidor para capturar esses eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a API dos serviços de implantação do Windows](about-the-windows-deployment-services-api.md)
</dt> <dt>

[Uso da API de servidor de Serviços de Implantação do Windows](using-the-windows-deployment-services-server-api.md)
</dt> </dl>

 

 