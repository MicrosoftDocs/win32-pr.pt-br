---
title: Media. durationstring
description: A propriedade durationstring recupera um valor de cadeia de caracteres que indica a duração do item de mídia atual no formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media. durationstring Windows Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763334"
---
# <a name="mediadurationstring"></a>Media. durationstring

A propriedade **durationstring** recupera um valor de **cadeia de caracteres** que indica a duração do item de mídia atual no formato hh: mm: SS.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **duraçãostring**

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Se essa propriedade for usada com um item de mídia diferente daquele especificado no *Player*. **currentMedia**, ele não pode conter um valor válido. Se o item de mídia for menor que uma hora, a parte HH: do valor de retorno será omitida.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **durationstring** para exibir a duração do item de mídia atual como texto formatado. Um elemento HTML DIV chamado MediaInfo exibe as informações de duração. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

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

[**Duração da mídia**](media-duration.md)
</dt> <dt>

[**Player. currentMedia**](player-currentmedia.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





