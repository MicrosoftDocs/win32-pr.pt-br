---
title: Método Media. getmarcadortime
description: O método getmarcadortime recupera a hora do marcador no índice especificado.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- método GetMarkerTime Windows Media Player
- método getmarkertime Windows Media Player, classe de mídia
- classe de mídia Windows Media Player, método getmarcadortime
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
ms.openlocfilehash: 0f90d1382302e4a053a6dee4dac911d2cc0c0aa67066469c8143f6f38b3bd889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508406"
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

## <a name="return-value"></a>Valor retornado

Esse método retorna um **número** (**duplo**) especificando o local do marcador em segundos a partir do início do clipe.

## <a name="remarks"></a>Comentários

Esse método retornará **NULL** se o marcador especificado não existir.

Alguns itens de mídia digital não contêm marcadores. Use **markerCount** para descobrir quantos marcadores estão no clipe atual.

Os números de índice de marcador começam em 1.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *mídia*. **Getmarcadortime** para preencher um elemento de TextArea HTML chamado MTIMES com o local de cada marcador. O objeto de **jogador** foi criado com ID = "Player".


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

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





