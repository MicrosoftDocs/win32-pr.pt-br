---
description: Lista os tipos ACE definidos no momento.
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: ACE (Winnt.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa93490c4cf74ac33e3b15eeb888f011f81aa2b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470982"
---
# <a name="ace"></a>ACE

Uma **ACE** é uma [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) em uma ACL [*(lista de controle de*](/windows/desktop/SecGloss/a-gly) acesso).

A tabela a seguir lista os tipos **ACE** definidos no momento.




| Tipo ACE | Estrutura | Tipo de ACL | 
|----------|-----------|----------|
| <ul><li>Acesso permitido</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso permitido</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso permitido</li><li>Específico do objeto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso permitido</li><li>Específico do objeto</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso negado</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso negado</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso negado</li><li>Específico do objeto</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a> | Discricionário | 
| <ul><li>Acesso negado</li><li>Específico do objeto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a> | Discricionário | 
| <ul><li>Alarme do sistema</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a> | Sistema | 
| <ul><li>Alarme do sistema</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a> | Sistema | 
| <ul><li>Alarme do sistema</li><li>Específico do objeto</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Alarme do sistema</li><li>Específico do objeto</li></ul> | <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Auditoria do sistema</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a> | Sistema | 
| <ul><li>Auditoria do sistema</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a> | Sistema | 
| <ul><li>Auditoria do sistema</li><li>Específico do objeto</li><li>Permite o retorno de chamada durante a verificação de acesso</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a> | Sistema | 
| <ul><li>Auditoria do sistema</li><li>Específico do objeto</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a> | Sistema | 




 

Atualmente, não há suporte para ACEs de alarme do sistema e alarme do sistema específicas do objeto.

> [!Note]  
> Cada ACE começa com uma [**estrutura ACE \_ HEADER.**](/windows/desktop/api/Winnt/ns-winnt-ace_header) O formato dos dados após o header varia de acordo com o tipo ACE especificado no header.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Winnt.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**ACE \_ DE \_ ACESSO PERMITIDO**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**ACE \_ DE \_ ACESSO NEGADO**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**SYSTEM \_ ALARM \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**ACE \_ DE AUDITORIA DO \_ SISTEMA**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

