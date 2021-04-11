---
title: Sobre os objetos Error e ErrorItem
description: Sobre os objetos Error e ErrorItem
ms.assetid: 187f6835-3101-45db-87bd-930d222165ce
keywords:
- Windows Media Player, objeto de erro
- Modelo de objeto do Windows Media Player, objeto de erro
- modelo de objeto, objeto de erro
- Controle ActiveX do Windows Media Player, objeto de erro
- Controle ActiveX, objeto de erro
- Controle ActiveX móvel do Windows Media Player, objeto de erro
- Windows Media Player Mobile, objeto de erro
- Objeto de erro
- Windows Media Player, objeto ErrorItem
- Modelo de objeto do Windows Media Player, objeto ErrorItem
- modelo de objeto, objeto ErrorItem
- Controle ActiveX do Windows Media Player, objeto ErrorItem
- Controle ActiveX, objeto ErrorItem
- Controle ActiveX móvel do Windows Media Player, objeto ErrorItem
- Windows Media Player Mobile, objeto ErrorItem
- Objeto ErrorItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23064670f13229aca84ae6dc86cf27cf34abbc56
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292299"
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

 

 




