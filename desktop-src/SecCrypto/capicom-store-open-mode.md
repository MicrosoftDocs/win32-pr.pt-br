---
description: Usado com o método Store. Open para indicar como um repositório de certificados deve ser aberto.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Enumeração de CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
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
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752743"
---
# <a name="capicom_store_open_mode-enumeration"></a>\_Enumeração do \_ modo de abertura do armazenamento CAPICOM \_

O tipo de enumeração do modo de armazenamento CAPICOM \_ \_ \_ é usado com o método [**Store. Open**](store-open.md) para indicar como um repositório de certificados deve ser aberto.

## <a name="members"></a>Membros



| Membro                                      | DESCRIÇÃO                                                                                                                                                              | Valor |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM de \_ leitura do armazenamento \_ \_ \_**        | Abra o repositório no modo somente leitura.<br/>                                                                                                                             | 0     |
| **o CAPICOM de \_ \_ leitura e \_ \_ gravação aberta**       | Abra o repositório no modo de leitura/gravação.<br/>                                                                                                                            | 1     |
| **\_ \_ \_ máximo permitido de armazenamento \_ de CAPICOM**  | Abra o repositório no modo de leitura/gravação se o usuário tiver permissões de leitura/gravação. Se o usuário não tiver permissões de leitura/gravação, abra o repositório no modo somente leitura.<br/> | 2     |
| **CAPICOM \_ Store \_ abrir \_ \_ somente existente**    | Abrir somente repositórios existentes; Não crie um novo repositório. Introduzido por CAPICOM 2,0.<br/>                                                                              | 128   |
| **o CAPICOM de \_ Store \_ aberto \_ incluem \_ arquivados** | Inclua certificados arquivados ao usar o repositório. Introduzido por CAPICOM 2,0.<br/>                                                                                | 256   |



## <a name="remarks"></a>Comentários

Ao usar a enumeração do modo de abertura do armazenamento CAPICOM \_ \_ \_ , somente uma das seguintes configurações pode ser usada.

-   CAPICOM de \_ leitura do armazenamento \_ \_ \_
-   o CAPICOM de \_ \_ leitura e \_ \_ gravação aberta
-   \_ \_ \_ máximo permitido de armazenamento \_ de CAPICOM

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> </dl>

 

 




