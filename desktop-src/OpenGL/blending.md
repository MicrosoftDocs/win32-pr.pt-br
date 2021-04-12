---
title: Mesclagem
description: A mesclagem combina os valores R, G, B e A dos fragmentos com aqueles armazenados no framebuffer no local correspondente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline de processamento OpenGL, mesclagem
- combinação de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292174"
---
# <a name="blending"></a>Mesclagem

A mesclagem combina os valores R, G, B e A dos fragmentos com aqueles armazenados no framebuffer no local correspondente. A mesclagem, que é executada somente no modo RGBA, depende do valor alfa do fragmento e do pixel armazenado atualmente correspondente; Ele também pode depender dos valores RGB. Você controla a mesclagem com o [**glBlendFunc**](glblendfunc.md), com o qual você indica os fatores de mesclagem de origem e destino.

 

 




