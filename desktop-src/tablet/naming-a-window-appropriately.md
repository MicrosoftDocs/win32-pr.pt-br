---
description: Visão geral de nomear uma janela adequadamente e definir a legenda da janela para o Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Nomeando uma janela adequadamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771764"
---
# <a name="naming-a-window-appropriately"></a>Nomeando uma janela adequadamente

Atribua a cada janela uma legenda amigável, mesmo se a janela ou sua legenda estiver invisível. Isso permite que a funcionalidade de fala identifique a janela e a hierarquia da janela. Essa recomendação se aplica a todas as janelas: janelas de nível superior com quadros visíveis; janelas filhas, como paletas flutuantes; controles personalizados; barras e painéis dentro de uma janela, quando implementados como janelas filhas.

Há três maneiras de definir a legenda da janela:

-   Defina a cadeia de caracteres no script de recurso ao chamar [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou funções relacionadas.
-   Chame a função [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .
-   Defina o nome dos controles nas caixas de diálogo usando as técnicas descritas em [controles de nomenclatura nas caixas de diálogo](naming-controls-in-dialog-boxes.md). Esse é o único método para rotular um controle de edição, pois definir o rótulo intrínseco dos controles altera o conteúdo dos controles.

Você pode consultar a legenda usando o Microsoft Acessibilidade Ativa ou a mensagem de \_ gettext do WM.

Para obter mais informações sobre como consultar a legenda usando Acessibilidade Ativa, consulte a seção [acessibilidade](/windows/desktop/accessibility) .

 

 
