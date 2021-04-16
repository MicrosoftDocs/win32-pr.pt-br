---
description: Define os nomes de uso de chave estendidos com base em onde eles podem ser usados.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Enumeração de CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757479"
---
# <a name="capicom_eku-enumeration"></a>Enumeração EKU de CAPICOM \_

O tipo de enumeração **\_ EKU capicor** define os nomes de uso de chave estendidos com base em onde eles podem ser usados.

## <a name="members"></a>Membros



| Membro                                     | DESCRIÇÃO                                                                                                                                                 | Valor |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_outro EKU de CApicom \_**                    | O certificado tem usos definidos na política local. Isso será usado se o EKU necessário não for predefinido e o valor de OID precisar ser definido pelo aplicativo.<br/> | 0     |
| **\_autenticação de \_ servidor de EKU capicor \_**             | O certificado pode ser usado para autenticar um servidor.<br/>                                                                                                | 1     |
| **\_autenticação de \_ cliente de EKU capicor \_**             | O certificado pode ser usado para autenticar um cliente.<br/>                                                                                                | 2     |
| **\_assinatura de \_ código de EKU CAPICOM \_**            | O certificado pode ser usado para criar uma assinatura digital.<br/>                                                                                           | 3     |
| **\_proteção de \_ email de EKU CAPICOM \_**        | O certificado pode ser usado para proteção de email.<br/>                                                                                                    | 4     |
| **\_logon de \_ cartão inteligente \_ capicor EKU**         | O certificado pode ser usado para logon de cartão inteligente. Introduzido no CAPICOM 2,0.<br/>                                                                         | 5     |
| **\_sistema de \_ arquivos com criptografia EKU \_ de CAPICOM \_** | O certificado pode ser usado para o EFS. Introduzido no CAPICOM 2,0.<br/>                                                                                      | 6     |



## <a name="remarks"></a>Comentários

O tipo de enumeração **\_ EKU capicor** é usado pelo [**EKU. Propriedade Name**](eku-name.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




