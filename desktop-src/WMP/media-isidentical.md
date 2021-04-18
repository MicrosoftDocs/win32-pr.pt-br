---
title: Método Media. isidêntico
description: O método isidêntico recupera um valor que indica se o objeto fornecido é o mesmo que o atual. | Método Media. isidêntico
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- método isidêntico do Windows Media Player
- método isidêntico Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método isidêntico
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
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810682"
---
# <a name="mediaisidentical-method"></a>Método Media. isidêntico

O método **isidêntico** recupera um valor que indica se o objeto fornecido é o mesmo que o atual.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mídia* \[ no\]
</dt> <dd>

Objeto de **mídia** a ser comparado com o objeto de **mídia** atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **valor booleano**.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **isidêntico** para verificar se um item de mídia chamado newMedia é o mesmo que o item de mídia atual. Se eles não forem iguais, o novo item de mídia será reproduzido. Caso contrário, a mídia atual continuará a ser executada sem interrupção. O objeto de **jogador** foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> </dl>

 

 





