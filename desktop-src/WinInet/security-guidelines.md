---
title: Diretriz de segurança
description: É importante manter o usuário informado sobre possíveis problemas de segurança.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084778"
---
# <a name="security-guideline"></a>Diretriz de segurança

É importante manter o usuário informado sobre possíveis problemas de segurança.

## <a name="notify-the-user-of-security-related-events"></a>Notificar o usuário sobre eventos de Security-Related

Sempre notifique o usuário sobre qualquer alteração na segurança, seja um erro relacionado à segurança, como uma falha de certificado, ou uma alteração na segurança do protocolo subjacente, como alterar de um site HTTPS para um site HTTP.

## <a name="notify-the-user-of-security-related-errors"></a>Notificar o usuário sobre erros de Security-Related

Quando seu aplicativo recebe uma mensagem de erro que pode indicar um problema de segurança, a função **InternetErrorDlg** fornece uma interface padrão e familiar para notificar o usuário na maioria dos casos.

Entre os erros que se enquadram nessa categoria estão:

**ERRO \_ \_ de http \_ da Internet para \_ https \_ no \_ REDIR**

**ERRO \_ de \_ AC inválida \_ da Internet**

**ERRO \_ a \_ postagem na Internet \_ \_ não é \_ segura**

**\_erros de certificados da Internet \_ SEC \_ \_**

**ERRO \_ CN do certificado da Internet \_ SEC \_ \_ \_ inválido**

**ERRO de data de CERT. de \_ Internet \_ \_ \_ \_ inválida**

Uma falha ao notificar o usuário sobre erros como esses podem expor o usuário a vários tipos de violações de segurança, incluindo ataques de falsificação ou divulgação involuntária de informações.

## <a name="notify-the-user-when-connection-security-changes"></a>Notificar o usuário quando a segurança da conexão for alterada

Sempre notifique o usuário quando a segurança da conexão for alterada, por exemplo, de HTTPS para HTTP. Caso contrário, a menos que o usuário tenha optado explicitamente por não ser notificado sobre tais alterações, você está ocultando os riscos da divulgação involuntária de informações.

Entre as funções que relatam tal alteração na segurança da conexão estão a função de retorno de chamada **InternetStatusCallback** e a função **InternetConfirmZoneCrossing** .

> [!Note]  
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 