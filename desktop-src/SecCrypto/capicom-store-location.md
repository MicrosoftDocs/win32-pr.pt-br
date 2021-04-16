---
description: Indica o local de um repositório de certificados.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Enumeração de CAPICOM_STORE_LOCATION (CAPICOM. h)
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
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758280"
---
# <a name="capicom_store_location-enumeration"></a>Enumeração do local de \_ armazenamento CApicom \_

O tipo de enumeração do **\_ \_ local de armazenamento capicor** indica o local de um [*repositório de certificados*](../secgloss/c-gly.md).

## <a name="members"></a>Membros



| Membro                                      | DESCRIÇÃO                                                                                                                                                                                                                                                                      | Valor |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_armazenamento de memória CApicom \_**                  | O repositório é um repositório de memória. As alterações no conteúdo da loja não são persistentes.<br/>                                                                                                                                                                              | 0     |
| **CAPICOM do \_ \_ armazenamento do computador local \_**          | O repositório é um repositório do computador local. Os repositórios do computador local poderão ser armazenamentos de leitura/gravação somente se o usuário tiver permissões de leitura/gravação. Se o usuário tiver permissões de leitura/gravação e se o repositório for aberto como leitura/gravação, as alterações no conteúdo do repositório serão persistidas.<br/> | 1     |
| **\_armazenamento de \_ usuário \_ atual do CAPICOM**           | O repositório é um armazenamento de usuário atual. Um armazenamento de usuário atual pode ser um repositório de leitura/gravação. Se for, as alterações no conteúdo do repositório serão persistidas.<br/>                                                                                                                      | 2     |
| **armazenamento de usuários do CAPICOM \_ \_ do Active Directory \_ \_** | O repositório é um repositório Active Directory. Active Directory armazenamentos só podem ser abertos no modo somente leitura. Os certificados não podem ser adicionados ou removidos de repositórios Active Directory.<br/>                                                                                        | 3     |
| **\_armazenamento de \_ usuário do cartão inteligente \_ CAPICOM \_**       | Os repositórios dão suporte a repositórios de certificados baseados em cartão inteligente. O repositório é o grupo de cartões inteligentes presentes. Introduzido no CAPICOM 2,0.<br/>                                                                                                                                         | 4     |



## <a name="remarks"></a>Comentários

O tipo de enumeração do **\_ \_ local de armazenamento CAPICOM** é usado pelos seguintes métodos:

-   [**PrivateKey. Open**](privatekey-open.md)
-   [**Store. Open**](store-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
