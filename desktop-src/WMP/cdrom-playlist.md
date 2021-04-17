---
title: Cdrom. playlist
description: A propriedade playlist recupera um objeto playlist que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz do DVD.
ms.assetid: 71c76b6c-1344-4d45-b86b-7e49be44dba8
keywords:
- Cdrom. playlist Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.playlist
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb50daa169c6f6eb0690de376abd4433ffe130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105783624"
---
# <a name="cdromplaylist"></a>Cdrom. playlist

A propriedade **playlist** recupera um objeto **playlist** que representa as faixas no CD atualmente na unidade de CD ou as entradas de título no nível raiz do DVD.

``` syntax
player.cdromCollection.item(
        index
        ).playlist
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é um objeto de **lista de reprodução** somente leitura.

## <a name="remarks"></a>Comentários

Normalmente, os DVDs são organizados em títulos. Cada título contém um ou mais capítulos. Cada DVD é criado de forma diferente, portanto, como os títulos e capítulos são usados, cabe ao autor do conteúdo.

Para DVD, esse método recupera uma lista de reprodução que contém como o primeiro item um objeto de **mídia** que representa a mídia de DVD. A reprodução dos resultados do item no DVD será reproduzida desde o início se for a primeira reprodução após a inserção de um novo DVD ou a retomada da reprodução se o DVD for o mesmo que o último DVD exibido. Definir esse item como o atual durante os resultados da reprodução no DVD é reproduzido desde o início.

Itens adicionais (objetos de **mídia** ) na playlist são títulos de DVD que são representados por listas de reprodução aninhadas. Quando você especifica *controles*. **currentItem** para igual a um desses itens aninhados da lista de reprodução, o Windows Media Player define automaticamente a lista de reprodução aninhada como *Player*. **currentPlaylist** após a reprodução do capítulo começar. Você pode usar as propriedades, métodos e eventos do objeto **currentPlaylist** para trabalhar com capítulos de DVD, que também são itens de playlist.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa *cdrom*. **lista de reprodução** para preencher um elemento de texto HTML, chamado mytext, com os títulos do CD de áudio atualmente na primeira unidade de CD. Use *cdromCollection*. **contagem** para determinar o número de unidades de CD disponíveis. O objeto de **jogador** foi criado com ID = "Player".


```
// Store the CD playlist object.
var pl = Player.cdromCollection.Item(0).Playlist;

// Iterate through the CD track list.
for(var i = 0; i < pl.count; i++){

   // Print each CD track name.
   myText.value += pl.Item(i).name + "\n"; 
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Versão<br/>                  | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto cdrom**](cdrom-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





