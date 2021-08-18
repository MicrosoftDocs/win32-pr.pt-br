---
description: Personalize o comportamento do Winlogon implementando um Provedor de Credenciais.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalização do Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10b2ae1e029bb741a2402a25d8e51f331fdd1cac1e9918dfef3b35b36c8e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008654"
---
# <a name="customizing-winlogon"></a>Personalização do Winlogon

Personalize o comportamento do [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando um Provedor de Credenciais. Para obter informações sobre provedores de credenciais, consulte [**Interface ICredentialProvider**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).

**Windows Server 2003 e Windows XP:** Não há suporte para provedores de credenciais.

As seções a seguir descrevem maneiras de personalizar o Winlogon Windows versões anteriores ao Windows Vista.

> [!Note]  
> As DLLs e os pacotes de notificação winlogon DEÃO são ignorados no Windows Vista.

 

-   [Pacotes de notificação do Winlogon](#winlogon-notification-packages)
-   [Stubs DE STUBS DE STU](#gina-stubs)
-   [Ganchos DE GANCHO](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Pacotes de notificação do Winlogon

Um pacote de notificação do Winlogon é uma DLL que exporta funções que lidam com eventos do Winlogon. Por exemplo, quando um usuário faz logout no sistema, o Winlogon chama cada pacote de notificação para fornecer informações sobre o evento. Para obter mais informações, consulte [Pacotes de notificação do Winlogon](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>Stubs DE STUBS DE STU

Um [*stub DE STUB*](/windows/desktop/SecGloss/g-gly) é uma DLL CUSTOM QUE usa as implementações de função de exportação de uma DLL DOIS instalada anteriormente (normalmente MsGina.dll). Um stub DE STUB obtém ponteiros para cada função exportada pela DLL de LTD instalada anteriormente. Em seguida, cada função stub DEEI usa o ponteiro de função apropriado para chamar a função correspondente na DLL DE CALL instalada anteriormente.

> [!IMPORTANT]
> Cada função stub DE STU DEVE chamar a função correspondente no TAMBÉM instalado anteriormente.

 

Uma função stub DE STU PODE implementar funcionalidades adicionais em uma ou mais de suas funções de exportação. Por exemplo, a [**função WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) de um stub DE STUB PODE verificar a hora atual antes de chamar a função **WlxLoggedOutSAS** do MsGina.dll. Se a hora atual estivesse dentro de um intervalo específico, a função stub poderia exibir uma mensagem indicando que o logon não é permitido durante esse período e retornar **WLX \_ SAS \_ ACTION \_ NONE** para Winlogon. A **função WlxLoggedOutSAS** do MsGina.dll seria chamada somente durante o período de tempo permitido.

O aplicativo stub DE STU obtém uma tabela de expedição para funções de suporte do Winlogon por meio do parâmetro *pWinlogonFunctions* da [**função WlxInitialize.**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) O aplicativo stub DOIS pode usar essa tabela de expedição para chamar funções de suporte do Winlogon. Por exemplo, um aplicativo stub DERIA pode chamar [*a*](/windows/desktop/SecGloss/s-gly) função [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) para causar um evento SAS (sequência de atenção segura) quando um [*cartão*](/windows/desktop/SecGloss/s-gly) inteligente é inserido em um [*leitor*](/windows/desktop/SecGloss/r-gly).

Para obter mais informações sobre como criar um stub DE STUB, consulte o exemplo de Stubs de Stubs de Samples no diretório Samples Security LtdStub de uma instalação do \\ \\ \\ SDK (Kit de Desenvolvimento de \\ Software de Plataforma).

> [!Note]  
> Todas as chamadas entre um ÂMBITO e Winlogon devem estar dentro de um único thread.

 

## <a name="gina-hooks"></a>Ganchos DE GANCHO

Um gancho DEEI é um stub DEEI que, em sua implementação da função [**WlxInitialize,**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) substitui o ponteiro para a função de suporte [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) na tabela de expedição por um ponteiro para sua própria implementação da **função WlxDialogBoxParam.** Como resultado, cada vez que o TAMBÉM instalado anteriormente (normalmente MsGina.dll) chama a função **WlxDialogBoxParam,** a função implementada pelo gancho DEEI é chamada.

A [**função WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementada pelo gancho DELP pode substituir o procedimento de retorno de chamada [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) que responde a um evento de caixa de diálogo específico.

Isso dá ao gancho DEEI controle total sobre a aparência e o comportamento de todas as caixas de diálogo que MsGina.dll cria.

Para obter mais informações sobre como criar um gancho DENCI, consulte o exemplo de Ganchos DeMos no diretório Samples Security De Uma instalação do \\ \\ \\ \\ SDK da Plataforma.

> [!Note]  
> Todas as chamadas entre um ÂMBITO e Winlogon devem estar dentro de um único thread.

 

 

 
