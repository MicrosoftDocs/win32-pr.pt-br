---
description: Visão geral de como nomear uma janela adequadamente e definir a legenda da janela para o Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Nomeando uma janela adequadamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f2109568306e8817c518eecd8761ab00a2b1ecb8c54d4388b78e3eb456278d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883396"
---
# <a name="naming-a-window-appropriately"></a>Nomeando uma janela adequadamente

Atribua a cada janela uma legenda amigável, mesmo que a janela ou sua legenda seja invisível. Isso permite que a funcionalidade de fala identifique a janela e a hierarquia da janela. Essa recomendação se aplica a todas as janelas: janelas de nível superior com quadros visíveis; janelas filho, como paletas flutuantes; controles personalizados; barras de ferramentas; e painéis dentro de uma janela, quando implementados como janelas filho.

Há três maneiras de definir a legenda da janela:

-   Definir a cadeia de caracteres no script de recurso ao chamar [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou funções relacionadas.
-   Chame a [**função SetWindowText.**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta)
-   Defina o nome dos controles nas caixas de diálogo usando as técnicas descritas em Controles de [Nomen entre Caixas de Diálogo](naming-controls-in-dialog-boxes.md). Esse é o único método para rotular um controle de edição, pois definir o rótulo intrínseco dos controles altera o conteúdo dos controles.

Você pode consultar a legenda usando a Microsoft Active Accessibility ou a mensagem WM \_ GETTEXT.

Para obter mais informações sobre como consultar a legenda usando Acessibilidade Ativa, consulte a [seção Acessibilidade.](/windows/desktop/accessibility)

 

 
