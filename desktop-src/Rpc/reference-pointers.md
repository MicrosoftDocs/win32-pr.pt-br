---
title: Ponteiros de referência
description: Ponteiros de referência são os ponteiros mais simples e exigem a menor quantidade de processamento pelo stub do cliente.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6338b1017f05bdf004fee2b288c4eae1ee9775eaa2ad225d5f4b6afa3e74d8ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927027"
---
# <a name="reference-pointers"></a>Ponteiros de referência

Ponteiros de referência são os ponteiros mais simples e exigem a menor quantidade de processamento pelo stub do cliente. Quando um programa cliente passa um ponteiro de referência para um procedimento remoto, o ponteiro de referência sempre contém o endereço de um bloco de memória válido. Ele ainda estará apontando para o mesmo bloco de memória quando o procedimento remoto for concluído. Esses ponteiros são usados principalmente para implementar semânticas de referência e para permitir \[ parâmetros de [**saída**](/windows/desktop/Midl/out-idl) \] em C.

No exemplo a seguir, o valor do ponteiro não é alterado durante a chamada, embora o conteúdo dos dados no endereço indicado pelo ponteiro possa ser alterado.

![alteração de dados em um endereço de ponteiro de referência estática](images/prog-a07.png)

Um ponteiro de referência tem as seguintes características:

-   Ele sempre aponta para um armazenamento válido e nunca tem o valor **NULL**.
-   Ele nunca muda durante uma chamada e sempre aponta para o mesmo armazenamento antes e depois da chamada.
-   Os dados retornados do procedimento remoto são gravados no armazenamento existente.
-   O armazenamento apontado por um ponteiro de referência não pode ser acessado por nenhum outro ponteiro ou por qualquer outro nome na função.

Use o \[ [](/windows/desktop/Midl/ref) \] atributo ref para especificar ponteiros de referência em definições de interface, conforme mostrado no exemplo a seguir.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

Este exemplo define o parâmetro *pChar* como um ponteiro para um único caractere, não uma matriz de caracteres. É um parâmetro \[ **out** \] e um ponteiro de referência que aponta para a memória que a rotina de servidor RemoteFn preencherá com os dados.

 

 