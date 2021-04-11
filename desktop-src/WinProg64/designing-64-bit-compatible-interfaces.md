---
title: Criando interfaces compatíveis com 64 bits
description: Problemas de compatibilidade com versões anteriores surgem quando você adiciona novos tipos de dados ou métodos a uma interface, altera tipos de dados antigos ou usa tipos de dados inadequadamente.
ms.assetid: 676affd8-a155-4ac2-9647-0c7352c87a31
keywords:
- compatibilidade com versões anteriores programação de 64 bits do Windows
- interfaces compatíveis com 64 bits – programação de 64 bits do Windows
- Guia de programação do Windows de 64 bits, programação do Windows de 64 bits, compatibilidade
- compatibilidade 64-programação do Windows de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebcde0e621d35cf216c2191f2e4b7da624dc274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292142"
---
# <a name="designing-64-bit-compatible-interfaces"></a>Criando interfaces compatíveis com 64 bits

A portabilidade de janelas de 32 bits para o Windows de 64 bits não deve, por si só, criar problemas para aplicativos distribuídos, se eles usam RPC (chamadas de procedimento remoto) diretamente ou por DCOM. O modelo de programação RPC especifica os tamanhos de dados e tipos inteiros bem definidos que têm o mesmo tamanho em cada extremidade da conexão. Além disso, no modelo de dados abstrato LLP64 desenvolvido para o Windows de 64 bits, somente os ponteiros se expandem para 64 bits – todos os outros tipos de dados inteiros permanecem 32 bits. Como os ponteiros são locais para cada lado da conexão de cliente/servidor e geralmente são transmitidos como marcadores **nulos** ou não **nulos** , o mecanismo de marshaling pode manipular diferentes tamanhos de ponteiro em qualquer extremidade de uma conexão de forma transparente.

No entanto, problemas de compatibilidade com versões anteriores surgem quando você adiciona novos tipos de dados ou métodos a uma interface, altera tipos de dados antigos ou usa tipos de dados inadequadamente. Os tópicos a seguir discutem como evitar essas situações (quando possível) e como criar soluções alternativas robustas quando não é possível evitá-las.

## <a name="in-this-section"></a>Nesta seção

-   [Alterando uma interface existente](changing-an-existing-interface.md)
-   [Evitando a ocultação de informações](avoiding-information-hiding.md)
-   [Evitando o polimorfismo](avoiding-polymorphism.md)
-   [Usando novos tipos de dados em seu arquivo IDL](using-new-data-types-in-your-idl-file.md)
-   [Preparando seu aplicativo para o Windows de 64 bits](preparing-your-application-for-64-bit-windows.md)

## <a name="related-sections"></a>Seções relacionadas

Se você ainda não estiver familiarizado com os novos tipos de dados, o ambiente de trabalho e as alterações de API para o Windows de 64 bits, consulte [preparando-se para o Windows de 64 bits](getting-ready-for-64-bit-windows.md).

 

 




