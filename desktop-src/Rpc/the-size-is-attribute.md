---
title: O atributo size_is
description: O atributo \ Size \_ is \ está associado a uma constante, expressão ou variável de inteiro que especifica o tamanho de alocação da matriz.
ms.assetid: 5252c1a2-8e07-4e28-8280-6a9563d1b291
keywords:
- size_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7159c68d6bc3c1485c14db20d97c488916cb7b22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823821"
---
# <a name="the-size_is-attribute"></a><span data-ttu-id="d1434-104">O \[ tamanho \_ é \] atributo</span><span class="sxs-lookup"><span data-stu-id="d1434-104">The \[size\_is\] Attribute</span></span>

<span data-ttu-id="d1434-105">O \[ [atributo \_ size](/windows/desktop/Midl/size-is) é \] associado a uma constante, expressão ou variável de inteiro que especifica o tamanho de alocação da matriz.</span><span class="sxs-lookup"><span data-stu-id="d1434-105">The \[ [size\_is](/windows/desktop/Midl/size-is)\] attribute is associated with an integer constant, expression, or variable that specifies the allocation size of the array.</span></span> <span data-ttu-id="d1434-106">Considere uma matriz de caracteres cujo comprimento seja determinado pela entrada do usuário:</span><span class="sxs-lookup"><span data-stu-id="d1434-106">Consider a character array whose length is determined by user input:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(2.0)
]
interface arraytest
{
  void fArray2([in] short sSize,
               [in, out, size_is(sSize)] char achArray[*]);
}
```

> [!Note]  
> <span data-ttu-id="d1434-107">O asterisco ( \* ) que marca o espaço reservado para a dimensão da matriz de variável é opcional.</span><span class="sxs-lookup"><span data-stu-id="d1434-107">The asterisk (\*) that marks the placeholder for the variable-array dimension is optional.</span></span>

 

<span data-ttu-id="d1434-108">O stub do servidor deve alocar memória no servidor que corresponda à memória no cliente para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d1434-108">The server stub must allocate memory on the server that corresponds to the memory on the client for that parameter.</span></span> <span data-ttu-id="d1434-109">A variável que especifica o tamanho deve ser sempre pelo menos um \[ parâmetro [in](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="d1434-109">The variable that specifies the size must always be at least an \[ [in](/windows/desktop/Midl/in)\] parameter.</span></span> <span data-ttu-id="d1434-110">O atributo direcional é necessário para que o valor de tamanho seja definido na entrada para o stub do servidor. **\[ \]**</span><span class="sxs-lookup"><span data-stu-id="d1434-110">The **\[in\]** directional attribute is required so that the size value is defined on entry to the server stub.</span></span> <span data-ttu-id="d1434-111">Esse valor de tamanho fornece informações que o stub de servidor requer para alocar a memória.</span><span class="sxs-lookup"><span data-stu-id="d1434-111">This size value provides information that the server stub requires to allocate the memory.</span></span>

<span data-ttu-id="d1434-112">O parâmetro Size também pode ser \[ in, [out](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="d1434-112">The size parameter can also be \[in, [out](/windows/desktop/Midl/out-idl)\].</span></span> <span data-ttu-id="d1434-113">Isso é útil se, por exemplo, a matriz que o cliente envia não for grande o suficiente para os dados que o servidor precisa armazenar nele.</span><span class="sxs-lookup"><span data-stu-id="d1434-113">This is useful if, for instance, the array the client sends is not large enough for the data that the server needs to store in it.</span></span> <span data-ttu-id="d1434-114">Você pode usar um parâmetro **\[ in, \] out** size para enviar o tamanho necessário de volta para o programa cliente.</span><span class="sxs-lookup"><span data-stu-id="d1434-114">You can use an **\[in, out\]** size parameter to send the required size back to the client program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1434-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1434-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1434-116">Vários níveis de ponteiros</span><span class="sxs-lookup"><span data-stu-id="d1434-116">Multiple Levels of Pointers</span></span>](multiple-levels-of-pointers.md)
</dt> </dl>

 

 