---
description: Um aplicativo executa testes de clique em regiões para determinar as coordenadas da posição atual do cursor.
ms.assetid: 861a2558-0967-43f6-be3f-580992da05ff
title: Regiões de teste de clique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe136c3ba9ab4babfc1150ae4c3eee878cb42327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165074"
---
# <a name="hit-testing-regions"></a>Regiões de teste de clique

Um aplicativo executa testes de clique em regiões para determinar as coordenadas da posição atual do cursor. Em seguida, ele passa essas coordenadas, bem como um identificador que identifica a região para a função [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) . As coordenadas do cursor podem ser recuperadas processando as várias mensagens do mouse, como o [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) , o [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) , o [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e o [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md). O valor de retorno para PtInRegion indica se a posição do cursor está dentro da região especificada.

 

 
