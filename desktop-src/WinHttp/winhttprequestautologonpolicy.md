---
description: Inclui configurações possíveis para a política de logon automático.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Enumeração WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782576"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>Enumeração WinHttpRequestAutoLogonPolicy

A enumeração **WinHttpRequestAutoLogonPolicy** inclui possíveis configurações para a [política de logon automática](authentication-in-winhttp.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ sempre**
</dt> <dd>

Um logon autenticado, usando as credenciais padrão, é executado para todas as solicitações.

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**
</dt> <dd>

Um logon autenticado, usando as credenciais padrão, é executado somente para solicitações na intranet local. A intranet local é considerada como qualquer servidor na lista de bypass de proxy na configuração de proxy atual.

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ nunca**
</dt> <dd>

A autenticação não é usada automaticamente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para definir a política de logon automático, chame o método [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) e especifique uma das constantes anteriores.

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




