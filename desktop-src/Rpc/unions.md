---
title: palavra-chave Union (RPC)
description: As uniões exigem palavras-chave MIDL especiais para dar suporte ao uso com RPC (chamada de procedimento remoto).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294095"
---
# <a name="union-keyword-rpc"></a><span data-ttu-id="a3257-103">palavra-chave Union (RPC)</span><span class="sxs-lookup"><span data-stu-id="a3257-103">union keyword (RPC)</span></span>

<span data-ttu-id="a3257-104">Alguns recursos da linguagem C, como uniões, exigem palavras-chave MIDL especiais para dar suporte ao uso em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a3257-104">Some features of the C language, such as unions, require special MIDL keywords to support their use in remote procedure calls.</span></span> <span data-ttu-id="a3257-105">Uma União na linguagem C é uma variável que contém objetos de tipos e tamanhos diferentes.</span><span class="sxs-lookup"><span data-stu-id="a3257-105">A union in the C language is a variable that holds objects of different types and sizes.</span></span> <span data-ttu-id="a3257-106">O desenvolvedor geralmente cria uma variável para controlar os tipos armazenados na União.</span><span class="sxs-lookup"><span data-stu-id="a3257-106">The developer usually creates a variable to keep track of the types stored in the union.</span></span> <span data-ttu-id="a3257-107">Para operar corretamente em um ambiente distribuído, a variável que indica o tipo de Union, ou *discriminante*, também deve estar disponível para o computador remoto.</span><span class="sxs-lookup"><span data-stu-id="a3257-107">To operate correctly in a distributed environment, the variable that indicates the type of the union, or the *discriminant*, must also be available to the remote computer.</span></span> <span data-ttu-id="a3257-108">MIDL fornece o \[ [**\_ tipo de opção**](/windows/desktop/Midl/switch-type) \] e o \[ [**interruptor \_ são**](/windows/desktop/Midl/switch-is) \] palavras-chave para identificar o tipo e o nome de discriminante.</span><span class="sxs-lookup"><span data-stu-id="a3257-108">MIDL provides the \[[**switch\_type**](/windows/desktop/Midl/switch-type)\] and \[[**switch\_is**](/windows/desktop/Midl/switch-is)\] keywords to identify the discriminant type and name.</span></span>

<span data-ttu-id="a3257-109">MIDL requer que o discriminante seja transmitido com a União de uma das duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="a3257-109">MIDL requires that the discriminant be transmitted with the union in one of two ways:</span></span>

-   <span data-ttu-id="a3257-110">A União e o discriminante devem ser fornecidos como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a3257-110">The union and the discriminant must be provided as parameters.</span></span>
-   <span data-ttu-id="a3257-111">A União e o discriminante devem ser empacotados em uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="a3257-111">The union and the discriminant must be packaged in a structure.</span></span>

<span data-ttu-id="a3257-112">Dois tipos fundamentais de uniões discriminadas são fornecidos por MIDL: [**\_ União não encapsulada**](/windows/desktop/Midl/nonencapsulated-unions) e [**\_ União encapsulada**](/windows/desktop/Midl/encapsulated-unions).</span><span class="sxs-lookup"><span data-stu-id="a3257-112">Two fundamental types of discriminated unions are provided by MIDL: [**nonencapsulated\_union**](/windows/desktop/Midl/nonencapsulated-unions) and [**encapsulated\_union**](/windows/desktop/Midl/encapsulated-unions).</span></span> <span data-ttu-id="a3257-113">O discriminante de uma União não encapsulada será outro parâmetro se a União for um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a3257-113">The discriminant of a nonencapsulated union is another parameter if the union is a parameter.</span></span> <span data-ttu-id="a3257-114">Será outro campo se a União for um campo de uma estrutura.</span><span class="sxs-lookup"><span data-stu-id="a3257-114">It is another field if the union is a field of a structure.</span></span> <span data-ttu-id="a3257-115">A definição de uma União encapsulada é transformada em uma definição de estrutura cujo primeiro campo é o discriminante e cujo segundo e último campos são a União.</span><span class="sxs-lookup"><span data-stu-id="a3257-115">The definition of an encapsulated union is turned into a structure definition whose first field is the discriminant and whose second and last fields are the union.</span></span> <span data-ttu-id="a3257-116">O exemplo a seguir demonstra como fornecer os parâmetros Union e discriminante como:</span><span class="sxs-lookup"><span data-stu-id="a3257-116">The following example demonstrates how to provide the union and discriminant as parameters:</span></span>

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

