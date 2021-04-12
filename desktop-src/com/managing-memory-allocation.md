---
title: Gerenciando a alocação de memória
description: Gerenciando a alocação de memória
ms.assetid: 8a189fe8-5555-44bb-968b-04408fa7fce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2af04b4ecc5b8480230b17ae710b84ce8e6ce5d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366787"
---
# <a name="managing-memory-allocation"></a>Gerenciando a alocação de memória

No COM, muitos, se não a maioria, os métodos de interface são chamados pelo código escrito por uma organização de programação e implementados pelo código escrito por outro. Muitos dos parâmetros e valores de retorno dessas funções são de tipos que podem ser transmitidos por valor. Às vezes, no entanto, é necessário passar estruturas de dados para as quais esse não é o caso, portanto, é necessário para o chamador e chamado ter uma política de alocação e desalocação compatível. COM define uma convenção universal para alocação de memória, porque ela é mais razoável do que definir regras de caso por caso e para que a implementação de chamada de procedimento remoto COM possa gerenciar corretamente a memória.

Os métodos de uma interface COM sempre fornecem gerenciamento de memória de ponteiros para a interface chamando as funções [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) encontradas na interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , da qual todas as outras interfaces com derivam. (Consulte [regras para gerenciar contagens de referência](rules-for-managing-reference-counts.md) para obter mais informações.)

Esta seção descreve apenas como alocar memória para parâmetros que não são passados por valor — não ponteiros para interfaces, mas coisas mais comunss, como cadeias de caracteres, ponteiros para estruturas e assim por diante.

Para mais informações, consulte os seguintes tópicos:

-   [O alocador de memória OLE](the-ole-memory-allocator.md)
-   [Regras de gerenciamento de memória](memory-management-rules.md)
-   [Depurando alocações de memória](debugging-memory-allocations.md)

 

 