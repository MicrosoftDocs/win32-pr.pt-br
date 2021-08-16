---
description: Controles sem janela podem chamar a função SetInputScope sempre que o foco é movido entre os elementos do controle sem janela; no entanto, isso não é recomendado por motivos de desempenho.
ms.assetid: 616ffe1a-3788-4a99-bbfa-6cbaf45b93b7
title: Configurando contexto para controles sem janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c2093c0e475b3f88ee94baa93c4821696cba5b6c8dd89dce6bf0661c1d0593
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589866"
---
# <a name="setting-context-for-windowless-controls"></a>Configurando contexto para controles sem janela

Controles sem janela podem chamar a função [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) sempre que o foco é movido entre os elementos do controle sem janela; no entanto, isso não é recomendado por motivos de desempenho.

 

 
