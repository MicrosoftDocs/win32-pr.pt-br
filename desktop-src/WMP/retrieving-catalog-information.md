---
title: Recuperando Informações do catálogo
description: Recuperando Informações do catálogo
ms.assetid: f2ec795f-6e6f-4c0c-9332-f1e96524221a
keywords:
- Windows Media Player lojas online, recuperando informações do catálogo
- lojas online, recuperando informações do catálogo
- Digite 1 lojas online, recuperando informações do catálogo
- Windows Media Player lojas online, informações de diagnóstico em catálogos
- lojas online, informações de diagnóstico em catálogos
- Digite 1 lojas online, informações de diagnóstico em catálogos
- Windows Media Player lojas online catcomp.exe
- lojas online, catcomp.exe
- Digite 1 lojas online, catcomp.exe
- catcomp.exe
- informações de diagnóstico em catálogos
- Recuperando Informações do catálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3b28da6d2d5f5143dab0664c10d0c906f971a6a60e4fdb502f4331fa71f408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570197"
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



 

 




