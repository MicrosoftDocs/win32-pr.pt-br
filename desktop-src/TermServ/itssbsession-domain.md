---
title: Propriedade de domínio ITsSbSession
description: Recupera o nome de domínio do usuário.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface ITsSbSession
- Serviços de Área de Trabalho Remota de interface ITsSbSession, propriedade de domínio
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52854f719830933c96bc130dbec4f0b15f1264344396382ad59099d4c37cf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128301"
---
# <a name="itssbsessiondomain-property"></a>ITsSbSession: Propriedade omain de:D

Recupera o nome de domínio do usuário.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma variável **BSTR** que recebe o nome de domínio do usuário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





