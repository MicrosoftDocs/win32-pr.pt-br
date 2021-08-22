---
title: Método Media.isIdentical
description: O método isIdentical recupera um valor que indica se o objeto fornecido é o mesmo que o atual. | Método Media.isIdentical
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- Método isIdentical Windows Media Player
- método isIdentical Windows Media Player , classe media
- Classe de Windows Media Player de mídia , método isIdentical
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147d6ccc72d570709ef6ad898bf52872909dc5e3800d9cc671c774510b45d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054634"
---
# <a name="mediaisidentical-method"></a>Método Media.isIdentical

O **método isIdentical** recupera um valor que indica se o objeto fornecido é o mesmo que o atual.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mídia* \[ Em\]
</dt> <dd>

**Objeto de** mídia a ser comparado com o objeto **media** atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um **booliana.**

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Mídia*. **isIdentical para** verificar se um item de mídia chamado newMedia é o mesmo que o item de mídia atual. Se eles não são os mesmos, o novo item de mídia é interpretado. Caso contrário, a mídia atual continuará a reproduzir ininterruptamente. O **objeto** Player foi criado com ID = "Player".


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 





