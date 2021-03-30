---
title: Recuperando Informações do catálogo
description: Recuperando Informações do catálogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Lojas online do Windows Media Player, recuperando informações do catálogo
- lojas online, recuperando informações do catálogo
- Digite 1 lojas online, recuperando informações do catálogo
- Armazenamentos online do Windows Media Player, informações de diagnóstico em catálogos
- lojas online, informações de diagnóstico em catálogos
- Digite 1 lojas online, informações de diagnóstico em catálogos
- Armazenamentos online do Windows Media Player, catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- catcomp.exe
- informações de diagnóstico em catálogos
- Recuperando Informações do catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721d6ba3e4d6b5106cf44446d4c96ed842ccd61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636644"
---
# <a name="retrieving-catalog-information"></a>Recuperando Informações do catálogo

Você pode exibir informações de diagnóstico em um catálogo executando catcomp com a seguinte sintaxe:


```C++
catcomp info <catalogpath> [track|artist|album] [ID]
```



Por exemplo, o comando a seguir exibe informações sobre um catálogo inteiro, incluindo a versão, a localidade e as informações internas em itens de catálogo:


```C++
catcomp info C:\Catalog210\catalog.wmdb
```



A seguir são exibidas informações para o roteiro com a ID 3256:


```C++
catcomp info C:\Catalog210\catalog.wmdb track 3256
```



 

 




