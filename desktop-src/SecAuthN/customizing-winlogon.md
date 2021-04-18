---
description: Personalize o comportamento do Winlogon implementando um provedor de credenciais.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalizando o Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750506"
---
# <a name="customizing-winlogon"></a>Personalizando o Winlogon

Personalize o comportamento do [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando um provedor de credenciais. Para obter informações sobre provedores de credenciais, consulte [**interface ICredentialProvider**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).

**Windows Server 2003 e Windows XP:** Não há suporte para provedores de credenciais.

As seções a seguir descrevem maneiras de personalizar o Winlogon em versões do Windows anteriores ao Windows Vista.

> [!Note]  
> As DLLs GINAs e os pacotes de notificação Winlogon são ignorados no Windows Vista.

 

-   [Pacotes de notificação do Winlogon](#winlogon-notification-packages)
-   [Stubs GINA](#gina-stubs)
-   [Ganchos GINA](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Pacotes de notificação do Winlogon

Um pacote de notificação do Winlogon é uma DLL que exporta funções que manipulam eventos do Winlogon. Por exemplo, quando um usuário faz logon no sistema, o Winlogon chama cada pacote de notificação para fornecer informações sobre o evento. Para obter mais informações, consulte [pacotes de notificação do Winlogon](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>Stubs GINA

Um stub [*Gina*](/windows/desktop/SecGloss/g-gly) é uma DLL Gina personalizada que usa as implementações de função de exportação de uma DLL Gina instalada anteriormente (normalmente MsGina.dll). Um stub GINA Obtém ponteiros para cada função exportada pela DLL GINA instalada anteriormente. Cada função de stub da GINA usa o ponteiro de função apropriado para chamar a função correspondente na DLL GINA instalada anteriormente.

> [!IMPORTANT]
> Cada função de stub GINA deve chamar a função correspondente na GINA instalada anteriormente.

 

Uma função de stub GINA pode implementar funcionalidade adicional em uma ou mais de suas funções de exportação. Por exemplo, a função [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) de um stub Gina pode verificar a hora atual antes de chamar a função **WlxLoggedOutSAS** do MsGina.dll. Se a hora atual estiver dentro de um intervalo específico, a função de stub poderá exibir uma mensagem indicando que o logon não é permitido durante esse período de tempo e retornará a **\_ ação de SAS WLX \_ \_ None** para o Winlogon. A função **WlxLoggedOutSAS** da MsGina.dll seria então chamada somente durante o período de tempo permitido.

O aplicativo stub GINA Obtém uma tabela de expedição para funções de suporte do Winlogon por meio do parâmetro *pWinlogonFunctions* da função [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) . O aplicativo stub GINA pode usar essa tabela de expedição para chamar funções de suporte do Winlogon. Por exemplo, um aplicativo stub GINA pode chamar a função [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) para causar um evento de [*sequência de atenção segura*](/windows/desktop/SecGloss/s-gly) (SAS) quando um [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) é inserido em um [*leitor*](/windows/desktop/SecGloss/r-gly).

Para obter mais informações sobre como criar um stub GINA, consulte o exemplo stubs da Gina no \\ diretório Samples \\ Security \\ Gina \\ GinaStub de uma instalação do SDK (Software Development Kit) da plataforma.

> [!Note]  
> Todas as chamadas entre uma GINA e Winlogon devem estar dentro de um único thread.

 

## <a name="gina-hooks"></a>Ganchos GINA

Um gancho GINA é um stub GINA que, em sua implementação da função [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , substitui o ponteiro para a função de suporte [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) na tabela de expedição com um ponteiro para sua própria implementação da função **WlxDialogBoxParam** . Como resultado, cada vez que a GINA (normalmente MsGina.dll) instalada anteriormente chama a função **WlxDialogBoxParam** , a função implementada pelo gancho Gina é chamada.

A função [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementada pelo gancho Gina pode substituir o procedimento de retorno de chamada [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) que responde a um evento de caixa de diálogo específico.

Isso dá ao gancho GINA controle total sobre a aparência e o comportamento de todas as caixas de diálogo que MsGina.dll cria.

Para obter mais informações sobre como criar um gancho GINA, consulte o exemplo de ganchos Gina no \\ diretório Samples \\ Security \\ Gina \\ GinaHook de uma instalação do Platform SDK.

> [!Note]  
> Todas as chamadas entre uma GINA e Winlogon devem estar dentro de um único thread.

 

 

 
