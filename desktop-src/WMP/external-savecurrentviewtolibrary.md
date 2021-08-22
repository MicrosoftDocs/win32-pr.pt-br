---
title: Método external. saveCurrentViewToLibrary
description: O método saveCurrentViewToLibrary cria uma lista de reprodução a partir dos itens de mídia na exibição atual e salva a lista de reprodução na biblioteca local.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- Windows Media Player do método saveCurrentViewToLibrary
- método saveCurrentViewToLibrary Windows Media Player, classe externa
- classe externa Windows Media Player, método saveCurrentViewToLibrary
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
ms.openlocfilehash: cf14a6f712a72116860e7251edae73c91c4ef1dfb70876fd5f80dc329591673a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648436"
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

**Cadeia de caracteres** que especifica um nome amigável para a lista de reprodução. Windows Media Player exibe esse nome em sua interface do usuário.

</dd> <dt>

*Local* \[ no\]
</dt> <dd>

**Booliano** que especifica se a playlist é dinâmica ou estática. **True** especifica dinâmico e **false** especifica estático.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

 

 





