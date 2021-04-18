---
title: Constantes de sessão
description: As constantes de sessão na \_ \_ Enumeração WSManSessionFlags especificam a autenticação e outras informações para chamadas de WSMan. CreateSession ou IWSMan CreateSession que se conectam a um computador remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793826"
---
# <a name="session-constants"></a>Constantes de sessão

As constantes de sessão na enumeração **\_ \_ WSManSessionFlags** especificam a autenticação e outras informações para as chamadas [**WSMan. CreateSession**](wsman-createsession.md) ou [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectam a um computador remoto. Essas constantes também estão fortemente relacionadas aos comutadores da ferramenta de linha de comando do **WinRM** .

## <a name="using-session-constants"></a>Usando constantes de sessão

Você pode definir os sinalizadores de sessão para a chamada para [**WSMan. CreateSession**](wsman-createsession.md) de duas maneiras diferentes. Uma é mais curta e mais simples. A maneira mais longa, como é mostrado no exemplo a seguir, é localizar o valor do sinalizador que você deseja usar e criar uma constante em seu script com esse valor. Em seguida, a constante é usada para definir o valor do parâmetro *iFlags* .

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

A maneira recomendada, conforme mostrado no exemplo a seguir, é usar o método de objeto [**WSMan**](wsman.md) associado ao sinalizador.

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes de autenticação**](authentication-constants.md)
</dt> <dd>

Especifique o método de autenticação e como lidar com servidores de certificado.

</dd> <dt>

<span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Outras constantes de sessão**](other-session-constants.md)
</dt> <dd>

Especifique a codificação, a criptografia e a porta do nome da entidade de serviço.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes e enumerações do WinRM](winrm-constants-and-enumerations.md)
</dt> <dt>

[**WSMan. CreateSession**](wsman-createsession.md)
</dt> <dt>

[Autenticação para conexões remotas](authentication-for-remote-connections.md)
</dt> </dl>

 

 




