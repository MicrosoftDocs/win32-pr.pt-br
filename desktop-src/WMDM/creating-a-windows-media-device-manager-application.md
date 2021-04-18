---
title: Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows
description: Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows
ms.assetid: 6a200bd9-19dd-4130-acb4-e038b469c334
keywords:
- Windows Media Gerenciador de Dispositivos, criando aplicativos
- Gerenciador de Dispositivos, criando aplicativos
- Windows Media Gerenciador de Dispositivos, guia de programação
- Gerenciador de Dispositivos, guia de programação
- Guia de programação, aplicativos de área de trabalho
- Guia de programação, Windows Media Gerenciador de Dispositivos
- Guia de programação, plug-ins
- Guia de programação, criando aplicativos
- Windows Media Gerenciador de Dispositivos, aplicativos de área de trabalho
- Gerenciador de Dispositivos, aplicativos de área de trabalho
- Gerenciador de Dispositivos de mídia do Windows, plug-ins
- Gerenciador de Dispositivos, plug-Insp
- plug-ins, criando
- plug-ins, guia de programação
- aplicativos de desktop, criando
- Criando aplicativos de Gerenciador de Dispositivos de mídia do Windows, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b50a2dfce057b993f84c0aca4c8f45796f67ba8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781475"
---
# <a name="creating-a-windows-media-device-manager-application"></a>Criando um aplicativo de Gerenciador de Dispositivos de mídia do Windows

Esta seção descreve como usar o Windows Media Gerenciador de Dispositivos em seu aplicativo. O termo "aplicativo" aqui significa um executável, como um player de mídia ou um plug-in COM, como um plug-in de medição.

A Microsoft inclui vários provedores de serviços com o Windows XP e o Windows Media Player 10, incluindo um provedor de serviços do MTP, um provedor de serviços de Windows CE (para dispositivos que executam Windows CE e usando o protocolo RAPI, como o Pocket PC) e um provedor de serviços para dispositivos de categoria de armazenamento em massa (MSC). Você também pode criar seu próprio provedor de serviços para garantir a comunicação com seu próprio dispositivo; para obter mais informações, consulte [criando um provedor de serviços](creating-a-service-provider.md).

Há vários provedores de serviços herdados de terceiros que abordam um dispositivo específico do fabricante, não RAPI ou não-MSC. Esses provedores de serviços estão incluídos no disco do driver fornecido com esses dispositivos.

Um aplicativo que usa o Windows Media Gerenciador de Dispositivos deve executar as etapas a seguir.

1.  **Fique atento aos problemas de privacidade envolvidos no desenvolvimento de um aplicativo.** Consulte a [política de privacidade](privacy-statement.md) para saber mais sobre problemas de privacidade envolvendo o desenvolvimento de um aplicativo de Gerenciador de dispositivos de mídia do Windows.
2.  **Inclua a biblioteca e os arquivos de cabeçalho necessários para seu aplicativo.** Consulte [os arquivos de biblioteca e de cabeçalho necessários para um aplicativo](required-library-and-header-files-for-an-application.md) para saber quais arquivos você precisará incluir em seu projeto.
3.  **Autentique o aplicativo e adquira a interface IWMDMDevice raiz.** A primeira tarefa que um aplicativo deve fazer para usar o Windows Media Gerenciador de Dispositivos é autenticar a si mesmo. Esse processo verifica a identidade do aplicativo para o Windows Media Gerenciador de Dispositivos usando um certificado fictício para a funcionalidade limitada do Windows Media Gerenciador de Dispositivos ou usando um certificado oficial para a funcionalidade completa. Para obter mais informações, consulte [Autenticando o aplicativo](authenticating-the-application.md).
4.  **Enumere os dispositivos conectados.** A primeira etapa na comunicação com dispositivos é descobrir quais dispositivos estão conectados e acessíveis ao Windows Media Gerenciador de Dispositivos. Para obter mais informações, consulte [enumerando dispositivos](enumerating-devices.md).
5.  **Verifique o status dos componentes DRM do dispositivo.** Para usar arquivos protegidos por DRM, um dispositivo deve ser criado em alguma versão do Windows Media DRM para dispositivos portáteis e os componentes DRM devem estar atualizados. Antes de começar a lidar com arquivos no dispositivo, é melhor ver se o dispositivo dá suporte a arquivos protegidos por DRM e se o dispositivo precisa ser atualizado. Para obter mais informações, consulte [lidando com conteúdo protegido no aplicativo](handling-protected-content-in-the-application.md).
6.  **Explorar um dispositivo.** Depois de encontrar o dispositivo desejado, você pode explorar o conteúdo desse dispositivo. Para obter mais informações, consulte [explorando um dispositivo](exploring-a-device.md).
7.  **Ler arquivos do dispositivo e gravar arquivos no dispositivo.** Depois de saber sobre o layout do dispositivo, você pode começar a transferir arquivos de e para o dispositivo. Para obter mais informações, consulte [lendo arquivos do dispositivo](reading-files-from-the-device.md) e [gravando arquivos no dispositivo](writing-files-to-the-device.md).
8.  **Crie listas de reprodução no dispositivo.** Um tipo de arquivo que você pode gravar no dispositivo é um arquivo abstrato, que é uma coleção de referências a outros arquivos. Embora a capacidade de gravar arquivos abstratos em um dispositivo dependa do provedor de serviços e do dispositivo, geralmente somente os dispositivos MTP têm esse recurso. Para obter mais informações, consulte [criando uma lista de reprodução no dispositivo](creating-a-playlist-on-the-device.md).

Além dessas etapas, há vários outros recursos que você pode habilitar em seu aplicativo:

-   **Notificações.** Você pode habilitar seu aplicativo para receber notificações quando os dispositivos se conectarem ou desconectarem do computador. Para obter mais informações, consulte [habilitando notificações](enabling-notifications.md).
-   **Logout.** O Windows Media Gerenciador de Dispositivos usa um objeto de log que salva um registro de suas ações em um arquivo de texto local. Você pode adicionar mensagens a esse log para ajudá-lo a analisar erros ou desempenho em seu aplicativo. Para obter mais informações, consulte [habilitando o log](enabling-logging.md).
-   **Medição do uso de conteúdo.** Você pode recuperar estatísticas de uso de conteúdo para licenças que concedem esse direito. Essas estatísticas podem então ser enviadas para um servidor Web para calcular pagamentos de royalties para proprietários de conteúdo. Para obter mais informações, consulte [medição do uso de conteúdo](metering-content-usage.md).

**Uma observação de cuidado**

Seu aplicativo pode precisar trabalhar com uma variedade de dispositivos, incluindo alguns que você não desenvolveu e nunca testou seu código. Esses dispositivos podem ou não responder com precisão a consultas e comandos, ou implementar MTP ou outras especificações. Certifique-se de incluir a verificação de erros robusta e a funcionalidade de fallback para lidar com o inesperado. Programa de defesa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




