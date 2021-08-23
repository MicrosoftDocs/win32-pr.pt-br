---
description: Um manipulador de terminação garante que um bloco específico de código seja executado sempre que o fluxo de controle deixar um corpo de código protegido em particular. Um manipulador de encerramento consiste nos seguintes elementos.
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: Tratamento de encerramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23e2c81465ab9d469d3d5c503c12f5bf1c7a333507d302f3e5639e0158834e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292950"
---
# <a name="termination-handling"></a>Tratamento de encerramento

Um *manipulador de terminação* garante que um bloco específico de código seja executado sempre que o fluxo de controle deixar um corpo de código protegido em particular. Um manipulador de encerramento consiste nos seguintes elementos.

-   Um corpo de código protegido
-   Um bloco de código de término a ser executado quando o fluxo de controle deixa o corpo protegido

Os manipuladores de terminação são declarados na sintaxe específica do idioma. Usando o compilador de otimização do Microsoft C/C++, eles são implementados usando **\_ \_ try** e **\_ \_ finally**. Para obter mais informações, consulte [sintaxe do manipulador](handler-syntax.md).

O corpo de código protegido pode ser um bloco de código, um conjunto de blocos aninhados ou um procedimento ou uma função inteira. Sempre que o corpo protegido for executado, o bloco de código de encerramento será executado. A única exceção a isso é quando o thread é encerrado durante a execução do corpo protegido (por exemplo, se a função [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) ou [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) for chamada de dentro do corpo protegido).

O bloco de terminação é executado quando o fluxo de controle deixa o corpo protegido, independentemente de o corpo protegido ser encerrado normalmente ou de forma anormal. O corpo protegido é considerado como encerrado normalmente quando a última instrução no bloco é executada e o controle prossegue em sequência no bloco de terminação. A finalização anormal ocorre quando o fluxo de controle deixa o corpo protegido devido a uma exceção, ou devido a uma instrução de controle como **Return**, **goto**, **Break** ou **continue**. A função [**AbnormalTermination**](abnormaltermination.md) pode ser chamada de dentro do bloco de terminação para determinar se o corpo protegido foi encerrado normalmente.

 

 
