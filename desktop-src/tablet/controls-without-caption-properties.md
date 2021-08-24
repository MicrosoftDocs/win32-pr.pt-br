---
description: Introdução ao uso de controles sem propriedades de legenda para o Tablet PC.
ms.assetid: 8c44e1eb-8d57-4c3b-a329-c8ad77423cb7
title: Controles sem propriedades de legenda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5cd8eb0c87f946d8540fb63d75408dcf98a880cefcd1ba295ba2ba113e6828f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774106"
---
# <a name="controls-without-caption-properties"></a>Controles sem propriedades de legenda

Quando um controle não tiver sua própria propriedade Caption, execute as seguintes etapas para garantir que os auxílios de acessibilidade possam identificar os controles:

-   Crie um controle de texto estático com um nome descritivo e significativo.
-   Coloque o rótulo estático para que ele preceda imediatamente o controle referenciado, na ordem de tabulação.
-   verifique se o texto do rótulo termina com dois-pontos, por exemplo, "Configurações:"
-   Posicione o texto do rótulo imediatamente à esquerda ou antes do controle referenciado.
-   Torne o texto estático invisível se não for apropriado exibi-lo visualmente. Faça isso atribuindo o atributo apropriado no script de recurso. Isso pode ser apropriado quando o nome ou a função de um controle é fornecido visualmente por meio de um controle de texto estático, como um gráfico ou um botão de opção relacionado.

O uso adequado de controles estáticos é a única maneira de implementar corretamente chaves de acesso de sublinhado para controles que não têm rótulos intrínsecos. Para obter mais informações sobre como usar controles que não têm propriedades de legenda, consulte a seção [acessibilidade](/windows/desktop/accessibility) .

 

 
