---
title: Combinando parâmetros de pipe e nonpipe
description: Combinando parâmetros de pipe e nonpipe na chamada de procedimento remoto (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823914"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinando parâmetros de pipe e nonpipe

Quando você combina tipos de pipe e outros tipos em uma chamada de procedimento remoto, os dados são transmitidos de acordo com a direção do parâmetro:

-   Na direção **\[ in \]** , os dados de todos os argumentos de não-pipe são transmitidos primeiro, seguidos por dados de pipe.
-   Na direção de **\[ saída \]** , o servidor envia os dados do pipe primeiro. Depois que a rotina Manager é retornada, o servidor transmite os dados sem pipe.
-   Quando há argumentos **\[ de pipe in \] , out** combinados com argumentos **\[ in, \] out** non-pipe, primeiro os dados de entrada são transmitidos em sua totalidade, conforme descrito anteriormente. Em seguida, os dados de saída são transmitidos conforme descrito anteriormente.

A seguinte restrição se aplica a esta implementação de Pipes (MIDL 3,0): quando você combina tipos de pipe e outros tipos em uma única chamada de procedimento remoto, os parâmetros de não-pipe devem ter um tamanho bem definido para permitir que o compilador MIDL Calcule o tamanho de buffer necessário. Por exemplo, você não pode combinar parâmetros de pipe com um \[ [](/windows/desktop/Midl/unique) \] ponteiro exclusivo ou uma estrutura compatível, já que seus tamanhos não podem ser determinados no tempo de compilação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 