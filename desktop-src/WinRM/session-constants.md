---
title: Constantes de sessão
description: As constantes de sessão na enumeração WSManSessionFlags especificam a autenticação e outras informações para as chamadas \_ \_ WSMan.CreateSession ou CreateSession IWSession que se conectam a um computador remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584eb15c4b235a006b52551de8f9999ddb65459412af68db81f0500a0828888b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743217"
---
# <a name="session-constants"></a>Constantes de sessão

As constantes de sessão na enumeração **\_ \_ WSManSessionFlags** especificam autenticação e outras informações para chamadas [**WSMan.CreateSession**](wsman-createsession.md) ou [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectam a um computador remoto. Essas constantes também estão intimamente relacionadas às opções de ferramenta de linha de comando do **Winrm.**

## <a name="using-session-constants"></a>Usando constantes de sessão

Você pode definir os sinalizadores de sessão para a chamada para [**WSMan.CreateSession**](wsman-createsession.md) de duas maneiras diferentes. Uma é mais curta e mais simples. A maneira mais longa, conforme é mostrado no exemplo a seguir, é localizar o valor do sinalizador que você deseja usar e criar uma constante em seu script com esse valor. Em seguida, a constante é usada para definir o valor do *parâmetro iFlags.*

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

A maneira recomendada, conforme mostrado no exemplo a seguir, é usar o método de objeto [**WSMan**](wsman.md) associado ao sinalizador .

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes de autenticação**](authentication-constants.md)
</dt> <dd>

Especifique o método de autenticação e como tratar servidores de certificado.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Outras constantes de sessão**](other-session-constants.md)
</dt> <dd>

Especifique a porta de codificação, criptografia e nome da entidade de serviço.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes e enumerações winRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[Autenticação para conexões remotas](authentication-for-remote-connections.md)
</dt> </dl>

 

 




