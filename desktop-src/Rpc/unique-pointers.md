---
title: Ponteiros exclusivos
description: Em programas em C, mais de um ponteiro pode conter o endereço dos dados.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3adb39d2505daa623f23f47c936fb73d0ecff6e0ad7749c951f9926fd66f33d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010984"
---
# <a name="unique-pointers"></a>Ponteiros exclusivos

Em programas em C, mais de um ponteiro pode conter o endereço dos dados. Os ponteiros são considerados para criar um [*alias*](a-glos.md) para os dados. Os aliases também são criados quando os ponteiros apontam para variáveis declaradas. O fragmento de código a seguir ilustra os dois métodos de alias:


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



Em um programa típico do C, você pode especificar uma árvore binária usando a seguinte definição:


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



Mais de um ponteiro pode acessar o conteúdo de um nó de árvore. Isso geralmente é bom para aplicativos não distribuídos. No entanto, esse estilo de programação gera um código de suporte de RPC mais complicado. Os stubs de cliente e servidor exigem o código adicional para gerenciar os dados e os ponteiros. O código stub subjacente deve resolver os vários ponteiros para os endereços e determinar qual cópia dos dados representa a versão mais recente.

A quantidade de processamento pode ser reduzida se você garantir que o ponteiro seja a única maneira como o aplicativo pode acessar essa área de memória. O ponteiro ainda pode ter muitos dos recursos de um ponteiro de C. Por exemplo, ele pode mudar entre valores **nulos** e não **nulos** ou permanecer o mesmo. O exemplo a seguir ilustra essa situação. O ponteiro é **nulo** antes da chamada e aponta para uma cadeia de caracteres válida após a chamada:

![ponteiro mudando entre valores nulos e não nulos](images/prog-a01.png)

Por padrão, o compilador MIDL aplica o \[ [](/windows/desktop/Midl/unique) \] atributo de ponteiro exclusivo a todos os ponteiros que não são parâmetros. Essa configuração padrão pode ser alterada com o \[ [atributo \_ padrão de ponteiro](/windows/desktop/Midl/pointer-default) \] .

Um ponteiro exclusivo tem as seguintes características:

-   Ele pode ter o valor **NULL**.
-   Ele pode mudar de **nulo** para não **nulo** durante a chamada. Quando o valor muda para não **nulo**, a nova memória é alocada no retorno.
-   Ele pode mudar de não **nulo** para **nulo** durante a chamada. Quando o valor é alterado para **NULL**, o aplicativo é responsável por liberar a memória.
-   O valor pode ser alterado de um valor não **nulo** para outro.
-   O armazenamento que um ponteiro exclusivo aponta para não pode ser acessado por nenhum outro ponteiro ou nome na operação.
-   Os dados de retorno são gravados no armazenamento existente se o ponteiro não tiver o valor **NULL**.

O exemplo a seguir demonstra como definir um ponteiro exclusivo.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, unique] char *ach);
}
```

Neste exemplo, o parâmetro *ach* é um ponteiro exclusivo para dados de caractere que é enviado a um servidor para ser processado com a rotina RemoteFn.

 

 