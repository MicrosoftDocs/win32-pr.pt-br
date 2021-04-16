---
title: Visão geral do modo de UILess
description: Visão geral do modo de UILess
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- TSF (estrutura de serviços de texto), UILessMode
- TSF (estrutura de serviços de texto), UILessMode
- Aplicativos habilitados para TSF, UILessMode
- UILessMode
- TSF (estrutura de serviços de texto), lista de candidatos UIElement
- TSF (estrutura de serviços de texto), UIElement de lista de candidatos
- Aplicativos habilitados para TSF, lista de candidatos UIElement
- UIElement da lista de candidatos
- TSF (estrutura de serviços de texto), dica UIElement
- TSF (estrutura de serviços de texto), dica UIElement
- Aplicativos habilitados para TSF, dica UIElement
- Dica UIElement
- TSF (estrutura de serviços de texto), elementos de interface do usuário predefinidos
- TSF (estrutura de serviços de texto), elementos de interface do usuário predefinidos
- Aplicativos habilitados para TSF, elementos de interface do usuário predefinidos
- elementos predefinidos da interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7354a88fb28fd0d6bf5f4180ac23359a2117fe7
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104554035"
---
# <a name="uiless-mode-overview"></a>Visão geral do modo de UILess

## <a name="how-to-create-uilessmode"></a>Como criar UILessMode

**Criando thread sem interface do usuário:** O aplicativo pode tornar uma interface do usuário com menos thread por [**ITfThreadMgrEx:: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) com ITF \_ AE \_ UIELEMENTENABLEDONLY. Quando ThreadMgr é ativado com esse sinalizador, somente as dicas que podem controlar seu elemento de interface do usuário são ativadas no thread. O aplicativo precisa implementar a interface [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) e aconselhar a interface no Gerenciador de threads. [**ITfUIElementSink:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) é chamado quando Tip mostra sua interface do usuário. O aplicativo pode retornar **true** no parâmetro pbShow para permitir que a dica mostre a interface do usuário original da dica quando o aplicativo não deseja desenhar. Se o aplicativo não permitir a interface do usuário de TIP, ele poderá retornar **false** em pbShow (consulte os diagramas abaixo). O aplicativo pode desenhar a interface do usuário por si só obtendo algumas informações do parâmetro *pElement* . Pode ser a lista de candidatos, o item de barra de idiomas ou a interface do usuário personalizada de TIP. O aplicativo pode saber o tipo de interface do usuário pela interface QIing [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) . Quando a interface do usuário é alterada, [**ITfUIElementSink:: UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) é chamado. O aplicativo pode comparar o GUID de pElement->GetGuid () para saber se o elemento está desenhado no momento pelo aplicativo.

**Criando dica com menos reconhecimento à interface do usuário:** A TIP deve dar suporte ao modo menos de interface do usuário se quiser executar sob o aplicativo que não deseja permitir a interface do usuário da TIP, como aplicativos de jogo ou de tela inteira. Para ser menos ciente da interface do usuário, a TIP precisa implementar a interface [**ITfTextInputProcessorEx**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) . Se essa interface não for implementada, a TIP não será ativada sob o thread de modo inferior da interface do usuário. Além disso, a TIP deve chamar [**ITFUIElementMgr:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) antes de mostrar uma interface do usuário visível na tela. Esse método faz uma chamada para [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) para notificar o aplicativo. E o aplicativo decidirá se ele pode ser mostrado ou não. Quando TIP chama BeginUIElement (), a TIP precisa ter a interface [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) para a interface do usuário correspondente. O aplicativo irá QI da interface para obter outra interface específica da interface do usuário para recuperar mais informações para desenhar a interface do usuário. O sistema predefine [**ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) e [**ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) para Tip. Quando a dica deseja mostrar a lista de candidatos em thread de modo inferior da interface do usuário, a TIP deve criar uma instância da interface **ITfCandidateListUIElement** e chamar **ITFUIElementMgr:: BeginUIElement**. Quando [**ITfTextInputProcessorEx:: ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) é chamado, a dica já sabe que o thread é a interface do usuário menos para que possa eliminar a interface do usuário personalizada extra. No entanto, é claro que ele pode implementar sua própria interface que pode ser QIed e tentar fazer uma notificação. Portanto, a TIP e a **ITfUIElement** de aplicação podem ter uma negociação para a interface do usuário personalizada da TIP.

