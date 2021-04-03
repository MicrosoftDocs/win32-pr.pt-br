---
title: Ponteiros exclusivos
description: Em programas em C, mais de um ponteiro pode conter o endereço dos dados.
ms.assetid: da4f466d-2c59-4e48-b6c5-1a49b933621a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf9a45965c82416ec838f8598c2796ba621a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007584"
---
# <a name="unique-pointers"></a><span data-ttu-id="be340-103">Ponteiros exclusivos</span><span class="sxs-lookup"><span data-stu-id="be340-103">Unique Pointers</span></span>

<span data-ttu-id="be340-104">Em programas em C, mais de um ponteiro pode conter o endereço dos dados.</span><span class="sxs-lookup"><span data-stu-id="be340-104">In C programs, more than one pointer can contain the address of data.</span></span> <span data-ttu-id="be340-105">Os ponteiros são considerados para criar um [*alias*](a-glos.md) para os dados.</span><span class="sxs-lookup"><span data-stu-id="be340-105">The pointers are said to create an [*alias*](a-glos.md) for the data.</span></span> <span data-ttu-id="be340-106">Os aliases também são criados quando os ponteiros apontam para variáveis declaradas.</span><span class="sxs-lookup"><span data-stu-id="be340-106">Aliases are also created when pointers point at declared variables.</span></span> <span data-ttu-id="be340-107">O fragmento de código a seguir ilustra os dois métodos de alias:</span><span class="sxs-lookup"><span data-stu-id="be340-107">The following code fragment illustrates both of these methods of aliasing:</span></span>


```C++
int iAnInteger=50;

// The next statement makes ipAnIntegerPointer an
// alias for iAnInteger.
int *ipAnIntegerPointer = &iAnInteger;

// This statement creates an alias for ipAnIntegerPointer.
int *ipAnotherIntegerPointer = ipAnIntegerPointer;
```



<span data-ttu-id="be340-108">Em um programa típico do C, você pode especificar uma árvore binária usando a seguinte definição:</span><span class="sxs-lookup"><span data-stu-id="be340-108">In a typical C program, you might specify a binary tree using the following definition:</span></span>


```C++
typedef struct _treetype 
{
    long               lValue;
    struct _treetype * left;
    struct _treetype * right;
} TREETYPE;

TREETYPE * troot;
```



<span data-ttu-id="be340-109">Mais de um ponteiro pode acessar o conteúdo de um nó de árvore.</span><span class="sxs-lookup"><span data-stu-id="be340-109">More than one pointer can access the contents of a tree node.</span></span> <span data-ttu-id="be340-110">Isso geralmente é bom para aplicativos não distribuídos.</span><span class="sxs-lookup"><span data-stu-id="be340-110">This is generally fine for nondistributed applications.</span></span> <span data-ttu-id="be340-111">No entanto, esse estilo de programação gera um código de suporte de RPC mais complicado.</span><span class="sxs-lookup"><span data-stu-id="be340-111">However, this style of programming generates more complicated RPC support code.</span></span> <span data-ttu-id="be340-112">Os stubs de cliente e servidor exigem o código adicional para gerenciar os dados e os ponteiros.</span><span class="sxs-lookup"><span data-stu-id="be340-112">The client and server stubs require the additional code to manage the data and the pointers.</span></span> <span data-ttu-id="be340-113">O código stub subjacente deve resolver os vários ponteiros para os endereços e determinar qual cópia dos dados representa a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="be340-113">The underlying stub code must resolve the various pointers to the addresses and determine which copy of the data represents the most recent version.</span></span>

