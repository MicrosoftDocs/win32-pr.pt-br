---
description: O atributo de estilo especifica o padrão de linha que aparece quando uma caneta geométrica ou superficial específica é usada. Há oito estilos de caneta predefinidos. A ilustração a seguir mostra os sete desses estilos definidos pelo sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Estilo de caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42cc82510c58d36cec76039488ecc13c826609a0870b929f18d82282a87ba8cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666506"
---
# <a name="pen-style"></a>Estilo de caneta

O atributo de estilo especifica o padrão de linha que aparece quando uma caneta geométrica ou superficial específica é usada. Há oito estilos de caneta predefinidos. A ilustração a seguir mostra os sete desses estilos definidos pelo sistema.

![ilustração mostrando sete linhas, cada uma desenhada usando um estilo predefinido diferente](images/cspen-01.png)

O estilo de quadro interno é idêntico ao estilo sólido para canetas cosméticas. No entanto, ele opera de forma diferente quando usado com uma caneta geométrica. Se a caneta geométrica for maior do que um único pixel e uma função de desenho usar a caneta para desenhar uma borda em torno de um objeto preenchido, o sistema desenhará a borda dentro do quadro do objeto. Usando o estilo de quadro interno, um aplicativo pode garantir que um objeto apareça inteiramente dentro das dimensões especificadas, independentemente da largura da caneta geométrica.

Além dos sete estilos definidos pelo sistema, há um oitavo estilo definido pelo usuário (ou aplicativo). Um estilo definido pelo usuário gera linhas com uma série personalizada de traços e pontos.

Use a [**função CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) para criar uma caneta que tenha os estilos definidos pelo sistema. Use a **função ExtCreatePen** para criar uma caneta que tenha um estilo definido pelo usuário.

 

 



