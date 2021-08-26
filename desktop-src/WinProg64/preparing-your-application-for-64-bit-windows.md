---
title: Preparando seu aplicativo para aplicativos de 64 bits Windows
description: Há vários recursos que facilitam o desenvolvimento de aplicativos que serão executados em 32 e 64 bits Windows. A maioria deles, como os novos tipos de dados, é descrita em Preparando-se para 64 bits Windows.
ms.assetid: 6559b0ab-17cf-4bec-bf2d-3a0da0a344d3
keywords:
- Programação do kit de ferramentas de 64 bits Windows 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b6c8d31b685e6f545aca4bdaac341fe25a3c96f458048808536899a8416120a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071616"
---
# <a name="preparing-your-application-for-64-bit-windows"></a>Preparando seu aplicativo para aplicativos de 64 bits Windows

Há vários recursos que facilitam o desenvolvimento de aplicativos que serão executados em 32 e 64 bits Windows. A maioria deles, como os novos tipos de dados, é descrita em [Preparando-se para 64 bits Windows](getting-ready-for-64-bit-windows.md).

O kit de ferramentas de 64 bits que acompanha o SDK do Windows inclui um compilador MIDL de 64 bits, Midl.exe, para gerar stubs nativos de 64 bits, bem como stubs de 32 bits. Use a **opção /env win64** para gerar apenas stubs de 64 bits. O padrão é gerar stubs duplos que são executados em ambas as plataformas.

Observe que o MIDL de 64 bits dá suporte apenas aos [**modos de otimização /Oicf**](/windows/desktop/Midl/-oi) e [**/Os.**](/windows/desktop/Midl/-os)

 

 