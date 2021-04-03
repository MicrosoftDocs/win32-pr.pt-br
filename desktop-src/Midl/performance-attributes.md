---
title: Atributos de desempenho
description: Use os seguintes atributos em um arquivo IDL para reduzir o tamanho do código stub ou melhorar o desempenho.
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- MIDL, atributos, desempenho de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbfa518b400d237c9fd3789f61b7e74a0c38276
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006157"
---
# <a name="performance-attributes"></a>Atributos de desempenho

Use os seguintes atributos em um arquivo IDL para reduzir o tamanho do código stub ou melhorar o desempenho.



| Atributo                             | Uso                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ignorar**](ignore.md)              | Designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não sejam transmitidos.                        |
| [**local**](local.md)                | Designa uma função que é local para o aplicativo para o qual MIDL não precisa gerar código stub.                                           |
| [**\_marshaling de transmissão**](wire-marshal.md) | Define um tipo de dados como um tipo mais simples para transmissão em uma rede e permite que você implemente rotinas de marshaling e desempacotamento para o tipo. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de ACF de gerenciamento de memória](memory-management-acf-attributes.md)
</dt> <dt>

[Atributos de ACF de otimização de stub](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




