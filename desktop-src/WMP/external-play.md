---
title: Método external. Play
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. o método play instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- Windows Media Player do método play
- método play Windows Media Player, classe externa
- classe externa Windows Media Player, método play
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90644b357e56f40bfbdb576908b99aa6941f8153dc339daa996152f63d77372c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648626"
---
# <a name="externalplay-method"></a>Método external. Play

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

o método **play** instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LibraryLocationType* \[ no\]
</dt> <dd>

Uma [constante de local de biblioteca](library-location-constants.md) que especifica o tipo dos itens de mídia a serem reproduzidos. Por exemplo, CPAlbumID especifica que um ou mais álbuns devem ser reproduzidos.

</dd> <dt>

*LibraryLocationIDs* \[ no\]
</dt> <dd>

**Cadeia de caracteres** que contém os identificadores, delimitados por ponto e vírgula, dos itens de mídia a serem reproduzidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto externo para repositórios online do tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





