---
title: Cursores
description: Esta seção aborda os cursores que são pequenas imagens cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\cursors.htm
keywords:
- recursos, cursores
- cursores, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9014befcc41161d7491af97186b33088f508dd8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005599"
---
# <a name="cursors"></a>Cursores

Um cursor é uma pequena imagem cujo local na tela é controlado por um dispositivo apontador, como um mouse, uma caneta ou um trackball. No restante desta visão geral, o termo mouse se refere a qualquer dispositivo apontador.

Quando o usuário move o mouse, o sistema move o cursor de acordo. As funções de cursor permitem que os aplicativos criem, carreguem, exibam, animem, movam, confinam e destruam cursores.

### <a name="in-this-section"></a>Nesta seção



| Nome                                     | Descrição                                                   |
|------------------------------------------|---------------------------------------------------------------|
| [Sobre cursores](about-cursors.md)       | Discute os cursores padrão.<br/>                    |
| [Usando cursores](using-cursors.md)       | Discute como executar tarefas relacionadas a cursores.<br/> |
| [Referência do cursor](cursor-reference.md) | Contém a referência de API.<br/>                        |



 

### <a name="cursor-functions"></a>Funções do cursor



| Nome                                                 | Descrição                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor)                     | Ajusta o cursor para uma área retangular na tela. Se uma posição de cursor subsequente (definida pela função [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) ou pelo mouse) estiver fora do retângulo, o sistema ajustará automaticamente a posição para manter o cursor dentro da área retangular. <br/> |
| [**CopyCursor**](/windows/desktop/api/Winuser/nf-winuser-copycursor)                     | Copia o cursor especificado. <br/>                                                                                                                                                                                                                                                               |
| [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor)                 | Cria um cursor com o tamanho especificado, os padrões de bits e o ponto de acesso. <br/>                                                                                                                                                                                                                    |
| [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)               | Destrói um cursor e libera qualquer memória do cursor ocupada. Não use essa função para destruir um cursor compartilhado.<br/>                                                                                                                                                                            |
| [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor)               | Recupera as coordenadas de tela da área retangular à qual o cursor está confinado. <br/>                                                                                                                                                                                                  |
| [**GetCursor**](/windows/desktop/api/Winuser/nf-winuser-getcursor)                       | Recupera um identificador para o cursor atual. <br/>                                                                                                                                                                                                                                                  |
| [**GetCursorInfo**](/windows/desktop/api/Winuser/nf-winuser-getcursorinfo)               | Recupera informações sobre o cursor global.<br/>                                                                                                                                                                                                                                              |
| [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos)                 | Recupera a posição do cursor, em coordenadas da tela.<br/>                                                                                                                                                                                                                                     |
| [**GetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getphysicalcursorpos) | Recupera a posição do cursor em coordenadas físicas.<br/>                                                                                                                                                                                                                               |
| [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)                     | Carrega o recurso de cursor especificado do executável (. EXE) associado a uma instância do aplicativo.<br/>                                                                                                                                                                                |
| [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)     | Cria um cursor com base nos dados contidos em um arquivo. <br/>                                                                                                                                                                                                                                        |
| [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor)                       | Define a forma do cursor. <br/>                                                                                                                                                                                                                                                                     |
| [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos)                 | Move o cursor para as coordenadas de tela especificadas. Se as novas coordenadas não estiverem dentro do retângulo da tela definido pela chamada de função [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) mais recente, o sistema ajustará automaticamente as coordenadas para que o cursor permaneça dentro do retângulo. <br/>    |
| [**SetPhysicalCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setphysicalcursorpos) | Define a posição do cursor em coordenadas físicas.<br/>                                                                                                                                                                                                                                    |
| [**SetSystemCursor**](/windows/desktop/api/Winuser/nf-winuser-setsystemcursor)           | Permite que um aplicativo Personalize os cursores do sistema. Ele substitui o conteúdo do cursor do sistema especificado pelo parâmetro *ID* pelo conteúdo do cursor especificado pelo parâmetro *hcur* e, em seguida, destrói *hcur*. <br/>                                                          |
| [**Obter cursor**](/windows/desktop/api/Winuser/nf-winuser-showcursor)                     | Exibe ou oculta o cursor. <br/>                                                                                                                                                                                                                                                              |



 

### <a name="cursor-notifications"></a>Notificações do cursor



| Nome                                  | Descrição                                                                                                          |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**WM \_ SETcursor**](wm-setcursor.md) | Enviado a uma janela se o mouse fizer com que o cursor se mova dentro de uma janela e a entrada do mouse não for capturada. <br/> |



 

### <a name="cursor-structures"></a>Estruturas de cursor



| Nome                             | Descrição                                    |
|----------------------------------|------------------------------------------------|
| [**CURSORINFO**](/windows/win32/api/winuser/ns-winuser-cursorinfo) | Contém informações de cursor global.<br/> |



 

 

 





