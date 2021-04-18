---
title: Método external. Play
description: Observação Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online. O método play instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- método play Windows Media Player
- método de reprodução Windows Media Player, classe externa
- Classe externa Windows Media Player, método play
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
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783603"
---
# <a name="externalplay-method"></a>Método external. Play

> [!Note]  
> Este tópico descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

O método **Play** instrui o Windows Media Player a reproduzir um conjunto de itens de mídia.

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

## <a name="return-value"></a>Retornar valor

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

 

 





