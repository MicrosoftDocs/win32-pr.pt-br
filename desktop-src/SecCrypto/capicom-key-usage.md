---
description: A enumeração uso da chave capicor \_ \_ define as maneiras em que uma chave pode ser usada. Introduzido no CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Enumeração de CAPICOM_KEY_USAGE (CAPICOM. h)
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
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748459"
---
# <a name="capicom_key_usage-enumeration"></a>Enumeração de uso de \_ chave CApicom \_

A **enumeração \_ \_ uso da chave capicor** define as maneiras em que uma chave pode ser usada. Introduzido no CAPICOM 2,0.

## <a name="members"></a>Membros



| Membro                                      | DESCRIÇÃO                                                                                                                      | Valor      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| **\_uso de \_ chave de assinatura digital \_ CAPICOM \_** | A chave pode ser usada para criar uma assinatura digital.<br/>                                                                    | 0x00000080 |
| **\_uso da \_ chave de não repúdio \_ CAPICOM \_**   | A chave pode ser usada para não- [*repúdio*](../secgloss/n-gly.md).<br/> | 0x00000040 |
| **\_uso da \_ chave de codificação de chave CAPICOM \_ \_**  | A chave pode ser usada para criptografar uma chave.<br/>                                                                                 | 0x00000020 |
| **\_uso da \_ chave de codificação de dados CAPICOM \_ \_** | A chave pode ser usada para criptografar dados.<br/>                                                                                  | 0x00000010 |
| **\_uso da \_ chave do contrato de chave CAPICOM \_ \_**     | A chave pode ser usada para o contrato de chave.<br/>                                                                                | 0x00000008 |
| **\_uso da \_ chave de assinatura de certificado de chave CAPICOM \_ \_ \_**    | A chave pode ser usada para a assinatura de certificado de chave. Esse valor é equivalente ao \_ \_ \_ uso da chave de assinatura offline \_ do \_ CAPICOM.<br/> | 0x00000004 |
| **\_ \_ \_ uso da chave de \_ assinatura \_ de capico offline CRL** | A chave pode ser usada para a assinatura de certificado de chave. Esse valor é equivalente ao uso de chave de certificado de chave de CAPICOM \_ \_ \_ \_ \_ .<br/>    | 0x00000002 |
| **\_uso da \_ chave de assinatura do \_ CAPICOM \_**          | A chave pode ser usada para assinatura.<br/>                                                                                      | 0x00000002 |
| **somente criptografia de capicos de \_ \_ \_ uso de chave \_**     | A chave só pode ser usada para criptografar.<br/>                                                                                  | 0x00000001 |
| **CAPICOM o \_ \_ \_ uso da chave somente de codificação \_**     | A chave só pode ser usada para descriptografar.<br/>                                                                                  | 0x00008000 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
