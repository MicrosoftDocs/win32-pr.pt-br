---
title: Media.markerCount
description: A propriedade markerCount recupera o número de marcadores no item de mídia.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media.markerCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00206991f81c6a445648a063a37bcc45bf91f647b60317772478142eefd1b20e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123346"
---
# <a name="mediamarkercount"></a>Media.markerCount

A **propriedade markerCount** recupera o número de marcadores no item de mídia.

## <a name="syntax"></a>Syntax

*player*. *currentMedia*. **markerCount**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**) que especifica o número de marcadores no arquivo.

## <a name="remarks"></a>Comentários

Essa propriedade retornará zero se um arquivo não tiver marcadores ou se o item de mídia não for igual ao *Player*. **currentMedia**.

Os números de marcador começam em 1.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir usa *Mídia*. **markerCount** para recuperar o número de marcadores no item de mídia atual. Esse valor é usado como o limite superior para uma estrutura de looping, que itera pela lista de marcadores para recuperar cada nome de marcador. Um elemento HTML TEXTAREA chamado MNAMES exibe os nomes dos marcadores no item de mídia atual. O **objeto** Player foi criado com ID = "Player".


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Player.currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





