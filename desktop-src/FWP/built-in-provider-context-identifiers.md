---
title: Identificadores de contexto do provedor interno (Fwpmu. h)
description: Contextos de provedor interno identificam as políticas padrão a serem usadas com soquetes de segurança.
ms.assetid: 439a5abc-08ac-4514-a126-d738e5311003
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP
- FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942ed1d21d2acd46f0dc6b303049e0936e3cf63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454609"
---
# <a name="built-in-provider-context-identifiers"></a>Identificadores de contexto do provedor interno

Os identificadores para os contextos de provedor que são internos à WFP (Windows Filtering Platform) são representados por um GUID. Esses contextos de provedor internos identificam as políticas padrão a serem usadas com soquetes seguros.

Esses identificadores são definidos da seguinte maneira.

<dl> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_AUTHIP"></span><span id="fwpm_provider_context_secure_socket_authip"></span>**FWPM \_ de \_ \_ soquete seguro do contexto do \_ provedor \_**
</dt> <dd> <dl> <dt>



Política padrão de modo principal de AuthIP (protocolo Authenticated IP) para soquetes seguros.


</dt> </dl> </dd> <dt>

<span id="FWPM_PROVIDER_CONTEXT_SECURE_SOCKET_IPSEC"></span><span id="fwpm_provider_context_secure_socket_ipsec"></span>**contexto do provedor de FWPM \_ \_ \_ Secure \_ Socket \_ IPSec**
</dt> <dd> <dl> <dt>



Política padrão de modo rápido do IPsec (Internet Protocol Security) para soquetes seguros.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





