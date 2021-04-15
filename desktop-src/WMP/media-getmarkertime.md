---
title: Método Media. getmarcadortime
description: O método getmarcadortime recupera a hora do marcador no índice especificado.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- método getmarcadortime Windows Media Player
- método getmarcadortime Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getmarcadortime
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761192"
---
# <a name="mediagetmarkertime-method"></a>Método Media. getmarcadortime

O método **Getmarcadortime** recupera a hora do marcador no índice especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*markerNum* \[ no\]
</dt> <dd>

**Número** (**longo**) que especifica o índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **número** (**duplo**) especificando o local do marcador em segundos a partir do início do clipe.

## <a name="remarks"></a>Comentários

Esse método retornará **NULL** se o marcador especificado não existir.

Alguns itens de mídia digital não contêm marcadores. Use **markerCount** para descobrir quantos marcadores estão no clipe atual.

Os números de índice de marcador começam em 1.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **Getmarcadortime** para preencher um elemento de TextArea HTML chamado MTIMES com o local de cada marcador. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
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
</dt> <dt>

[**Media. getmarkname**](media-getmarkername.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





