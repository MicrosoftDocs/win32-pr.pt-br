---
title: Método external. saveCurrentViewToLibrary
description: O método saveCurrentViewToLibrary cria uma lista de reprodução a partir dos itens de mídia na exibição atual e salva a lista de reprodução na biblioteca local.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- método saveCurrentViewToLibrary Windows Media Player
- método saveCurrentViewToLibrary Windows Media Player, classe externa
- Classe externa Windows Media Player, método saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762069"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>Método external. saveCurrentViewToLibrary

O método **saveCurrentViewToLibrary** cria uma lista de reprodução a partir dos itens de mídia na exibição atual e salva a lista de reprodução na biblioteca local.

## <a name="syntax"></a>Sintaxe


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FriendlyListName* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que especifica um nome amigável para a lista de reprodução. O Windows Media Player exibe esse nome na interface do usuário.

</dd> <dt>

*Local* \[ no\]
</dt> <dd>

**Booliano** que especifica se a playlist é dinâmica ou estática. **True** especifica dinâmico e **false** especifica estático.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





