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
ms.openlocfilehash: c0247b58b38de55eb67479c68e0c0955fb9d2a56a793215330366ca8ccfbe4e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951325"
---
# <a name="built-in-provider-context-identifiers"></a>Identificadores de contexto do provedor interno

os identificadores para os contextos do provedor que são internos para a Windows a plataforma de filtragem (WFP) são representados por um GUID. Esses contextos de provedor internos identificam as políticas padrão a serem usadas com soquetes seguros.

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





