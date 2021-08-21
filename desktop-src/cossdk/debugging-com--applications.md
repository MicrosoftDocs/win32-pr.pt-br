---
description: As técnicas de depuração para aplicativos COM+ dependem do idioma em que você opta por escrever seu componente.
ms.assetid: 781a0b3f-2bd0-435b-b6fe-4469cc02e8b6
title: Depurando aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcce186a954098bdebd4e7e326328b8be269a88ed9567a3e63185662fcda3d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307294"
---
# <a name="debugging-com-applications"></a>Depurando aplicativos COM+

As técnicas de depuração para aplicativos COM+ dependem do idioma em que você opta por escrever seu componente.

se você codificar em Microsoft Visual C++, poderá iniciar o depurador em C++ ou, com um cliente remoto, poderá depurar usando o controle de procedimento remoto OLE (RPC) e a depuração just-in-time (JIT). Você sempre pode usar a ferramenta administrativa serviços de componentes para depurar seu componente com a configuração COM+ **Iniciar no depurador** na guia **avançado** da caixa de diálogo **Propriedades** do aplicativo com+. Para obter mais informações sobre os componentes de depuração codificados em C++, consulte [depuração de componentes escritos em Visual C++](debugging-components-written-in-visual-c--.md).

a menos que você esteja depurando no momento vários threads, rastreamento de componentes, chamadas remotas ou isolamento de processo, você pode usar o ambiente de Visual Basic da Microsoft para fins de depuração. [componentes de depuração escritos em Visual Basic](debugging-components-written-in-visual-basic.md) descreve o processo de depuração em um ambiente de Visual Basic.

o tópico [depurando no Visual Basic IDE](debugging-in-the-visual-basic-ide.md) fornece uma visão geral com diretrizes, dicas e um procedimento sobre a depuração no ide (ambiente de desenvolvimento integrado).

para exibir mais informações sobre a depuração de processos avançados, consulte [depurando componentes Visual Basic compilados](debugging-compiled-visual-basic-components.md).

> [!Note]  
> várias limitações associadas ao uso do ambiente de Visual Basic para depurar componentes com o MTS foram resolvidas para COM+. para obter mais informações, consulte [suporte à depuração de Visual Basic COM+ em contraste com o MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de erros no COM+](handling-errors-in-com-.md)
</dt> </dl>

 

 



