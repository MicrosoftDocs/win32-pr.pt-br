---
title: Teste de propriedade de pixel
description: O teste de propriedade de pixel determina se o contexto OpenGL atual possui o pixel no framebuffer correspondente a um fragmento específico.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline de processamento de OpenGL, teste de propriedade de pixel
- OpenGL de teste de propriedade de pixel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292337"
---
# <a name="pixel-ownership-test"></a>Teste de propriedade de pixel

O teste de propriedade de pixel determina se o contexto OpenGL atual possui o pixel no framebuffer correspondente a um fragmento específico. Nesse caso, o fragmento prossegue para o próximo teste. Caso contrário, o sistema de janelas determinará se o fragmento será descartado ou se outras operações de fragmento serão executadas com esse fragmento. Com esse teste, o sistema de janelas controla o comportamento quando, por exemplo, uma janela OpenGL é obscurecida.

 

 




