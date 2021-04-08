---
title: Espaço de endereço virtual (guia de programação para Windows de 64 bits)
description: Por padrão, aplicativos baseados no Microsoft Windows de 64 bits têm um espaço de endereço de modo de usuário de vários terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, espaço de endereço virtual
- espaço de endereço virtual programação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e4aa6eb67ebf931d1152b3a1101df2757e899b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008670"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Espaço de endereço virtual (guia de programação para Windows de 64 bits)

Por padrão, aplicativos baseados no Microsoft Windows de 64 bits têm um espaço de endereço de modo de usuário de vários terabytes. Para obter valores precisos, consulte [limites de memória para versões do Windows e do Windows Server](/windows/desktop/Memory/memory-limits-for-windows-releases). No entanto, os aplicativos podem especificar que o sistema deve alocar toda a memória para o aplicativo abaixo de 2 gigabytes. Esse recurso é benéfico para aplicativos de 64 bits se as seguintes condições forem verdadeiras:

-   Um espaço de endereço de 2 GB é suficiente.
-   O código tem muitos avisos de truncamento de ponteiro.
-   Ponteiros e inteiros são misturados livremente.
-   O código tem polimorfismo usando tipos de dados de 32 bits.

Todos os ponteiros ainda são ponteiros de 64 bits, mas o sistema garante que cada alocação de memória ocorra abaixo do limite de 2 GB, de modo que, se o aplicativo truncar um ponteiro, nenhum dado significativo será perdido. Os ponteiros podem ser truncados para valores de 32 bits e estendidos para valores de 64 bits por extensão de assinatura ou extensão zero.

Para especificar essa limitação de memória, use a opção **/LARGEADDRESSAWARE: no** linker. Observe que **/LARGEADDRESSAWARE: no** é ignorado para um binário ARM64. No entanto, lembre-se de que podem ocorrer problemas ao usar essa opção. Se você criar uma DLL que usa essa opção e a DLL for chamada por um aplicativo que não usa essa opção, a DLL poderá truncar um ponteiro de 64 bits cujos bits superiores 32 sejam significativos. Isso pode causar falha no aplicativo sem nenhum aviso.

 

 
