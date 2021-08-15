---
title: Visão geral do modo sem interface do usuário
description: Visão geral do modo sem interface do usuário
ms.assetid: cc0e4936-eab1-452d-9ba1-188401918e99
keywords:
- Estrutura de Serviços de Texto (TSF), UILessMode
- TSF (Estrutura de Serviços de Texto),UILessMode
- Aplicativos habilitados para TSF, UILessMode
- UILessMode
- Estrutura de Serviços de Texto (TSF), lista de candidatos UIElement
- TSF (Estrutura de Serviços de Texto), lista de candidatos UIElement
- Aplicativos habilitados para TSF, UIElement da lista de candidatos
- lista de candidatos UIElement
- Estrutura de Serviços de Texto (TSF),UIElement TIP
- TSF (Estrutura de Serviços de Texto),UIElement TIP
- Aplicativos habilitados para TSF, UIElement TIP
- DICA DE UIElement
- Estrutura de Serviços de Texto (TSF), elementos de interface do usuário predefinidos
- TSF (Estrutura de Serviços de Texto), elementos de interface do usuário predefinidos
- Aplicativos habilitados para TSF, elementos de interface do usuário predefinidos
- elementos de interface do usuário predefinidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdac8e43cc8342c50a6d232b801af0c65315fd407b9f413f2b5fdcb7074282fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949843"
---
# <a name="uiless-mode-overview"></a>Visão geral do modo sem interface do usuário

## <a name="how-to-create-uilessmode"></a>Como criar UILessMode

**Fazendo thread sem interface do usuário:** O aplicativo pode tornar um thread de interface do usuário menor [**por ITfThreadMgrEx::ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgrex-activateex) com ITF \_ AE \_ UIELEMENTENABLEDONLY. Quando o ThreadMgr é ativado com esse sinalizador, somente OS TIPs que podem controlar seu elemento de interface do usuário são ativados no thread. O aplicativo precisa implementar a interface [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) e aconselha a interface no gerenciador de threads. [**ITfUIElementSink::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-beginuielement) é chamado quando TIP mostra sua interface do usuário. O aplicativo pode retornar **TRUE no** param pbShow para permitir que TIP mostre a interface do usuário original da TIP quando o aplicativo não deseja desenhar. Se o aplicativo não permitir a interface do usuário do TIP, ele poderá retornar **FALSE** em pbShow (consulte os diagramas abaixo). O aplicativo pode desenhar a interface do usuário por si só, recebendo algumas informações do *param pElement.* Pode ser a lista de candidatos, o item de barra de idiomas ou a interface do usuário personalizada do TIP. O aplicativo pode saber o tipo de interface do usuário pela interface [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) de QIing. Quando a interface do usuário é alterada, [**ITfUIElementSink::UpdateUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementsink-updateuielement) é chamado. O aplicativo pode comparar o GUID de pElement->GetGUID() para saber se o elemento está desenhado no momento pelo aplicativo.

**Como fazer a DICA sem conhecimento da interface do usuário:** A DICA deverá dar suporte ao modo de interface do usuário menor se ela quiser ser executado no aplicativo que não deseja permitir a interface do usuário do TIP, como aplicativos de jogos ou aplicativos de tela inteira. Para ter menos conhecimento da interface do usuário, TIP precisa implementar a interface [**ITfTextInputProcessorEx.**](/windows/desktop/api/Msctf/nn-msctf-itftextinputprocessorex) Se essa interface não for implementada, TIP não será ativado no thread de modo de interface do usuário menor. Além disso, TIP deve chamar [**ITFUIElementMgr::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement) antes de mostrar uma interface do usuário visível para a tela. Esse método faz uma chamada para [**ITfUIElementSink**](/windows/desktop/api/Msctf/nn-msctf-itfuielementsink) para notificar o aplicativo. E o aplicativo decidirá se ele pode ser mostrado ou não. Quando TIP chama BeginUIElement(), TIP precisa ter a interface [**ITfUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfuielement) para a interface do usuário correspondente. O aplicativo fará a QI da interface para obter outra interface específica da interface do usuário para recuperar mais informações para desenhar a interface do usuário. O sistema [**predefine ITfCandidateListUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfcandidatelistuielement) [**e ITfReadingInformationUIElement**](/windows/desktop/api/Msctf/nn-msctf-itfreadinginformationuielement) para TIP. Quando TIP deseja mostrar a lista de candidatos no thread de modo sem interface do usuário, TIP deve criar uma instância da interface **ITfCandidateListUIElement** e chamar **ITFUIElementMgr::BeginUIElement**. Quando [**ITfTextInputProcessorEx::ActivateEx**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessorex-activateex) é chamado, TIP já sabe que o thread é menos interface do usuário para que possa eliminar a interface do usuário personalizada extra. No entanto, é claro, ele pode implementar sua própria interface que pode ser QIed de e tentar fazer uma notificação. Portanto, TIP e a **cation appli ITfUIElement** podem ter uma negociação para a interface do usuário personalizada tip.

