---
title: Método Media. GetMarkerName
description: O método getmarcadorname recupera o nome do marcador no índice especificado.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- método GetMarkerName do Windows Media Player
- método getmarcadorname do Windows Media Player, classe de mídia
- Classe de mídia Windows Media Player, método getmarcadorname
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763842"
---
# <a name="mediagetmarkername-method"></a>Método Media. GetMarkerName

O método **Getmarcadorname** recupera o nome do marcador no índice especificado.

## <a name="syntax"></a>Sintaxe


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*markerNum* \[ no\]
</dt> <dd>

**Número** (**longo**) que especifica um índice de marcador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

Esse método retornará **NULL** se o marcador especificado não existir.

Alguns itens de mídia digital não contêm marcadores. Use **markerCount** para descobrir quantos marcadores estão no clipe atual.

Os números de índice de marcador começam em 1.

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **Getmarcadorname** para preencher um elemento de TextArea HTML chamado MNAMES com os nomes dos marcadores no item de mídia atual. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
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

[**Media. getmarcadortime**](media-getmarkertime.md)
</dt> <dt>

[**Media. markerCount**](media-markercount.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





