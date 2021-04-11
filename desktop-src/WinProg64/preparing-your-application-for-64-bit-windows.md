---
title: Preparando seu aplicativo para o Windows de 64 bits
description: Há vários recursos que facilitam o desenvolvimento de aplicativos que serão executados em janelas de 32 e 64 bits. A maioria deles, como os novos tipos de dados, é descrita em preparando-se para o Windows de 64 bits.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Kit de ferramentas de 64 bits 64-programação do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76f3b40d2fb22b84abdd4322f476981dc54c7ad3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162387"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Preparando seu aplicativo para o Windows de 64 bits

Há vários recursos que facilitam o desenvolvimento de aplicativos que serão executados em janelas de 32 e 64 bits. A maioria deles, como os novos tipos de dados, é descrita em [preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md).

O kit de ferramentas de 64 bits fornecido com o SDK do Windows inclui um compilador de MIDL de 64 bits, Midl.exe, para gerar stubs de 64 bits nativos, bem como stubs de 32 bits. Use a opção **/env Win64** para gerar somente stubs de 64 bits. O padrão é gerar stubs duplos que são executados em ambas as plataformas.

Observe que o MIDL de 64 bits dá suporte apenas aos modos de otimização [**/Oicf**](/windows/desktop/Midl/-oi) e [**/os**](/windows/desktop/Midl/-os) .

 

 