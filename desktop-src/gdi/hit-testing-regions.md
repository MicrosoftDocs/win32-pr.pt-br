---
description: Um aplicativo executa testes de acerto em regiões para determinar as coordenadas da posição atual do cursor.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Regiões de teste de acerto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5734ffb886bd2978d3ee0b49773d752d4abf43a4d98dc060f3dfaf2956e3084a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118760972"
---
# <a name="hit-testing-regions"></a>Regiões de teste de acerto

Um aplicativo executa testes de acerto em regiões para determinar as coordenadas da posição atual do cursor. Em seguida, ele passa essas coordenadas, bem como um identificador que identifica a região para a [**função PtInRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) As coordenadas do cursor podem ser recuperadas processando as várias mensagens do mouse, como [**WM \_ LBUTTONDOWN,**](../inputdev/wm-lbuttondown.md) [**WM \_ LBUTTONUP,**](../inputdev/wm-lbuttonup.md) [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e [**WM \_ RBUTTONUP.**](../inputdev/wm-rbuttonup.md) O valor de retorno para PtInRegion indica se a posição do cursor está dentro da região determinada.

 

 
