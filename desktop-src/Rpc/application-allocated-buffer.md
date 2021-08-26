---
title: Application-Allocated buffer
description: O atributo ACF \ contagem de byte\ direciona os stubs para usar um buffer pré-alocado que não é alocado ou liberado pelas rotinas de suporte \_ ao cliente.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb87390637cba57cbdf4021a43f4ec98ea64c3828c67dfdb615ffcd62dc8c16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024176"
---
# <a name="application-allocated-buffer"></a>Application-Allocated buffer

A contagem de byte do atributo ACF direciona os stubs para usar um buffer pré-alocado que não é alocado ou liberado pelas rotinas de suporte \[ [**\_**](/windows/desktop/Midl/byte-count) \] ao cliente. O \[ **atributo de contagem \_ de** \] byte é aplicado a um ponteiro ou parâmetro de matriz que aponta para o buffer. Ele requer um parâmetro que especifica o tamanho do buffer em bytes.

A área de memória alocada pelo cliente pode conter estruturas de dados complexas com vários ponteiros. Como a área de memória é contígua, o aplicativo não precisa fazer várias chamadas para liberar cada ponteiro e estrutura individualmente. Assim como ao usar o atributo \[ [**allocate(all \_ nodes),**](/windows/desktop/Midl/allocate) a área de memória pode ser alocada ou liberada com uma chamada para a rotina de alocação de memória ou a \] rotina livre. No entanto, ao contrário de usar o atributo \[ **allocate (todos os \_ nós),** o parâmetro de buffer não é gerenciado pelo stub do cliente, \] mas pelo aplicativo cliente.

O buffer deve ser um parâmetro somente saída e o comprimento do buffer em \[ [](/windows/desktop/Midl/out-idl) \] bytes deve ser \[ [**um parâmetro em**](/windows/desktop/Midl/in) \] -only. O \[ [**atributo de contagem \_ de**](/windows/desktop/Midl/byte-count) \] byte só pode ser aplicado a tipos de ponteiro. O atributo ACF de contagem de byte é uma extensão da Microsoft para ADL de DCE e, como tal, não estará disponível se você compilar usando a opção \[ **\_** \] MIDL [**/osf.**](/windows/desktop/Midl/-osf)

No exemplo a seguir, o parâmetro *pRoot* usa a contagem de byte:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

O \[ [**atributo de \_ contagem**](/windows/desktop/Midl/byte-count) \] de byte aparece no ACF como:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

O stub de cliente gerado com esses arquivos IDL e ACF não aloca nem libera a memória para esse buffer. O stub do servidor aloca e libera o buffer em uma única chamada usando o parâmetro de tamanho fornecido. Se os dados são muito grandes para o tamanho do buffer especificado, uma exceção é criada.

 

 