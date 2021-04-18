---
description: Visão geral da estrutura de serviços de texto para o Tablet PC.
ms.assetid: f77fe77a-8625-47c5-bfc7-b473c8e8a8c6
title: Estrutura de serviços de texto (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25eb3e635ae7394502ed203cb9ea31e115dc09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788085"
---
# <a name="text-services-framework-tablet-pc"></a>Estrutura de serviços de texto (Tablet PC)

Quando a [estrutura de serviços de texto (TSF)](../tsf/text-services-framework.md) é habilitada em um controle com um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) anexado, o objeto PenInputPanel pode inserir texto diretamente. Se o controle não oferecer suporte à TSF (estrutura de serviços de texto), o objeto PenInputPanel deverá recorrer ao uso da [função SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) para inserir texto.

A capacidade de inserir texto diretamente se torna muito importante para aqueles que estão inserindo caracteres do leste asiático, em que o uso da [função SendInput](/windows/win32/api/winuser/nf-winuser-sendinput) pode produzir caracteres incorretos.

O TSF fornece uma interface para corrigir erros de reconhecimento, permitindo que o usuário final corrija, reescreva ou até mesmo dite o texto adequado.

O TSF é habilitado chamando o método [EnableTsf](/previous-versions/ms569656(v=vs.100)) com o parâmetro *Enable* definido como **true**.

\[C\#\]


```C++
PenInputPanel thePenInputPanel = new PenInputPanel(theControl);
//...
thePenInputPanel.EnableTsf(true);
```



Um objeto [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) anexado a um controle [InkEdit](/previous-versions/ms552265(v=vs.100)) fornece uma experiência de usuário robusta, pois INKEDIT dá suporte a TSF. No entanto, certifique-se de definir a propriedade [InkMode](/previous-versions/ms835850(v=msdn.10)) como [Microsoft. Ink. InkMode. Ink](/previous-versions/ms827399(v=msdn.10)) no controle InkEdit conforme mencionado no tópico [práticas recomendadas](best-practices.md) .

O [exemplo PenInputPanel](peninputpanel-sample.md) fornece um exemplo de como habilitar o TSF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estrutura de serviços de texto](../tsf/text-services-framework.md)
</dt> </dl>

 

 
