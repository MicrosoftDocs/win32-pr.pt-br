---
description: Especifica permissões de controle de acesso para um diretório em um cartão inteligente.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: Enumeração de CARD_DIRECTORY_ACCESS_CONDITION (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 8038179c7337edaff0138fc46c34191f99821250808c4ace16dc76cdfafd3b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878956"
---
# <a name="card_directory_access_condition-enumeration"></a>\_Enumeração de \_ condição de acesso ao diretório de cartão \_

A **enumeração \_ \_ \_ condição de acesso ao diretório de cartão** especifica permissões de controle de acesso para um diretório em um [*cartão inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**
</dt> <dd>

Esse valor não é válido.

</dd> <dt>

<span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**
</dt> <dd>

Usuários específicos podem ler, gravar e excluir o diretório.

</dd> <dt>

<span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**
</dt> <dd>

Os administradores podem ler, gravar e excluir o diretório.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows xp, \[ somente aplicativos da área de trabalho do Windows xp\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows servidor 2003, Windows server 2003 \[ somente aplicativos da área de trabalho\]<br/>            |
| Cabeçalho<br/>                   | <dl> <dt>Cardmod. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de criptografia de cartão inteligente base da Microsoft](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[**CardCreateDirectory**](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[**CardDeleteDirectory**](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