<span data-ttu-id="a3257-117">A União no exemplo anterior pode conter um único valor: **curto**, **float** ou **Char**.</span><span class="sxs-lookup"><span data-stu-id="a3257-117">The union in the preceding example can contain a single value: either **short**, **float**, or **char**.</span></span> <span data-ttu-id="a3257-118">A definição de tipo para a União inclui o atributo de **\_ tipo de opção** MIDL que especifica o tipo de discriminante.</span><span class="sxs-lookup"><span data-stu-id="a3257-118">The type definition for the union includes the MIDL **switch\_type** attribute that specifies the type of the discriminant.</span></span> <span data-ttu-id="a3257-119">Aqui, \[ tipo de comutador \_ (curto) \] especifica que o discriminante é do tipo **curto**.</span><span class="sxs-lookup"><span data-stu-id="a3257-119">Here, \[switch\_type(short)\] specifies that the discriminant is of type **short**.</span></span> <span data-ttu-id="a3257-120">A opção deve ser um tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="a3257-120">The switch must be an integer type.</span></span>

<span data-ttu-id="a3257-121">Se Union for um membro de uma estrutura, o discriminante deverá ser um membro da mesma estrutura.</span><span class="sxs-lookup"><span data-stu-id="a3257-121">If the union is a member of a structure, then the discriminant must be a member of the same structure.</span></span> <span data-ttu-id="a3257-122">Se Union for um parâmetro, o discriminante deverá ser outro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a3257-122">If the union is a parameter, then the discriminant must be another parameter.</span></span> <span data-ttu-id="a3257-123">O protótipo para a função **UnionParamProc** no exemplo anterior mostra o discriminante *sUtype* como o último parâmetro da chamada.</span><span class="sxs-lookup"><span data-stu-id="a3257-123">The prototype for the function **UnionParamProc** in the preceding example shows the discriminant *sUtype* as the last parameter of the call.</span></span> <span data-ttu-id="a3257-124">(O discriminante pode aparecer em qualquer posição na chamada.) O tipo do parâmetro especificado na **\[ opção \_ \]** o atributo deve corresponder ao tipo especificado no atributo de **\[ \_ tipo \] de comutador** .</span><span class="sxs-lookup"><span data-stu-id="a3257-124">(The discriminant can appear in any position in the call.) The type of the parameter specified in the **\[switch\_is\]** attribute must match the type specified in the **\[switch\_type\]** attribute.</span></span>

<span data-ttu-id="a3257-125">O exemplo a seguir demonstra o uso de uma única estrutura que empacota o discriminante com a União:</span><span class="sxs-lookup"><span data-stu-id="a3257-125">The following example demonstrates the use of a single structure that packages the discriminant with the union:</span></span>

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

<span data-ttu-id="a3257-126">O compilador Microsoft RPC MIDL permite declarações Union fora de construções [**typedef**](/windows/desktop/Midl/typedef) .</span><span class="sxs-lookup"><span data-stu-id="a3257-126">The Microsoft RPC MIDL compiler allows union declarations outside of [**typedef**](/windows/desktop/Midl/typedef) constructs.</span></span> <span data-ttu-id="a3257-127">Esse recurso é uma extensão para o DCE IDL.</span><span class="sxs-lookup"><span data-stu-id="a3257-127">This feature is an extension to DCE IDL.</span></span> <span data-ttu-id="a3257-128">Para obter mais informações, consulte [**Union**](/windows/desktop/Midl/union).</span><span class="sxs-lookup"><span data-stu-id="a3257-128">For more information, see [**union**](/windows/desktop/Midl/union).</span></span>

 

 