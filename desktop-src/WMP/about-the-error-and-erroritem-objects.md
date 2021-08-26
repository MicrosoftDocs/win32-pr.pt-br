---
title: Sobre os objetos Error e ErrorItem
description: Sobre os objetos Error e ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, objeto de erro
- modelo de objeto Windows Media Player, objeto de erro
- modelo de objeto, objeto de erro
- controle de ActiveX de Windows Media Player, objeto de erro
- controle de ActiveX, objeto de erro
- Windows Media Player controle de ActiveX móvel, objeto de erro
- Windows Media Player Celular, objeto de erro
- Objeto de erro
- Windows Media Player, objeto ErrorItem
- modelo de objeto Windows Media Player, objeto ErrorItem
- modelo de objeto, objeto ErrorItem
- Windows Media Player ActiveX controle, objeto ErrorItem
- controle de ActiveX, objeto ErrorItem
- Windows Media Player controle de ActiveX móvel, objeto ErrorItem
- Windows Media Player Mobile, objeto ErrorItem
- Objeto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84dcd8e0961007c185640b32ac53d249d2e739ca5e1aa4247a6735e09b2a3242
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004396"
---
# <a name="about-the-error-and-erroritem-objects"></a>Sobre os objetos Error e ErrorItem

Os objetos **Error** e **ErrorItem** regem os recursos de tratamento de erros do Windows Media Player. O objeto de **erro** é obtido do objeto **Player** por meio da propriedade **Error** . Você pode obter um código específico do objeto de **erro** usando a propriedade **Item** do objeto **Error** para criar o objeto **ErrorItem** . Por exemplo, para obter o código de erro do primeiro item de erro, digite:


```C++
myerrorcode = player.error.item(0).errorCode;

```



Você também pode invocar a ajuda da Web com o objeto de **erro** usando o seguinte código:


```C++
player.error.webHelp();

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Objeto Error**](error-object.md)
</dt> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> <dt>

[**Modelo de objeto do Player para linguagens de script**](player-object-model-for-scripting-languages.md)
</dt> </dl>

 

 




