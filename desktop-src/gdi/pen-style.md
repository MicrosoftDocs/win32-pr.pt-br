---
description: O atributo Style especifica o padrão de linha que aparece quando uma caneta superficial ou geométrica específica é usada. Há oito estilos de caneta predefinidos. A ilustração a seguir mostra os sete desses estilos que são definidos pelo sistema.
ms.assetid: a9aaa999-529c-46e1-9a3f-b6fdcbeb5b51
title: Estilo da caneta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f447839627f97d7662fdef35bd7088ef7b0dcba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921285"
---
# <a name="pen-style"></a>Estilo da caneta

O atributo Style especifica o padrão de linha que aparece quando uma caneta superficial ou geométrica específica é usada. Há oito estilos de caneta predefinidos. A ilustração a seguir mostra os sete desses estilos que são definidos pelo sistema.

![ilustração mostrando sete linhas, cada uma desenhada usando um estilo predefinido diferente](images/cspen-01.png)

O estilo de quadro interno é idêntico ao estilo sólido para canetas superficiais. No entanto, ele funciona de forma diferente quando usado com uma caneta geométrica. Se a caneta geométrica for mais ampla do que um único pixel e uma função de desenho usar a caneta para desenhar uma borda em torno de um objeto preenchido, o sistema desenhará a borda dentro do quadro do objeto. Usando o estilo de quadro interno, um aplicativo pode garantir que um objeto apareça inteiramente dentro das dimensões especificadas, independentemente da largura da caneta geométrica.

Além dos sete estilos definidos pelo sistema, há um oitavo estilo definido pelo usuário (ou aplicativo). Um estilo definido pelo usuário gera linhas com uma série personalizada de traços e pontos.

Use a função [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)ou [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) para criar uma caneta que tenha os estilos definidos pelo sistema. Use a função **ExtCreatePen** para criar uma caneta que tenha um estilo definido pelo usuário.

 

 



