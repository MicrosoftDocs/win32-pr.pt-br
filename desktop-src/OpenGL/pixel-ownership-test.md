---
title: Teste de propriedade de pixel
description: O teste de propriedade de pixel determina se o contexto OpenGL atual possui o pixel no framebuffer correspondente a um fragmento específico.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Pipeline de processamento openGL, teste de propriedade de pixel
- Teste de propriedade de pixel OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12cfefe133b3951fa70d51736f664ec5a7cb9942c4c05f892115dd222013f294
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936245"
---
# <a name="pixel-ownership-test"></a>Teste de propriedade de pixel

O teste de propriedade de pixel determina se o contexto OpenGL atual possui o pixel no framebuffer correspondente a um fragmento específico. Se for o caso, o fragmento prosseguirá para o próximo teste. Caso não, o sistema de janelas determina se o fragmento é descartado ou se outras operações de fragmento serão executadas com esse fragmento. Com esse teste, o sistema de janela controla o comportamento quando, por exemplo, uma janela OpenGL é obscurecida.

 

 




