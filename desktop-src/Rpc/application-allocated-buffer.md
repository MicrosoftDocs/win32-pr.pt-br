---
title: Buffer de Application-Allocated
description: O atributo de ACF \ \_ contagem de bytes \ instrui os stubs a usar um buffer pré-alocado que não está alocado ou liberado pelas rotinas de suporte do cliente.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454264"
---
# <a name="application-allocated-buffer"></a>Buffer de Application-Allocated

A contagem de \[ [**bytes \_**](/windows/desktop/Midl/byte-count) do atributo ACF \] direciona os stubs para usar um buffer pré-alocado que não está alocado ou liberado pelas rotinas de suporte do cliente. O \[ **atributo \_ contagem de bytes** \] é aplicado a um parâmetro de ponteiro ou de matriz que aponta para o buffer. Ele requer um parâmetro que especifica o tamanho do buffer em bytes.

A área de memória alocada pelo cliente pode conter estruturas de dados complexas com vários ponteiros. Como a área de memória é contígua, o aplicativo não precisa fazer várias chamadas para liberar cada ponteiro e estrutura individualmente. Como ao usar o \[ atributo [**ALLOCATE (todos os \_ nós)**](/windows/desktop/Midl/allocate) \] , a área de memória pode ser alocada ou liberada com uma chamada para a rotina de alocação de memória ou a rotina gratuita. No entanto, ao contrário do uso do \[ atributo **ALLOCATE (todos os \_ nós)** \] , o parâmetro buffer não é gerenciado pelo stub do cliente, mas pelo aplicativo cliente.

O buffer deve ser um \[ [](/windows/desktop/Midl/out-idl) \] parâmetro somente out e o comprimento do buffer em bytes deve ser um \[ [](/windows/desktop/Midl/in) \] parâmetro somente no. O \[ [**atributo \_ contagem de bytes**](/windows/desktop/Midl/byte-count) \] só pode ser aplicado a tipos de ponteiro. O \[ atributo ACF de **\_ contagem de bytes** \] é uma extensão da Microsoft para o DCE IDL e, dessa forma, não estará disponível se você compilar usando a opção MIDL [**/OSF**](/windows/desktop/Midl/-osf)

No exemplo a seguir, o parâmetro *pRoot* usa contagem de bytes:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

O \[ [**atributo \_ contagem de bytes**](/windows/desktop/Midl/byte-count) \] aparece no ACF como:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

O stub do cliente gerado a partir desses arquivos IDL e ACF não aloca ou libera a memória para esse buffer. O stub do servidor aloca e libera o buffer em uma única chamada usando o parâmetro de tamanho fornecido. Se os dados forem muito grandes para o tamanho de buffer especificado, uma exceção será gerada.

 

 