---
title: Classes, objetos e interfaces
description: Classes, objetos e interfaces
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54008f316103a8a113e6702e4a4b1192bc0576f5a61fb28b38dbe2502bae881b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786176"
---
# <a name="classes-objects-and-interfaces"></a>Classes, objetos e interfaces

Na linguagem de programação C++, uma *classe* consiste em *Propriedades* (ou dados de membros) e *métodos* (ou funções de membro). As propriedades são elementos de dados, como os contidos em uma estrutura. Os métodos são usados para uma variedade de finalidades, como inicialização, atribuição, operações e acesso a dados. Você usa uma declaração de classe da mesma maneira que usa uma declaração de estrutura. A memória é alocada para uma classe quando você define um *objeto* de classe. Cada objeto de classe tem uma área de dados para suas propriedades e uma tabela de ponteiros para os métodos aos quais ele dá suporte.

No OLE, um objeto consiste em dados e métodos, como acontece em C++. No entanto, um objeto OLE segue regras mais rígidas. Os dados são estritamente internos. Um objeto expõe apenas interfaces. Uma *interface* é um conjunto de métodos relacionados para um objeto. Cada objeto pode dar suporte a várias interfaces. Todas as interfaces OLE dão suporte à interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

 

 




