---
title: Criando um aplicativo Windows de Gerenciador de Dispositivos mídia
description: Criando um aplicativo Windows de Gerenciador de Dispositivos mídia
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Mídia Gerenciador de Dispositivos, criando aplicativos
- Gerenciador de Dispositivos, criando aplicativos
- Windows Mídia Gerenciador de Dispositivos, guia de programação
- Gerenciador de Dispositivos,guia de programação
- guia de programação, aplicativos da área de trabalho
- guia de programação, Windows mídia Gerenciador de Dispositivos
- guia de programação, plug-ins
- guia de programação, criação de aplicativos
- Windows Mídia Gerenciador de Dispositivos, aplicativos da área de trabalho
- Gerenciador de Dispositivos aplicativos da área de trabalho
- Windows Mídia Gerenciador de Dispositivos,plug-ins
- Gerenciador de Dispositivos,plug-insp
- plug-ins, criando
- plug-ins, guia de programação
- aplicativos da área de trabalho, criando
- criando Windows de Gerenciador de Dispositivos mídia, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba468d4d9a04176847259087b8ba2626c2ffa3e0cac089f8433993320a7e125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585553"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Criando um aplicativo Windows de Gerenciador de Dispositivos mídia

Esta seção descreve como usar o Windows mídia Gerenciador de Dispositivos em seu aplicativo. O termo "aplicativo" aqui significa um executável, como um player de mídia ou um plug-in COM, como um plug-in de medição.

A Microsoft inclui vários provedores de serviços com o Windows XP e o Windows Media Player 10, incluindo um provedor de serviços MTP, um provedor de serviços Windows CE (para dispositivos que executam o Windows CE e usando o protocolo VIOLAI, como o Pocket PC) e um provedor de serviços para dispositivos MSC (categoria de armazenamento em massa). Você também pode criar seu próprio provedor de serviços para garantir a comunicação com seu próprio dispositivo; Para obter mais informações, consulte [Criando um provedor de serviços](creating-a-service-provider.md).

Há vários provedores de serviços herdado de terceiros que abordam um dispositivo não MTP, não VIOLAI ou não MSC de um determinado fabricante. Esses provedores de serviços são incluídos no disco do driver fornecido com esses dispositivos.

Um aplicativo que usa Windows Mídia Gerenciador de Dispositivos deve executar as etapas a seguir.

1.  **Esteja ciente dos problemas de privacidade envolvidos no desenvolvimento de um aplicativo.** Confira [Política de privacidade](privacy-statement.md) para saber mais sobre alguns problemas de privacidade que envolvem o desenvolvimento de um Windows de Gerenciador de Dispositivos de mídia.
2.  **Inclua a biblioteca e os arquivos de header necessários para seu aplicativo.** Consulte [Arquivos de biblioteca e de header necessários para um](required-library-and-header-files-for-an-application.md) aplicativo para saber quais arquivos você precisará incluir em seu projeto.
3.  **Autenture o aplicativo e adquira a interface IWMDMDevice raiz.** A primeira tarefa que um aplicativo deve fazer para usar Windows mídia Gerenciador de Dispositivos é autenticar a si mesmo. Esse processo verifica a identidade do aplicativo para o Windows Media Gerenciador de Dispositivos usando um certificado fictício para funcionalidade limitada do Windows Media Gerenciador de Dispositivos ou usando um certificado oficial para funcionalidade completa. Para obter mais informações, [consulte Autenticando o aplicativo.](authenticating-the-application.md)
4.  **Enumerar os dispositivos conectados.** A primeira etapa na comunicação com dispositivos é descobrir quais dispositivos estão conectados e acessíveis para Windows mídia Gerenciador de Dispositivos. Para obter mais informações, consulte [Enumerando dispositivos](enumerating-devices.md).
5.  **Verifique o status dos componentes drm do dispositivo.** Para usar arquivos protegidos por DRM, um dispositivo deve ser criado em alguma versão do drm de mídia Windows para dispositivos portáteis e os componentes drm devem estar atualizados. Antes de começar a manipular arquivos no dispositivo, é melhor ver se o dispositivo dá suporte a arquivos protegidos por DRM e se o dispositivo precisa ser atualizado. Para obter mais informações, [consulte Tratamento de conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md).
6.  **Explorar um dispositivo.** Depois de encontrar o dispositivo que deseja, você pode explorar o conteúdo desse dispositivo. Para obter mais informações, consulte [Explorando um dispositivo](exploring-a-device.md).
7.  **Ler arquivos do dispositivo e gravar arquivos no dispositivo.** Depois de saber mais sobre o layout do dispositivo, você pode começar a transferir arquivos de e para o dispositivo. Para obter mais informações, consulte [Lendo arquivos do dispositivo e](reading-files-from-the-device.md) escrevendo arquivos no [dispositivo](writing-files-to-the-device.md).
8.  **Crie playlists no dispositivo.** Um tipo de arquivo que você pode gravar no dispositivo é um arquivo abstrato, que é uma coleção de referências a outros arquivos. Embora a capacidade de gravar arquivos abstratos em um dispositivo dependa do provedor de serviços e do dispositivo, geralmente apenas os dispositivos MTP têm essa funcionalidade. Para obter mais informações, consulte [Criando uma playlist no dispositivo](creating-a-playlist-on-the-device.md).

Além dessas etapas, há vários outros recursos que você pode habilitar em seu aplicativo:

-   **Notificações.** Você pode permitir que seu aplicativo receba notificações quando os dispositivos se conectam ou se desconectam do computador. Para obter mais informações, consulte [Habilitando notificações](enabling-notifications.md).
-   **Log.** Windows A Gerenciador de Dispositivos mídia usa um objeto de log que salva um registro de suas ações em um arquivo de texto local. Você pode adicionar mensagens a esse log para ajudá-lo a analisar erros ou desempenho em seu aplicativo. Para obter mais informações, consulte [Habilitando o registro em log.](enabling-logging.md)
-   **Uso de conteúdo de medição.** Você pode recuperar estatísticas de uso de conteúdo para licenças que concedem esse direito. Em seguida, essas estatísticas podem ser enviadas até um servidor Web para calcular pagamentos de imposto para proprietários de conteúdo. Para obter mais informações, consulte [Medição do uso de conteúdo.](metering-content-usage.md)

**Uma observação de cuidado**

Seu aplicativo pode precisar trabalhar com uma variedade de dispositivos, incluindo alguns que você não desenvolveu e nunca testou seu código. Esses dispositivos podem ou não responder com precisão a consultas e comandos ou implementar MTP ou outras especificações. Inclua a funcionalidade robusta de verificação de erros e fallback para lidar com o inesperado. Programa de forma defensiva.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




