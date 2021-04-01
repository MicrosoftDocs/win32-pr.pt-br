---
title: Atributos direcional (parâmetro)
description: Os atributos direcionais descrevem se os dados são transmitidos do cliente para o servidor, servidor para cliente ou ambos.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Chamada de procedimento remoto RPC, descrito, atributos direcionais
- in
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec37dbf65919f5aae9e7674cf7102eddcdf5170
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084718"
---
# <a name="directional-parameter-attributes"></a><span data-ttu-id="04a09-106">Atributos direcional (parâmetro)</span><span class="sxs-lookup"><span data-stu-id="04a09-106">Directional (Parameter) Attributes</span></span>

<span data-ttu-id="04a09-107">Os atributos direcionais descrevem se os dados são transmitidos do cliente para o servidor, servidor para cliente ou ambos.</span><span class="sxs-lookup"><span data-stu-id="04a09-107">Directional attributes describe whether the data is transmitted from client to server, server to client, or both.</span></span> <span data-ttu-id="04a09-108">Todos os parâmetros no protótipo de função devem ser associados a atributos direcionais.</span><span class="sxs-lookup"><span data-stu-id="04a09-108">All parameters in the function prototype must be associated with directional attributes.</span></span> <span data-ttu-id="04a09-109">As três combinações possíveis de atributos direcionais são: 1) \[ [**em**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] e 3) \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="04a09-109">The three possible combinations of directional attributes are: 1) \[[**in**](/windows/desktop/Midl/in)\], 2) \[[**out**](/windows/desktop/Midl/out-idl)\], and 3) \[**in**, **out**\].</span></span> <span data-ttu-id="04a09-110">Elas descrevem a maneira como os parâmetros são passados entre os procedimentos de chamada e chamados.</span><span class="sxs-lookup"><span data-stu-id="04a09-110">These describe the way parameters are passed between calling and called procedures.</span></span> <span data-ttu-id="04a09-111">Quando você compila no padrão (modo estendido da Microsoft) e omite um atributo direcional para um parâmetro, o compilador MIDL assume um valor padrão de \[ **no** \] .</span><span class="sxs-lookup"><span data-stu-id="04a09-111">When you compile in the default (Microsoft-extended mode) and you omit a directional attribute for a parameter, the MIDL compiler assumes a default value of \[**in**\].</span></span>

<span data-ttu-id="04a09-112">Um \[ parâmetro de [**saída**](/windows/desktop/Midl/out-idl) \] deve ser um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="04a09-112">An \[[**out**](/windows/desktop/Midl/out-idl)\] parameter must be a pointer.</span></span> <span data-ttu-id="04a09-113">Na verdade, o \[  \] atributo out não é significativo quando aplicado a parâmetros que não atuam como ponteiros porque os parâmetros da função C são passados por valor.</span><span class="sxs-lookup"><span data-stu-id="04a09-113">In fact, the \[**out**\] attribute is not meaningful when applied to parameters that do not act as pointers because C function parameters are passed by value.</span></span> <span data-ttu-id="04a09-114">Em C, a função chamada recebe uma cópia privada do valor do parâmetro; Ele não pode alterar o valor da função de chamada para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="04a09-114">In C, the called function receives a private copy of the parameter value; it cannot change the calling function's value for that parameter.</span></span> <span data-ttu-id="04a09-115">No entanto, se o parâmetro atuar como um ponteiro, ele poderá ser usado para acessar e modificar a memória.</span><span class="sxs-lookup"><span data-stu-id="04a09-115">If the parameter acts as a pointer, however, it can be used to access and modify memory.</span></span> <span data-ttu-id="04a09-116">O \[ atributo **out** \] indica que a função de servidor deve retornar o valor para a função de chamada do cliente e que a memória associada ao ponteiro deve ser retornada de acordo com os atributos atribuídos ao ponteiro.</span><span class="sxs-lookup"><span data-stu-id="04a09-116">The \[**out**\] attribute indicates that the server function should return the value to the client's calling function, and that memory associated with the pointer should be returned in accordance with the attributes assigned to the pointer.</span></span>

