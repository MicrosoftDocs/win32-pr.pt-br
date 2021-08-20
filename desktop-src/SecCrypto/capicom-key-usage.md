---
description: A enumeração CAPICOM \_ KEY USAGE define as maneiras pelas quais uma chave pode ser \_ usada. Introduzido no CAPICOM 2.0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: CAPICOM_KEY_USAGE enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bb477ee12b33c3d32fd2c48a56831dc2f56244b1e8a564cd2d0482e6e4a5d5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772421"
---
# <a name="capicom_key_usage-enumeration"></a>Enumeração CAPICOM \_ KEY \_ USAGE

A **enumeração CAPICOM \_ KEY \_ USAGE** define as maneiras pelas quais uma chave pode ser usada. Introduzido no CAPICOM 2.0.

## <a name="members"></a>Membros



| Membro                                      | DESCRIÇÃO                                                                                                                      | Valor      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **USO DA CHAVE DE ASSINATURA DIGITAL CAPICOM \_ \_ \_ \_** | A chave pode ser usada para criar uma assinatura digital.<br/>                                                                    | 0x00000080 |
| **USO DE CHAVE DE \_ \_ NÃO \_ REPÚDIO \_ CAPICOM**   | A chave pode ser usada [*para não repúdio.*](../secgloss/n-gly.md)<br/> | 0x00000040 |
| **CAPICOM \_ KEY \_ ENCIPHERMENT \_ KEY \_ USAGE**  | A chave pode ser usada para criptografar uma chave.<br/>                                                                                 | 0x00000020 |
| **USO DA CHAVE CAPICOM \_ DATA \_ ENCIPHERMENT \_ \_** | A chave pode ser usada para criptografar dados.<br/>                                                                                  | 0x00000010 |
| **USO DE CHAVE DO \_ CONTRATO DE \_ CHAVE \_ CAPICOM \_**     | A chave pode ser usada para o contrato de chave.<br/>                                                                                | 0x00000008 |
| **USO DA CHAVE DE \_ \_ SINALIZAÇÃO DE CERTIFICADO \_ \_ CAPICOM \_**    | A chave pode ser usada para assinatura de certificado de chave. Esse valor é equivalente ao USO DA CHAVE DE SINAL \_ DE \_ CRL OFFLINE CAPICOM. \_ \_ \_<br/> | 0x00000004 |
| **USO DA CHAVE DE \_ \_ SINALIZAÇÃO DE CRL OFFLINE \_ \_ DO CAPICOM \_** | A chave pode ser usada para assinatura de certificado de chave. Esse valor é equivalente a CAPICOM \_ KEY CERT SIGN KEY KEY SIGN KEY \_ \_ \_ \_ USAGE.<br/>    | 0x00000002 |
| **USO DA CHAVE DE \_ SINALIZAÇÃO DA CRL DO CAPICOM \_ \_ \_**          | A chave pode ser usada para assinatura.<br/>                                                                                      | 0x00000002 |
| **USO DE CHAVE SOMENTE CAPICOM \_ ENCIPHER \_ \_ \_**     | A chave só pode ser usada para criptografar.<br/>                                                                                  | 0x00000001 |
| **CAPICOM \_ DESCOMPACTAR \_ APENAS O USO DE \_ \_ CHAVE**     | A chave só pode ser usada para descriptografar.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
