---
title: Dicas de migração
description: É importante considerar os cálculos de endereço e a aritmética de ponteiro ao portar seu código para Windows de 64 bits.
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- guia de programação de Windows de 64 bits 64 – programação de Windows de bits, dicas de migração
- dicas de migração 64-bit Windows programação
- compatibilidade 64-bit Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee1480bec99bdc3b620d5d349343330aa3c34121ff697d5e8b15497c72baedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743591"
---
# <a name="migration-tips"></a>Dicas de migração

As duas áreas principais de preocupação ao examinar seu código para a compatibilidade de 64 bits são as seguintes:

-   Cálculos de endereço
-   Aritmética do ponteiro

Por muitos motivos, os desenvolvedores armazenavam endereços como um valor **ULONG** . afinal, no Windows de 32 bits, um endereço, um ponteiro e um valor **ULONG** são todos 32 bits de comprimento. no entanto, no Windows de 64 bits, um endereço e um **ULONG** não têm o mesmo comprimento. Embora um **ULONG** permaneça um valor de 32 bits, todos os ponteiros agora são valores de 64 bits.

## <a name="in-this-section"></a>Nesta seção

-   [Diretrizes gerais de portabilidade](general-porting-guidelines.md)
-   [Armazenando um valor de 64 bits](storing-a-64-bit-value.md)
-   [Erros comuns do compilador](common-compiler-errors.md)
-   [Considerações adicionais](additional-considerations.md)

 

 