<span data-ttu-id="04a09-117">A interface a seguir demonstra as três possíveis combinações de atributos direcionais que podem ser aplicados a um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="04a09-117">The following interface demonstrates the three possible combinations of directional attributes that can be applied to a parameter.</span></span> <span data-ttu-id="04a09-118">A função **InOutProc** é definida no arquivo IDL como:</span><span class="sxs-lookup"><span data-stu-id="04a09-118">The function **InOutProc** is defined in the IDL file as:</span></span>

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

<span data-ttu-id="04a09-119">O primeiro parâmetro, *S1*, é \[ somente [**no**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="04a09-119">The first parameter, *s1*, is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="04a09-120">Seu valor é transmitido para o computador remoto, mas não é retornado para o procedimento de chamada.</span><span class="sxs-lookup"><span data-stu-id="04a09-120">Its value is transmitted to the remote computer, but is not returned to the calling procedure.</span></span> <span data-ttu-id="04a09-121">Embora o aplicativo de servidor possa alterar seu valor para *S1*, o valor de *S1* no cliente é o mesmo antes e depois da chamada.</span><span class="sxs-lookup"><span data-stu-id="04a09-121">Although the server application can change its value for *s1*, the value of *s1* on the client is the same before and after the call.</span></span>

<span data-ttu-id="04a09-122">O segundo parâmetro, *PS2*, é definido no protótipo da função como um ponteiro com os \[ atributos [**in**](/windows/desktop/Midl/in) \] e \[ [**out**](/windows/desktop/Midl/out-idl) \] .</span><span class="sxs-lookup"><span data-stu-id="04a09-122">The second parameter, *ps2*, is defined in the function prototype as a pointer with both \[[**in**](/windows/desktop/Midl/in)\] and \[[**out**](/windows/desktop/Midl/out-idl)\] attributes.</span></span> <span data-ttu-id="04a09-123">O \[ atributo **in** \] indica que o valor do parâmetro é passado do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="04a09-123">The \[**in**\] attribute indicates that the value of the parameter is passed from the client to the server.</span></span> <span data-ttu-id="04a09-124">O \[ atributo **out** \] indica que o valor apontado por *PS2* é retornado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="04a09-124">The \[**out**\] attribute indicates that the value pointed to by *ps2* is returned to the client.</span></span>

<span data-ttu-id="04a09-125">O terceiro parâmetro está \[ [**fora**](/windows/desktop/Midl/out-idl) \] apenas.</span><span class="sxs-lookup"><span data-stu-id="04a09-125">The third parameter is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="04a09-126">O espaço é alocado para o parâmetro no servidor, mas o valor é indefinido na entrada.</span><span class="sxs-lookup"><span data-stu-id="04a09-126">Space is allocated for the parameter on the server, but the value is undefined on entry.</span></span> <span data-ttu-id="04a09-127">Conforme mencionado acima, todos os parâmetros de \[ **saída** \] devem ser ponteiros.</span><span class="sxs-lookup"><span data-stu-id="04a09-127">As mentioned above, all \[**out**\] parameters must be pointers.</span></span>

<span data-ttu-id="04a09-128">O procedimento remoto altera o valor de todos os três parâmetros, mas apenas os novos valores dos \[ [](/windows/desktop/Midl/out-idl) \] parâmetros out e \[ [**in**](/windows/desktop/Midl/in) \] estão disponíveis para o cliente.</span><span class="sxs-lookup"><span data-stu-id="04a09-128">The remote procedure changes the value of all three parameters, but only the new values of the \[[**out**](/windows/desktop/Midl/out-idl)\] and \[[**in**](/windows/desktop/Midl/in)\] parameters are available to the client.</span></span>


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



<span data-ttu-id="04a09-129">No retorno da chamada para **InOutProc**, o segundo e o terceiro parâmetros são modificados.</span><span class="sxs-lookup"><span data-stu-id="04a09-129">On return from the call to **InOutProc**, the second and third parameters are modified.</span></span> <span data-ttu-id="04a09-130">O primeiro parâmetro, que está \[ [**em**](/windows/desktop/Midl/in) \] apenas, é inalterado.</span><span class="sxs-lookup"><span data-stu-id="04a09-130">The first parameter, which is \[[**in**](/windows/desktop/Midl/in)\] only, is unchanged.</span></span>

![em parâmetros](images/prog-a22.png)

![parâmetros out](images/prog-a23.png)

![parâmetros de entrada](images/prog-a21.png)

 

 