---
description: A partir do Windows Vista, o TextInputPanel substitui o PenInputPanel para controlar a aparência e o comportamento da tela do painel de entrada do Tablet. as seções a seguir descrevem a programação do painel de entrada usando as interfaces de programação de aplicativo do painel de entrada de texto. TextInputPanel para usuários do painel de entrada do PenInputPanelUsing AutoCompleteEnabling correção de texto para tinta personalizada CollectorsNote o painel de entrada de texto é implementado em um arquivo executável chamado TabTip.exe. A execução de TabTip.exe com o parâmetro/SeekDesktop tenta executar uma versão de funcionalidade reduzida do painel de entrada em uma área de trabalho interativa não padrão, conforme criado com createdesktop. Para as áreas de trabalho mais criadas, o painel de entrada será executado automaticamente nesse modo. Esse parâmetro fornece os meios para iniciá-lo em cenários de aplicativos incomuns que, caso contrário, impedem o lançamento automático. Se o painel de entrada já estiver em execução na área de trabalho, esse parâmetro não terá efeito e a instância do TabTip.exe será encerrada imediatamente.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programando o painel de entrada de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785963"
---
# <a name="programming-the-text-input-panel"></a>Programando o painel de entrada de texto

A partir do Windows Vista, o [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) substitui o [**PenInputPanel**](peninputpanel-class.md) para controlar a aparência e o comportamento da tela do painel de entrada do Tablet.

As seções a seguir descrevem a programação do painel de entrada usando as interfaces de programação de aplicativo do painel de entrada de texto.

-   [TextInputPanel para usuários de PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Usando o preenchimento automático do painel de entrada](using-input-panel-autocomplete.md)
-   [Habilitando a correção de texto para coletores de tinta personalizados](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> O painel de entrada de texto é implementado em um arquivo executável chamado TabTip.exe. A execução de TabTip.exe com o parâmetro */SeekDesktop* tenta executar uma versão de funcionalidade reduzida do painel de entrada em uma área de trabalho interativa não padrão, conforme criado com [**createdesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa). Para as áreas de trabalho mais criadas, o painel de entrada será executado automaticamente nesse modo. Esse parâmetro fornece os meios para iniciá-lo em cenários de aplicativos incomuns que, caso contrário, impedem o lançamento automático. Se o painel de entrada já estiver em execução na área de trabalho, esse parâmetro não terá efeito e a instância do TabTip.exe será encerrada imediatamente.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Programando o painel de entrada usando a classe PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
