---
description: Indica o local de um armazenamento de certificados.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: CAPICOM_STORE_LOCATION enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 15aa93b70840e13901f88c40c715024ec33a835be14b7453da99aecae079b487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879006"
---
# <a name="capicom_store_location-enumeration"></a>Enumeração CAPICOM \_ STORE \_ LOCATION

O **tipo de enumeração CAPICOM \_ STORE \_ LOCATION** indica o local de um armazenamento [*de certificados.*](../secgloss/c-gly.md)

## <a name="members"></a>Membros



| Membro                                      | DESCRIÇÃO                                                                                                                                                                                                                                                                      | Valor |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **ARMAZENAMENTO DE MEMÓRIA CAPICOM \_ \_**                  | O armazenamento é um armazenamento de memória. As alterações no conteúdo do armazenamento não são persistentes.<br/>                                                                                                                                                                              | 0     |
| **ARMAZENAMENTO DE MÁQUINAS LOCAIS CAPICOM \_ \_ \_**          | O armazenamento é um armazenamento de máquinas local. Os armazenamentos de máquinas locais poderão ser armazenamentos de leitura/gravação somente se o usuário tiver permissões de leitura/gravação. Se o usuário tiver permissões de leitura/gravação e se o armazenamento for aberto para leitura/gravação, as alterações no conteúdo do armazenamento serão persistida.<br/> | 1     |
| **ARMAZENAMENTO DE USUÁRIO ATUAL DO CAPICOM \_ \_ \_**           | O armazenamento é um armazenamento de usuário atual. Um armazenamento de usuário atual pode ser um armazenamento de leitura/gravação. Se for, as alterações no conteúdo do armazenamento serão persistida.<br/>                                                                                                                      | 2     |
| **CAPICOM \_ ACTIVE \_ DIRECTORY \_ USER \_ STORE** | O armazenamento é um armazenamento do Active Directory. Os armazenamentos do Active Directory podem ser abertos somente no modo somente leitura. Os certificados não podem ser adicionados ou removidos dos armazenamentos do Active Directory.<br/>                                                                                        | 3     |
| **CAPICOM \_ SMART \_ CARD \_ USER \_ STORE**       | Os armazenamentos são suportados por armazenamentos de certificados baseados em cartão inteligente. A loja é o grupo de cartões inteligentes atuais. Introduzido no CAPICOM 2.0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Comentários

O **tipo de enumeração CAPICOM \_ STORE \_ LOCATION** é usado pelos seguintes métodos:

-   [**PrivateKey.Open**](privatekey-open.md)
-   [**Store.Open**](store-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
