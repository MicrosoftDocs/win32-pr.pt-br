---
description: Indica o que é verificado quando uma assinatura digital é verificada.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: CAPICOM_SIGNED_DATA_VERIFY_FLAG enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8f087a9a28d06e63bc19d75974bccba05da4c77658f81401fd994a7eadb9726a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772080"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a>Enumeração DO SINALIZADOR CAPICOM \_ \_ SIGNED DATA \_ VERIFY \_

A **enumeração CAPICOM \_ SIGNED DATA VERIFY \_ \_ \_ FLAG** indica o que é verificado quando uma assinatura [*digital*](../secgloss/d-gly.md) é verificada.

## <a name="members"></a>Membros



| Membro                                           | DESCRIÇÃO                                                                                                 | Valor |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ VERIFY \_ SIGNATURE \_ ONLY**             | Somente a assinatura está marcada.<br/>                                                                   | 0     |
| **CAPICOM \_ VERIFY \_ SIGNATURE \_ AND \_ CERTIFICATE** | A assinatura e a validade do certificado usado para criar a assinatura são verificadas.<br/> | 1     |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