## <a name="uielement-supporting-tip"></a>Dica de suporte a UIElement

A dica que dá suporte ao UIElement deve ser categorizada por GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED. A TIP no GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED deve usar [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) para mostrar qualquer interface do usuário para que o aplicativo possa controlar a visibilidade da interface do usuário.

**Mostrar/ocultar status do UIElement:** Mostrar/ocultar status indicado pelo método [**ITfUIElement:: show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) ou [**ITfUIElement:: ismostren**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) é o status real visível. Ele não está relacionado à disponibilidade do UIElement. O UIElement deve estar sempre disponível quando o status de exibição existir. O status de exibição é controlável do aplicativo. O aplicativo pode repentinamente mudar para o modo UILess e começar a desenhar alguma interface do usuário por si só, chamando **ITfUIElement:: show** com **false** para ocultar toda a interface do usuário de Tip. Em seguida, a TIP pode executar uma de algumas opções. 1) a TIP pode mover o UIElement para o status de ocultar e começar a gerar UpdateUIElement. 2) a TIP pode concluir o UIElement, pois o elemento de interface do usuário não dá suporte a ocultar status e Tip chama enduielement () para concluí-lo.

## <a name="predefined-ui-elements"></a>Elementos predefinidos da interface do usuário

**A lista de candidatos:** A lista de candidatos é um dos principais elementos da interface do usuário para a entrada EA. Este elemento de interface do usuário fornece a lista de candidatos e o número correspondente de cadeias de caracteres candidatas para desenho.

**A janela de informações de leitura** A janela de informações de leitura é comum para entrada de teclado chinês. Ele tem o estágio que não pode ser inserido no documento como a cadeia de caracteres de composição. Um processador de entrada em chinês abre uma pequena janela de informações de leitura que mostra as informações de leitura, fonética ou digitação.

## <a name="the-flow-chart-of-uilessmode"></a>O gráfico de fluxo de UILessMode

![Diagrama que mostra o gráfico de fluxo U I Lessmode.](images/tsf-uilessmode-ovw1.gif)

Depois que a dica recebe **true** em \* pbShown by [**ITfUIElementMgr:: BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement), a Tip não precisa chamar UpdateUIElement para o UIElement. Mas a TIP precisa chamar enduielement () para que o [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) e o aplicativo possam acompanhar o status de UIElement. A TIP deve chamar UpdateUIElement () depois de BeginUIElement () retornar **false** em \* pbShow. O aplicativo que deseja desenhar a interface do usuário não verifica o conteúdo em BeginUIElement (), ele apenas retorna o status show em BeginUIElement () e inicia a verificação do conteúdo em UpdateUIElement (). Por exemplo, o sinalizador de atualização da lista de candidatos UIElement tem todos os bits no primeiro UpdateUIElement (). Isso significa que o conteúdo de UIElement não precisa estar pronto em BeginUIElement ().

![Diagrama que mostra quando o T I P chama ' ITUIElementMgr:: BeginUIElement () ' e ' BeginUIElement de UIElementSink do aplicativo ' é chamado.](images/tsf-uilessmode-ovw2.gif)![O diagrama que mostra o aplicativo retorna falso em * pbShow.](images/tsf-uilessmode-ovw3.gif)![gráfico de fluxo uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>O UIElement da lista de candidatos

**Sobre pageIndex:** O aplicativo que desenha a lista de candidatos calculará o número de cadeias de caracteres por página quando o conteúdo da lista for alterado (TF \_ CLUIE \_ cadeia de caracteres está definida). Não é bom alterar o índice da página enquanto a lista de candidatos está disponível para o modo UILess. Isso significa que a lista de candidatos da TIP deve se comportar com a paginação em vez de rolar quando a seleção for movida para a próxima página. Se a rolagem ocorrer na seleção for movida, o índice da página será alterado e o aplicativo precisará recalcular o índice da página. O resultado pode não ser esperado por TIP.

**Nenhuma seleção:** [**ITfCandidateListUIElement:: GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) retornará S \_ false, se a lista de candidatos não tiver uma seleção. O valor de retorno do primeiro parâmetro é inválido.

 

 




