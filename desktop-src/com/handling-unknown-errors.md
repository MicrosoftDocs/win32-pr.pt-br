---
title: Manipulando erros desconhecidos
description: Manipulando erros desconhecidos
ms.assetid: d6a4cc60-8320-4b67-9f2e-7c4bea6c37fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8c3d9e70b89a9a78be62d2940ad8a69ac34c8f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006081"
---
# <a name="handling-unknown-errors"></a><span data-ttu-id="7d188-103">Manipulando erros desconhecidos</span><span class="sxs-lookup"><span data-stu-id="7d188-103">Handling Unknown Errors</span></span>

<span data-ttu-id="7d188-104">É legal retornar um código de status somente da implementação de um método de interface aprovado como legalmente retornado.</span><span class="sxs-lookup"><span data-stu-id="7d188-104">It is legal to return a status code only from the implementation of an interface method sanctioned as legally returnable.</span></span> <span data-ttu-id="7d188-105">A falha ao observar essa regra convida a possibilidade de conflito entre valores de código de erro retornados e aqueles aprovados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7d188-105">Failure to observe this rule invites the possibility of conflict between returned error-code values and those sanctioned by the application.</span></span> <span data-ttu-id="7d188-106">Preste atenção especial a esse possível problema ao propagar códigos de erro de funções que são chamadas internamente.</span><span class="sxs-lookup"><span data-stu-id="7d188-106">Pay particular attention to this potential problem when propagating error codes from functions that are called internally.</span></span>

<span data-ttu-id="7d188-107">Os aplicativos que chamam interfaces devem tratar qualquer código de erro desconhecido retornado (em oposição a um código de êxito) como sinônimo de E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="7d188-107">Applications that call interfaces should treat any unknown returned error code (as opposed to a success code) as synonymous with E\_UNEXPECTED.</span></span> <span data-ttu-id="7d188-108">Essa prática de manipulação de códigos de erro desconhecidos é exigida pelos clientes das interfaces e funções definidas COM.</span><span class="sxs-lookup"><span data-stu-id="7d188-108">This practice of handling unknown error codes is required by clients of the COM-defined interfaces and functions.</span></span> <span data-ttu-id="7d188-109">Como a prática de programação típica é manipular alguns códigos de erro específicos em detalhes e tratar o restante de forma genérica, esse requisito de manipulação de códigos de erro inesperados ou desconhecidos é facilmente atendido.</span><span class="sxs-lookup"><span data-stu-id="7d188-109">Because typical programming practice is to handle a few specific error codes in detail and treat the rest generically, this requirement of handling unexpected or unknown error codes is easily met.</span></span>

<span data-ttu-id="7d188-110">É importante lidar com todos os erros possíveis ao chamar um método de interface.</span><span class="sxs-lookup"><span data-stu-id="7d188-110">It is important to handle all possible errors when calling an interface method.</span></span> <span data-ttu-id="7d188-111">Se não for possível fazer isso, o aplicativo falhará, corromperá os dados ou ficará vulnerável a explorações de segurança.</span><span class="sxs-lookup"><span data-stu-id="7d188-111">Failure to do so could cause your application to crash, to corrupt data, or to become vulnerable to security exploits.</span></span> <span data-ttu-id="7d188-112">O exemplo de código a seguir mostra a maneira recomendada de lidar com erros desconhecidos:</span><span class="sxs-lookup"><span data-stu-id="7d188-112">The following code sample shows the recommended way of handling unknown errors:</span></span>


```C++
HRESULT hr; 
hr = xxMethod(); 
 
switch (GetScode(hr))  
{ 
    case NOERROR: 
      // Method returned success. 
      break; 
 
    case x1: 
      // Handle error x1 here.
      break; 
 
    case x2: 
      // Handle error x2 here.
      break; 
 
    case E_UNEXPECTED: 
    default: 
      // Handle unexpected errors here. 
      break; 
} 
 
```



<span data-ttu-id="7d188-113">A verificação de erro a seguir é frequentemente usada com essas rotinas que não retornam nada especial (além de S \_ OK ou algum erro inesperado):</span><span class="sxs-lookup"><span data-stu-id="7d188-113">The following error check is often used with those routines that do not return anything special (other than S\_OK or some unexpected error):</span></span>


```C++
if (xxMethod() == NOERROR) 
{
    // Handle success here.
} 
else 
{
    // Handle failure here.
} 
```



## <a name="related-topics"></a><span data-ttu-id="7d188-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d188-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d188-115">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="7d188-115">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

 




