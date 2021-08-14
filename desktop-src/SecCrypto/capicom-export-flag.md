---
description: O tipo de \_ enumeração CAPICOM EXPORT \_ FLAG define se os erros de exportação de chave privada são ignorados.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: CAPICOM_EXPORT_FLAG enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d6be9953640eeb2eb1d6c7fad812f5efe2d2da2f6888a01b4450c638ab68bfca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772461"
---
# <a name="capicom_export_flag-enumeration"></a>Enumeração CAPICOM \_ EXPORT \_ FLAG

O **tipo de enumeração \_ CAPICOM EXPORT \_ FLAG** define se os erros de exportação de chave privada são ignorados.

## <a name="members"></a>Membros



| Membro                                                            | DESCRIÇÃO                                               | Valor |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| **CAPICOM \_ EXPORT \_ DEFAULT**                                      | Os erros de exportação de chave privada não são ignorados.<br/> | 0     |
| **CAPICOM \_ EXPORT \_ IGNORE \_ PRIVATE \_ KEY \_ NOT \_ EXPORTABLE \_ ERROR** | Todos os erros de exportação de chave privada são ignorados.<br/>     | 1     |



## <a name="remarks"></a>Comentários

O tipo de \_ enumeração CAPICOM EXPORT \_ FLAG é usado pelo seguinte método:

-   [**Certificates.Save**](certificates-save.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