<span data-ttu-id="be340-114">A quantidade de processamento pode ser reduzida se você garantir que o ponteiro seja a única maneira como o aplicativo pode acessar essa área de memória.</span><span class="sxs-lookup"><span data-stu-id="be340-114">The amount of processing can be reduced if you guarantee that your pointer is the only way the application can access that area of memory.</span></span> <span data-ttu-id="be340-115">O ponteiro ainda pode ter muitos dos recursos de um ponteiro de C.</span><span class="sxs-lookup"><span data-stu-id="be340-115">The pointer can still have many of the features of a C pointer.</span></span> <span data-ttu-id="be340-116">Por exemplo, ele pode mudar entre valores **nulos** e não **nulos** ou permanecer o mesmo.</span><span class="sxs-lookup"><span data-stu-id="be340-116">For example, it can change between **null** and non-**null** values or stay the same.</span></span> <span data-ttu-id="be340-117">O exemplo a seguir ilustra essa situação.</span><span class="sxs-lookup"><span data-stu-id="be340-117">The following example illustrates this.</span></span> <span data-ttu-id="be340-118">O ponteiro é **nulo** antes da chamada e aponta para uma cadeia de caracteres válida após a chamada:</span><span class="sxs-lookup"><span data-stu-id="be340-118">The pointer is **null** before the call and points to a valid string after the call:</span></span>

![ponteiro mudando entre valores nulos e não nulos](images/prog-a01.png)

<span data-ttu-id="be340-120">Por padrão, o compilador MIDL aplica o \[ [](/windows/desktop/Midl/unique) \] atributo de ponteiro exclusivo a todos os ponteiros que não são parâmetros.</span><span class="sxs-lookup"><span data-stu-id="be340-120">By default, the MIDL compiler applies the \[ [unique](/windows/desktop/Midl/unique)\] pointer attribute to all pointers that are not parameters.</span></span> <span data-ttu-id="be340-121">Essa configuração padrão pode ser alterada com o \[ [atributo \_ padrão de ponteiro](/windows/desktop/Midl/pointer-default) \] .</span><span class="sxs-lookup"><span data-stu-id="be340-121">This default setting can be changed with the \[ [pointer\_default](/windows/desktop/Midl/pointer-default)\] attribute.</span></span>

<span data-ttu-id="be340-122">Um ponteiro exclusivo tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="be340-122">A unique pointer has the following characteristics:</span></span>

-   <span data-ttu-id="be340-123">Ele pode ter o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="be340-123">It can have the value **null**.</span></span>
-   <span data-ttu-id="be340-124">Ele pode mudar de **nulo** para não **nulo** durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="be340-124">It can change from **null** to non-**null** during the call.</span></span> <span data-ttu-id="be340-125">Quando o valor muda para não **nulo**, a nova memória é alocada no retorno.</span><span class="sxs-lookup"><span data-stu-id="be340-125">When the value changes to non-**null**, new memory is allocated on return.</span></span>
-   <span data-ttu-id="be340-126">Ele pode mudar de não **nulo** para **nulo** durante a chamada.</span><span class="sxs-lookup"><span data-stu-id="be340-126">It can change from non-**null** to **null** during the call.</span></span> <span data-ttu-id="be340-127">Quando o valor é alterado para **NULL**, o aplicativo é responsável por liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="be340-127">When the value changes to **NULL**, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="be340-128">O valor pode ser alterado de um valor não **nulo** para outro.</span><span class="sxs-lookup"><span data-stu-id="be340-128">The value can change from one non-**null** value to another.</span></span>
-   <span data-ttu-id="be340-129">O armazenamento que um ponteiro exclusivo aponta para não pode ser acessado por nenhum outro ponteiro ou nome na operação.</span><span class="sxs-lookup"><span data-stu-id="be340-129">The storage that a unique pointer points to cannot be accessed by any other pointer or name in the operation.</span></span>
-   <span data-ttu-id="be340-130">Os dados de retorno são gravados no armazenamento existente se o ponteiro não tiver o valor **NULL**.</span><span class="sxs-lookup"><span data-stu-id="be340-130">Return data is written into existing storage if the pointer does not have the value **null**.</span></span>

<span data-ttu-id="be340-131">O exemplo a seguir demonstra como definir um ponteiro exclusivo.</span><span class="sxs-lookup"><span data-stu-id="be340-131">The following example demonstrates how to define a unique pointer.</span></span>

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

<span data-ttu-id="be340-132">Neste exemplo, o parâmetro *ach* é um ponteiro exclusivo para dados de caractere que é enviado a um servidor para ser processado com a rotina RemoteFn.</span><span class="sxs-lookup"><span data-stu-id="be340-132">In this example, the parameter *ach* is a unique pointer to character data that is sent to a server to be processed with the RemoteFn routine.</span></span>

 

 