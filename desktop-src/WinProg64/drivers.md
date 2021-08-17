---
title: Drivers (Guia de Programação para Windows)
description: A versão de 64 bits do Windows foi projetada para tornar possível que os desenvolvedores usem uma única base de código-fonte para seus aplicativos de 32 bits e 64 bits. Em grande parte, isso também é verdadeiro para drivers de Windows de 32 bits e 64 bits.
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- drivers de programação Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cda928bbfc8c7f83e3aeac0bacbaea1e1a46214d9c0785d4675a3042b87fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132849"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>Drivers (Guia de Programação para Windows)

A versão de 64 bits do Windows foi projetada para tornar possível que os desenvolvedores usem uma única base de código-fonte para seus aplicativos de 32 bits e 64 bits. Em grande parte, isso também é verdadeiro para drivers de Windows de 32 bits e 64 bits.

No entanto, drivers de 32 bits não podem ser executados em Windows de 64 bits e devem ser portados. Para aplicativos de modo de usuário, o Windows de 64 bits inclui o WOW64, que permite que aplicativos Windows de 32 bits executem (com alguma perda de desempenho) em sistemas que executam Windows de 64 bits. Não existe nenhuma camada de conversão equivalente para drivers.

Para obter informações sobre como portar drivers para Windows de 64 bits, consulte Problemas de [64](https://msdn.microsoft.com/library/aa489627.aspx) bits no WDK (Kit de Driver do Windows).

 

 




