---
description: O tipo de enumeração do certificado CAPICOM de \_ \_ localizar \_ tipo define o tipo de critério de pesquisa usado para localizar certificados específicos. Esse tipo de enumeração foi introduzido no CAPICOM 2,0.
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: Enumeração de CAPICOM_CERTIFICATE_FIND_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fb10b9289ae094f27fe29c3f2723d639eccc029aa7e5512833ac7e859c5c36ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772691"
---
# <a name="capicom_certificate_find_type-enumeration"></a>\_Enumeração de \_ tipo de localização de certificado capicor \_

O tipo de enumeração do **certificado CAPICOM de \_ \_ localizar \_ tipo** define o tipo de critério de pesquisa usado para localizar certificados específicos. Esse tipo de enumeração foi introduzido no CAPICOM 2,0.

## <a name="members"></a>Membros



| Membro                                                | DESCRIÇÃO                                                                                                                                 | Valor |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **Certificado capicor \_ \_ localizar \_ \_ hash SHA1**            | Retorna certificados que correspondem a um hash SHA1 especificado.<br/>                                                                             | 0     |
| **certificado CAPICOM \_ \_ localizar \_ nome da entidade \_**         | Retorna certificados cujo nome da entidade corresponde exatamente ou parcialmente com um nome de entidade especificado.<br/>                                   | 1     |
| **\_nome do \_ emissor da localização do certificado CAPICOM \_ \_**          | Retorna certificados cujo nome do emissor corresponde exatamente ou parcialmente a um nome de emissor especificado.<br/>                                     | 2     |
| **\_nome da \_ raiz de localização do certificado CAPICOM \_ \_**            | Retorna certificados cujo nome da entidade raiz corresponde exatamente ou parcialmente a um nome de entidade raiz especificado.<br/>                         | 3     |
| **\_nome do \_ modelo de localização do certificado CAPICOM \_ \_**        | Retorna certificados cujo nome de modelo corresponde a um nome de modelo especificado.<br/>                                                      | 4     |
| **\_extensão de \_ localização de certificado CAPICOM \_**             | Retorna certificados que têm uma extensão que corresponde a uma extensão especificada.<br/>                                                  | 5     |
| **certificado capicor \_ \_ localizar \_ propriedade estendida \_**    | Retorna certificados que têm uma propriedade estendida cujo identificador de propriedade corresponde a um identificador de propriedade especificado.<br/>           | 6     |
| **certificado CAPICOM ao \_ \_ localizar \_ política de aplicativo \_**   | Retorna certificados no repositório que têm uma extensão ou propriedade de uso avançado de chave combinada com um identificador de uso.<br/> | 7     |
| **\_política de \_ certificado de localização de certificado CAPICOM \_ \_**   | Retorna certificados que contêm um OID de política especificado.<br/>                                                                          | 8     |
| **tempo de localização de certificado capicor \_ \_ \_ \_ válido**           | Retorna certificados cujo tempo é válido.<br/>                                                                                        | 9     |
| **tempo de localização de certificado capico \_ \_ \_ \_ \_ ainda não \_ válido** | Retorna certificados cujo tempo ainda não é válido.<br/>                                                                                | 10    |
| **tempo limite de localização do certificado CAPICOM \_ \_ \_ \_ expirado**         | Retorna certificados cujo tempo expirou.<br/>                                                                                     | 11    |
| **\_uso da \_ chave de localização de certificado CAPICOM \_ \_**            | Retorna certificados que contêm uma chave que pode ser usada na maneira especificada.<br/>                                                  | 12    |



## <a name="remarks"></a>Comentários

O tipo de enumeração de **\_ tipo de \_ localização \_ do certificado capicor** é usado pelo método [**Certificates. Find**](certificates-find.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