## <a name="uielement-supporting-tip"></a>DICA de suporte de UIElement

A DICA que dá suporte ao UIElement deve ser categorizada por GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED. A DICA no GUID \_ TFCAT \_ TIPCAP \_ UIELEMENTENABLED deve usar [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) para mostrar qualquer interface do usuário para que o aplicativo possa controlar a visibilidade da interface do usuário.

**Mostrar/ocultar o status de UIElement:** Mostrar/Ocultar status indicado pelo método [**ITfUIElement::Show**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-show) ou [**ITfUIElement::IsShown**](/windows/desktop/api/Msctf/nf-msctf-itfuielement-isshown) é o status visível real. Ele não está relacionado à disponibilidade do UIElement. O UIElement deve estar sempre disponível quando o status show existir. O status show é controlável do aplicativo. O aplicativo pode mudar repentinamente para o modo sem interface do usuário e começar a desenhar uma interface do usuário por conta própria, chamando **ITfUIElement::Show** com **FALSE** para ocultar toda a interface do usuário do TIP. Em seguida, TIP pode usar uma de algumas opções. 1) TIP pode mover o UIElement para o status Ocultar e começar a gerar UpdateUIElement. 2) TIP pode concluir UIElement, pois o elemento de interface do usuário não dá suporte a Ocultar status e tip chama EndUIElement() para finalização.

## <a name="predefined-ui-elements"></a>Elementos de interface do usuário predefinidos

**A lista de candidatos:** A lista de candidatos é um dos principais elementos de interface do usuário para entrada EA. Esse Elemento de interface do usuário fornece a lista de candidatos e o número correspondente das cadeias de caracteres candidatas para desenho.

**A janela de informações de leitura** A janela de informações de leitura é comum para entrada de teclado chinês. Ele tem o estágio que não pode ser inserido no documento como a cadeia de caracteres de composição. Um processador de entrada chinês abre uma pequena janela de informações de leitura que mostra as informações de leitura, de phonetic ou de digitação.

## <a name="the-flow-chart-of-uilessmode"></a>O gráfico de fluxo de UILessMode

![Diagrama que mostra o gráfico de fluxo de U I LessMode.](images/tsf-uilessmode-ovw1.gif)

Depois que a DICA receber **TRUE** em \* pbShown por [**ITfUIElementMgr::BeginUIElement**](/windows/desktop/api/Msctf/nf-msctf-itfuielementmgr-beginuielement), a TIP não precisa chamar UpdateUIElement para o UIElement. Mas TIP precisa chamar EndUIElement() para que [**ITfUIElementMgr**](/windows/desktop/api/Msctf/nn-msctf-itfuielementmgr) e o aplicativo possam acompanhar o status de UIElement. TIP deve chamar UpdateUIElement() depois que BeginUIElement() retornar **FALSE** em \* pbShow. O aplicativo que deseja desenhar a interface do usuário não verifica o conteúdo em BeginUIElement(), ele apenas retorna o status de show em BeginUIElement() e começa a verificar o conteúdo em UpdateUIElement(). Por exemplo, o sinalizador de atualização da lista de candidatos UIElement tem todos os bits no primeiro UpdateUIElement(). Isso significa que o conteúdo de UIElement não precisa estar pronto em BeginUIElement().

![Diagrama que mostra quando o T IP chama 'ITUIElementMgr::BeginUIElement()' e 'BeginUIElement of application's UIElementSink' é chamado.](images/tsf-uilessmode-ovw2.gif)![Diagrama que mostra que o aplicativo retorna FALSE em *pbShow.](images/tsf-uilessmode-ovw3.gif)![gráfico de fluxo de uilessmode](images/tsf-uilessmode-ovw4.gif)

## <a name="the-candidate-list-uielement"></a>A lista de candidatos UIElement

**Sobre PageIndex:** O aplicativo que desenha a lista de candidatos calculará o número de cadeias de caracteres por página quando o conteúdo da lista for alterado (TF \_ CLUIE \_ STRING está definido). Não é bom alterar o índice de página enquanto a lista de candidatos está disponível para o modo sem interface do usuário. Isso significa que a lista de candidatos do TIP deve se comportar na paging em vez de rolar quando a seleção é movida para a próxima página. Se a rolagem ocorrer na seleção, o índice da página será alterado e o aplicativo precisará recalcular o índice da página. O resultado pode não ser esperado pelo TIP.

**Sem Seleção:** [**ITfCandidateListUIElement::GetSelection**](/windows/desktop/api/Msctf/nf-msctf-itfcandidatelistuielement-getselection) retornará S FALSE, se a lista de \_ candidatos não tiver uma seleção. O valor de retorno do primeiro param é inválido.

 

 




