---
description: Visão geral das práticas recomendadas ao usar o objeto do painel de entrada da caneta.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Práticas recomendadas (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172068"
---
# <a name="best-practices-tablet-pc"></a>Práticas recomendadas (Tablet PC)

Há algumas diretrizes para ter em mente ao usar o objeto [**PenInputPanel**](peninputpanel-class.md) .

-   [Preferir o controle InkEdit](#prefer-inkedit-control)
-   [Desabilitar modo de tinta em controles InkEdit](#disable-ink-mode-on-inkedit-controls)
-   [Usando controles sem janela](#using-windowless-controls)
-   [Tópicos relacionados](#related-topics)

## <a name="prefer-inkedit-control"></a>Preferir o controle InkEdit

[InkEdit](inkedit-control-reference.md) é o controle preferencial ao qual anexar o objeto [**PenInputPanel**](peninputpanel-class.md) . O controle InkEdit fornece suporte para a [TSF (estrutura de serviços de texto)](text-services-framework.md).

## <a name="disable-ink-mode-on-inkedit-controls"></a>Desabilitar modo de tinta em controles InkEdit

Quando anexado a um controle [InkEdit](inkedit-control-reference.md) , defina a propriedade [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) do controle InkEdit como o valor [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) . Se a propriedade **InkMode** não estiver definida como o valor de **InkMode** , o controle InkEdit interpretará o primeiro toque como um traço, o passará para o reconhecedor e inserirá o texto no controle InkEdit. Como você já tem um objeto [**PenInputPanel**](peninputpanel-class.md) anexado para aceitar entrada à tinta, não é necessário ter o controle InkEdit também habilitado para entrada à tinta.

## <a name="using-windowless-controls"></a>Usando controles sem janela

Quando um objeto [**PenInputPanel**](peninputpanel-class.md) é anexado a uma janela pai que contém mais de um controle sem janela, o objeto **PenInputPanel** não sabe como controlar o cursor como o foco se move entre os filhos sem janelas. A entrada de manuscrito pode ser enviada para o filho incorreto quando o foco é movido de um controle sem janela para outro enquanto a entrada está pendente.

Para usar o objeto [**PenInputPanel**](peninputpanel-class.md) em um ambiente sem janelas, a técnica a seguir pode ser usada:

1.  Crie uma instância de um controle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) e posicione-o sobre o controle sem janela.
2.  Anexe o objeto [**PenInputPanel**](peninputpanel-class.md) ao novo controle de caixa de texto.
3.  Deixe o controle de caixa de texto coletar o texto reconhecido do objeto [**PenInputPanel**](peninputpanel-class.md) .
4.  Quando o foco é alterado para fora do controle de caixa de texto, chame o método [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) do objeto [**PenInputPanel**](peninputpanel-class.md) .
5.  Copie o texto reconhecido do controle caixa de texto para o filho sem janela.
6.  Desanexe o objeto [**PenInputPanel**](peninputpanel-class.md) definindo sua propriedade [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (código gerenciado somente) ou a propriedade [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) como NULL.
7.  Destrua o controle de caixa de texto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Classe PenInputPanel**](peninputpanel-class.md)
</dt> <dt>

[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))
</dt> <dt>

[Estrutura de serviços de texto](../tsf/text-services-framework.md)
</dt> </dl>

 

 
