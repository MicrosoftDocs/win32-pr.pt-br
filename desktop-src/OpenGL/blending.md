---
title: Mistura
description: A combinação combina os valores R, G, B e A de um fragmento com aqueles armazenados no framebuffer no local correspondente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline de processamento openGL, mesclagem
- mesclando OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5b38786d2320a646bd6cac096e535e4e1441df98522ac86a146836b929c0986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361430"
---
# <a name="blending"></a>Mistura

A combinação combina os valores R, G, B e A de um fragmento com aqueles armazenados no framebuffer no local correspondente. A combinação, que é executada somente no modo RGBA, depende do valor alfa do fragmento e do pixel armazenado no momento correspondente; ele também pode depender dos valores RGB. Você controla a combinação com [**glBlendFunc,**](glblendfunc.md)com o qual indica os fatores de combinação de origem e destino.

 

 




