---
description: Usado com o método Store.Open para indicar como um armazenamento de certificados deve ser aberto.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: CAPICOM_STORE_OPEN_MODE enumeração (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ebd46b751f4a098361618f3b6e992e4333425f501bf6afdedfca047e921ad7ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772053"
---
# <a name="capicom_store_open_mode-enumeration"></a>Enumeração CAPICOM \_ STORE \_ OPEN \_ MODE

O tipo de enumeração CAPICOM STORE OPEN MODE é usado com o método Store.Open para indicar como um armazenamento \_ \_ de \_ certificados deve ser aberto. [](store-open.md)

## <a name="members"></a>Membros



| Membro                                      | DESCRIÇÃO                                                                                                                                                              | Valor |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ STORE SOMENTE LEITURA \_ \_ \_ ABERTA**        | Abra o armazenamento no modo somente leitura.<br/>                                                                                                                             | 0     |
| **CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**       | Abra o armazenamento no modo de leitura/gravação.<br/>                                                                                                                            | 1     |
| **CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED**  | Abra o armazenamento no modo de leitura/gravação se o usuário tiver permissões de leitura/gravação. Se o usuário não tiver permissões de leitura/gravação, abra o armazenamento no modo somente leitura.<br/> | 2     |
| **CAPICOM \_ STORE ABRIR SOMENTE \_ \_ EXISTENTE \_**    | Abrir somente lojas existentes; não crie um novo armazenamento. Introduzido pelo CAPICOM 2.0.<br/>                                                                              | 128   |
| **CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED** | Inclua certificados arquivados ao usar o armazenamento. Introduzido pelo CAPICOM 2.0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Comentários

Ao usar a enumeração CAPICOM \_ STORE \_ OPEN \_ MODE, apenas uma das configurações a seguir pode ser usada.

-   CAPICOM \_ STORE SOMENTE LEITURA \_ \_ \_ ABERTA
-   CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE
-   CAPICOM \_ STORE \_ OPEN \_ MAXIMUM \_ ALLOWED

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                |
| Cabeçalho<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store.Open**](store-open.md)
</dt> </dl>

 

 




