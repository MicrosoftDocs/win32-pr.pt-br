---
title: Drivers (guia de programação para o Windows de 64 bits)
description: A versão de 64 bits do Windows foi projetada para possibilitar que os desenvolvedores usem uma base de código-fonte única para seus aplicativos de 32 bits e de 64 bits. Para uma grande extensão, isso também é verdadeiro para drivers do Windows de 32 bits e 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- drivers de programação de 64 bits do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6843a4efbb68652bf269c819c3a11ba102521318
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294726"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Drivers (guia de programação para o Windows de 64 bits)

A versão de 64 bits do Windows foi projetada para possibilitar que os desenvolvedores usem uma base de código-fonte única para seus aplicativos de 32 bits e de 64 bits. Para uma grande extensão, isso também é verdadeiro para drivers do Windows de 32 bits e 64 bits.

No entanto, os drivers de 32 bits não podem ser executados em janelas de 64 bits e devem ser portados. Para aplicativos de modo de usuário, o Windows de 64 bits inclui o WOW64, que permite que aplicativos do Windows de 32 bits sejam executados (com alguma perda de desempenho) em sistemas que executam o Windows de 64 bits. Não existe nenhuma camada de conversão equivalente para os drivers.

Para obter informações sobre como portar drivers para o Windows de 64 bits, consulte [problemas de 64 bits](https://msdn.microsoft.com/library/aa489627.aspx) no WDK (Kit de driver do Windows).

 

 




