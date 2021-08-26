---
title: Combinando parâmetros pipe e nonpipe
description: Combinando parâmetros de pipe e nonpipe na RPC (Chamada de Procedimento Remoto).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76bc2f334325c87cbf8c4a09898cf0fe54153cd84f6f2809995e66cc08e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022666"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinando parâmetros pipe e nonpipe

Quando você combina tipos de pipe e outros tipos em uma chamada de procedimento remoto, os dados são transmitidos de acordo com a direção do parâmetro:

-   Na **\[ direção, os \]** dados de todos os argumentos de não gaita são transmitidos primeiro, seguidos pelos dados de pipe.
-   Na direção **\[ de saída, \]** o servidor envia os dados de pipe primeiro. Depois que a rotina do gerenciador é retornada, o servidor transmite os dados de nãopipe.
-   Quando há **\[ argumentos \] in,out** pipe combinados com argumentos **\[ in,out \]** não pipe, primeiro os dados de entrada são transmitidos em sua totalidade, conforme descrito anteriormente. Em seguida, os dados de saída são transmitidos conforme descrito anteriormente.

A restrição a seguir se aplica a essa implementação (MIDL 3.0) de pipes: quando você combina tipos de pipe e outros tipos em uma única chamada de procedimento remoto, os parâmetros de nãopipe devem ter um tamanho bem definido para permitir que o compilador MIDL calcule o tamanho do buffer necessário. Por exemplo, você não pode combinar parâmetros de pipe com um ponteiro exclusivo ou uma estrutura compatível, pois seus tamanhos não podem ser \[ [](/windows/desktop/Midl/unique) \] determinados no tempo de compilação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tubo](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 