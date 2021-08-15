---
title: Constantes e enumerações winRM
description: Windows O Gerenciamento Remoto tem sinalizadores de bits usados na criação de sessões e enumerações e para tipos de acesso e autenticação em um servidor proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742932"
---
# <a name="winrm-constants-and-enumerations"></a>Constantes e enumerações winRM

Windows O Gerenciamento Remoto tem sinalizadores de bits usados na criação de sessões e enumerações e para tipos de acesso e autenticação em um servidor proxy. A lista a seguir lista os diferentes sinalizadores de bits.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Constantes de sessão](session-constants.md)
</dt> <dd>

Sinalizadores usados no parâmetro *flags* dos métodos [**WSMan.CreateSession**](wsman-createsession.md) ou [**IWSMan::CreateSession.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Constantes de enumeração**](enumeration-constants.md)
</dt> <dd>

Sinalizadores usados no *parâmetro flags* da chamada para [**Session.Enumerate**](session-enumerate.md) ou [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Sinalizadores usados no *parâmetro authenticationMechanism* da chamada para [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Sinalizadores usados no *parâmetro accessType* da chamada para [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




