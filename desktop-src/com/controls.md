---
title: Controls (COM)
description: Controles
ms.assetid: 73947c81-6727-4112-9da0-efa60360f458
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f440fff8f855f70c1a5ab3df78a6f6f6ed365ea
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294683"
---
# <a name="controls-com"></a>Controls (COM)

Um controle ActiveX é, na verdade, apenas outro termo para objeto OLE ou, mais especificamente, objeto COM. Em outras palavras, um controle, na pior das hipóteses, é um objeto COM que dá suporte à interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e também o registro em si. Por meio de [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) , um contêiner pode gerenciar o tempo de vida do controle, bem como descobrir dinamicamente a extensão completa da funcionalidade de um controle com base nas interfaces disponíveis. Isso permite que um controle implemente o mínimo de funcionalidade que ele precisa para, em vez de dar suporte a um grande número de interfaces que, na verdade, não fazem nada. Em suma, esse requisito mínimo para nada mais que **IUnknown** permite que qualquer controle seja tão leve quanto possível.

Em suma, além de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e Autoregistro, não há nenhum outro requisito para um controle. No entanto, há convenções que devem ser seguidas sobre o que o suporte de uma interface significa em termos de funcionalidade fornecida ao contêiner pelo controle. Em seguida, esta seção descreve o que significa para um controle para realmente dar suporte a uma interface, bem como métodos, propriedades e eventos que um controle deve fornecer como uma linha de base, se houver ocasiões para dar suporte a métodos, propriedades e eventos.

Para mais informações, consulte os seguintes tópicos:

-   [Registro automático para controles](self-registration-for-controls.md)
-   [O que é o suporte para uma interface significa](what-support-for-an-interface-means.md)
-   [Interfaces de persistência](persistence-interfaces.md)
-   [Métodos opcionais em interfaces de controle](optional-methods-in-control-interfaces.md)
-   [Opções de fábrica de classes](class-factory-options.md)
-   [Expondo Propriedades por meio de IDispatch](properties.md)
-   [Expondo métodos por meio de IDispatch](exposing-methods-through-idispatch.md)
-   [Eventos em controles](events-in-controls.md)
-   [Páginas de propriedade](property-pages.md)
-   [Propriedades de ambiente para controles](ambient-properties-for-controls.md)
-   [Usando a funcionalidade do contêiner](using-the-container-s-functionality.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretrizes de contêiner de controle e controle ActiveX](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 




