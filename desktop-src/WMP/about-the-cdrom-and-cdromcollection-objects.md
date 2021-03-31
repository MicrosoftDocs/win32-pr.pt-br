---
title: Sobre os objetos cdrom e cdromCollection
description: Sobre os objetos cdrom e cdromCollection
ms.assetid: b764806b-d9e1-4c36-b86b-24613501c926
keywords:
- Windows Media Player, objeto de cdrom
- Modelo de objeto do Windows Media Player, objeto cdrom
- modelo de objeto, objeto cdrom
- Controle ActiveX do Windows Media Player, objeto cdrom
- Controle ActiveX, objeto cdrom
- Controle ActiveX móvel do Windows Media Player, objeto cdrom
- Windows Media Player Mobile, objeto de cdrom
- Objeto cdrom
- Windows Media Player, o objeto cdromCollection
- Modelo de objeto do Windows Media Player, objeto cdromCollection
- modelo de objeto, objeto cdromCollection
- Controle ActiveX do Windows Media Player, objeto cdromCollection
- Controle ActiveX, objeto cdromCollection
- Controle ActiveX móvel do Windows Media Player, objeto cdromCollection
- Windows Media Player Mobile, o objeto cdromCollection
- Objeto cdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8fca9f7097f67226e31173670ca2935969704a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636202"
---
# <a name="about-the-cdrom-and-cdromcollection-objects"></a>Sobre os objetos cdrom e cdromCollection

Os objetos **cdrom** e **cdromCollection** regem a interface para as unidades de CD no seu computador para fins de leitura e reprodução de CDs.

O objeto **cdromCollection** é acessado somente por meio da propriedade **cdromCollection** do objeto **Player** . A propriedade **cdromCollection** retorna o objeto **cdromCollection** . Você só pode acessar as propriedades do objeto **cdromCollection** depois de criá-lo. Por exemplo, para usar a propriedade **Count** , você deve usar o seguinte código:


```C++
mycount = player.cdromcollection.count;
```



Você só pode acessar o objeto **cdrom** por meio do objeto **cdromCollection** . Por exemplo, para ejetar o CD usando o método **EJECT** , você deve primeiro criar o objeto de coleção e, em seguida, um item no objeto. Para ejetar o CD, use o seguinte código:


```C++
player.cdromcollection.item(0).eject();
```



Em ambos os casos, primeiro você está criando o objeto de coleção (**cdromCollection**) e, em seguida, obtendo um objeto específico dessa coleção. O objeto é o primeiro item da coleção, **Item**(0), que corresponde à primeira unidade de CD. Em seguida, você chama um método, **EJECT**, nesse item.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto cdrom**](cdrom-object.md)
</dt> <dt>

[**Objeto cdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




