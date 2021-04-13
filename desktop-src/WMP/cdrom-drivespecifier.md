---
title: Cdrom. driveSpecifier
description: A propriedade driveSpecifier recupera a letra da unidade de CD ou DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Cdrom. driveSpecifier Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499289"
---
# <a name="cdromdrivespecifier"></a>Cdrom. driveSpecifier

A propriedade **driveSpecifier** recupera a letra da unidade de CD ou DVD.

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a>Valores possíveis

Esta propriedade é uma **cadeia de caracteres** somente leitura.

## <a name="remarks"></a>Comentários

Normalmente, as unidades de DVD podem reproduzir mídia de CD, mas as unidades de CD não podem reproduzir mídias em DVD. Essa propriedade recupera um especificador de unidade para um índice de unidade com base em zero dentro do intervalo recuperado usando *cdromCollection*. **contagem**. O valor recuperado assume a forma *X*:, em que *X* representa a letra da unidade.

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para essa propriedade.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *cdrom*. **driveSpecifier** para preencher uma área de texto HTML chamada MyText com uma lista separada por vírgulas de unidades de CD e DVD disponíveis. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| Versão<br/>                  | Windows Media Player versão 7,0 ou posterior<br/>                               |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto cdrom**](cdrom-object.md)
</dt> <dt>

[**CdromCollection. contagem**](cdromcollection-count.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





