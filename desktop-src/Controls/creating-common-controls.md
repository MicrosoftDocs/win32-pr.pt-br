---
title: Criando controles comuns
description: Este tópico descreve como criar uma janela que pertence a uma classe de janela definida na biblioteca de controle comum, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ddc06def47cef1a34849bbe31bc3871d4c098890bd3ef53830ae6fe7076520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916336"
---
# <a name="creating-common-controls"></a>Criando controles comuns

Este tópico descreve como criar uma janela que pertence a uma classe de janela definida na biblioteca de controle comum, Comctl32.dll.


Os controles mais comuns pertencem a uma classe de janela definida na DLL de controle comum. A classe window e o procedimento de janela correspondente definem as propriedades, a aparência e o comportamento do controle. Para garantir que a DLL de controle comum seja carregada, inclua a [**função InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) em seu aplicativo. Você cria um controle comum especificando o nome da classe de janela ao chamar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou especificando o nome de classe apropriado em um modelo de caixa de diálogo.


Cada tipo de controle comum tem um conjunto de estilos de controle que você pode usar para variar a aparência e o comportamento do controle. A biblioteca de controle comum também inclui um conjunto de estilos de controle que se aplicam a dois ou mais tipos de controles comuns. Os estilos de controle comuns são descritos na [seção Estilos.](common-control-styles.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre controles comuns](common-controls-intro.md)
</dt> </dl>

 

 