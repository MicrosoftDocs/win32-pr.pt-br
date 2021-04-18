---
description: Define quais certificados em uma cadeia são salvos.
ms.assetid: 6f9e28e6-b01f-4803-8259-8ab73abeecf8
title: Enumeração de CAPICOM_CERTIFICATE_INCLUDE_OPTION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_INCLUDE_OPTION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 45ea9ccf7d3a43e325073f04e28bbd392fa34998
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771815"
---
# <a name="capicom_certificate_include_option-enumeration"></a>O certificado CAPICOM \_ \_ inclui a enumeração de \_ opção

O tipo de enumeração de **\_ \_ \_ opção do certificado CAPICOM** define quais certificados em uma cadeia são salvos. Esse tipo de enumeração foi introduzido no CAPICOM 2,0.

## <a name="members"></a>Membros



| Membro                                                 | DESCRIÇÃO                                                                           | Valor |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|-------|
| **CAPICOM de certificado de caissor \_ \_ \_ \_ , exceto \_ raiz** | Salva todos os certificados na cadeia com a exceção da entidade raiz.<br/> | 0     |
| **certificado CAPICOM \_ \_ incluir \_ \_ cadeia inteira**        | Salva a cadeia de certificados completa.<br/>                                      | 1     |
| **o certificado CAPICOM \_ \_ inclui \_ \_ somente entidade final \_**   | Salva apenas o certificado de entidade final.<br/>                                     | 2     |



## <a name="remarks"></a>Comentários

O tipo de enumeração de **\_ \_ \_ opção do certificado CAPICOM** é usado pelo método [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




