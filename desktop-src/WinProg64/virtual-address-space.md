---
title: Espaço de Endereço Virtual (Guia de Programação para Windows)
description: Por padrão, os aplicativos baseados em Windows Microsoft de 64 bits têm um espaço de endereço no modo de usuário de vários terabytes.
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- Guia de programação Windows de 64 Windows de 64 bits, espaço de endereço virtual
- espaço de endereço virtual de 64 bits Windows Programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2e673befb66c45501558effb37f3d04ee1a99199010f8cca89abb2cb31c6d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113366"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>Espaço de Endereço Virtual (Guia de Programação para Windows)

Por padrão, os aplicativos baseados em Windows Microsoft de 64 bits têm um espaço de endereço no modo de usuário de vários terabytes. Para valores precisos, consulte [Limites de memória para Windows e Windows Server Releases](/windows/desktop/Memory/memory-limits-for-windows-releases). No entanto, os aplicativos podem especificar que o sistema deve alocar toda a memória para o aplicativo abaixo de 2 gigabytes. Esse recurso é benéfico para aplicativos de 64 bits se as seguintes condições são verdadeiras:

-   Um espaço de endereço de 2 GB é suficiente.
-   O código tem muitos avisos de truncamento de ponteiro.
-   Ponteiros e inteiros são livremente mistos.
-   O código tem polimorfismo usando tipos de dados de 32 bits.

Todos os ponteiros ainda são ponteiros de 64 bits, mas o sistema garante que cada alocação de memória ocorra abaixo do limite de 2 GB, de modo que, se o aplicativo truncar um ponteiro, nenhum dado significativo será perdido. Os ponteiros podem ser truncados para valores de 32 bits e, em seguida, estendidos para valores de 64 bits por extensão de sinal ou extensão zero.

Para especificar essa limitação de memória, use **a opção de vinculador /LARGEADDRESSAWARE:NO.** Observe que **/LARGEADDRESSAWARE:NO** é ignorado para um binário ARM64. No entanto, esteja ciente de que podem ocorrer problemas ao usar essa opção. Se você criar uma DLL que usa essa opção e a DLL for chamada por um aplicativo que não usa essa opção, a DLL poderá truncar um ponteiro de 64 bits cujos 32 bits superiores são significativos. Isso pode causar falha do aplicativo sem nenhum aviso.

 

 
