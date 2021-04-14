---
title: Interpolação
description: Esta seção discute os Cursors que são linhas de intermitência, blocos ou bitmaps na área do cliente de uma janela.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- recursos, Cursors
- Cursors, sobre
- linhas piscando
- blocos piscando
- bitmaps piscando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104370804"
---
# <a name="carets"></a>Interpolação

Um *cursor* é uma linha, bloco ou bitmap piscando na área do cliente de uma janela. O cursor normalmente indica o local no qual o texto ou os gráficos serão inseridos.

A ilustração a seguir mostra algumas variações comuns na aparência do cursor.

![Mostra 5 maneiras diferentes que um cursor pode exibir.](images/cscrt-01.png)

Os aplicativos podem criar um cursor, alterar o tempo de intermitência e exibir, ocultar ou realocar o cursor.

### <a name="in-this-section"></a>Nesta seção



| Nome                                   | Descrição                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [Sobre os Cursors](about-carets.md)       | Discute os acentos.<br/>                                              |
| [Usando os Cursors](using-carets.md)       | Exemplos de código que mostram como executar tarefas relacionadas a Cursors.<br/> |
| [Referência de cursor](caret-reference.md) | Contém a referência de API.<br/>                                    |



 

### <a name="caret-functions"></a>Funções de cursor



| Nome                                           | Descrição                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Não importa**](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | Cria uma nova forma para o cursor do sistema e atribui a propriedade do cursor à janela especificada. A forma do cursor pode ser uma linha, um bloco ou um bitmap. <br/>                                                                                         |
| [**DestroyCaret**](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | Destrói a forma atual do cursor, libera o cursor da janela e remove o cursor da tela. <br/>                                                                                                                                       |
| [**GetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | Recupera o tempo necessário para inverter os pixels do cursor. O usuário pode definir esse valor. <br/>                                                                                                                                                            |
| [**GetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | Copia a posição do cursor para a estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) especificada. <br/>                                                                                                                                                                    |
| [**HideCaret**](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | Remove o cursor da tela. Ocultar um cursor não destrói sua forma atual ou invalidar o ponto de inserção. <br/>                                                                                                                           |
| [**SetCaretBlinkTime**](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | Define o tempo de intermitência do cursor para o número especificado de milissegundos. O tempo de intermitência é o tempo decorrido, em milissegundos, necessário para inverter os pixels do cursor. <br/>                                                                                    |
| [**SetCaretPos**](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | Move o cursor para as coordenadas especificadas. Se a janela que possui o cursor tiver sido criada com o estilo de classe **cs \_ OWNDC** , as coordenadas especificadas estarão sujeitas ao modo de mapeamento do contexto do dispositivo associado a essa janela. <br/> |
| [**Não importa**](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | Torna o cursor visível na tela na posição atual do cursor. Quando o cursor se torna visível, ele começa a piscar automaticamente. <br/>                                                                                                          |



 

 

