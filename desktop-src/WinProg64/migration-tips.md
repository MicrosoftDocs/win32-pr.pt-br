---
title: Dicas de migração
description: É importante considerar os cálculos de endereço e a aritmética de ponteiro ao portar seu código para o Windows de 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- Guia de programação do Windows de 64 bits-programação do Windows de 64 bits, dicas de migração
- Dicas de migração-programação do Windows de 64 bits
- compatibilidade 64-programação do Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5236012b84ee880b53f8d7e50b01694181e71112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636305"
---
# <a name="migration-tips"></a>Dicas de migração

As duas áreas principais de preocupação ao examinar seu código para a compatibilidade de 64 bits são as seguintes:

-   Cálculos de endereço
-   Aritmética do ponteiro

Por muitos motivos, os desenvolvedores armazenavam endereços como um valor **ULONG** . Afinal, no Windows de 32 bits, um endereço, um ponteiro e um valor **ULONG** são todos 32 bits de comprimento. No entanto, no Windows de 64 bits, um endereço e um **ULONG** não têm o mesmo comprimento. Embora um **ULONG** permaneça um valor de 32 bits, todos os ponteiros agora são valores de 64 bits.

## <a name="in-this-section"></a>Nesta seção

-   [Diretrizes gerais de portabilidade](general-porting-guidelines.md)
-   [Armazenando um valor de 64 bits](storing-a-64-bit-value.md)
-   [Erros comuns do compilador](common-compiler-errors.md)
-   [Considerações adicionais](additional-considerations.md)

 

 




