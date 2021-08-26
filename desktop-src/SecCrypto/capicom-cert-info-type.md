---
description: Define quais informações serão consultadas a partir de um certificado.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Enumeração de CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 480238556fce0470c51f00c394dd8566160686561342ec91da2e136c44a43cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879416"
---
# <a name="capicom_cert_info_type-enumeration"></a>\_Enumeração de \_ tipo de informações de certificado CAPICOM \_

O tipo de enumeração do **\_ tipo de \_ informações \_ do certificado capicor** define quais informações serão consultadas de um certificado.

## <a name="members"></a>Membros



| Membro                                         | DESCRIÇÃO                                                                                  | Valor |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **informações de certificado capicor \_ \_ \_ \_ nome simples da entidade \_** | Retorna o nome de exibição da entidade do certificado.<br/>                              | 0     |
| **\_ \_ \_ nome simples do emissor de informações de \_ certificado CAPICOM \_**  | Retorna o nome de exibição do emissor do certificado.<br/>                        | 1     |
| **CAPICOM \_ informações de certificado \_ nome de \_ email da entidade \_ \_**  | Retorna o endereço de email da entidade do certificado.<br/>                             | 2     |
| **capicor \_ informações do certificado \_ nome do \_ email do emissor \_ \_**   | Retorna o endereço de email do emissor do certificado.<br/>                       | 3     |
| **informações de certificado capicor \_ \_ \_ UPN da entidade \_**          | Retorna o UPN da entidade do certificado. Introduzido no CAPICOM 2,0.<br/>            | 4     |
| **\_UPN do \_ emissor de informações de certificado CAPICOM \_ \_**           | Retorna o UPN do emissor do certificado. Introduzido no CAPICOM 2,0.<br/>      | 5     |
| **CAPICOM \_ informações do certificado \_ \_ \_ nome DNS da entidade \_**    | Retorna o nome DNS da entidade do certificado. Introduzido no CAPICOM 2,0.<br/>       | 6     |
| **CAPICOM \_ informações do certificado \_ \_ \_ nome DNS do emissor \_**     | Retorna o nome DNS do emissor do certificado. Introduzido no CAPICOM 2,0.<br/> | 7     |



## <a name="remarks"></a>Comentários

O tipo de enumeração de **\_ tipo de \_ informações \_ do certificado capicor** é usado pelo método [**Certificate. GetInfo**](certificate-getinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




