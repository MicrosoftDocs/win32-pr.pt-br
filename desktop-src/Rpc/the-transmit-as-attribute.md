---
title: O atributo transmit_as
description: O atributo \ transmitir \_ como \ oferece uma maneira de controlar o marshaling de dados sem se preocupar com o marshaling de dados em um nível baixo \ 8212; ou seja, sem se preocupar com tamanhos de dados ou permutação de bytes em um ambiente heterogêneo.
ms.assetid: 04e670c9-b091-457d-aeca-058cf5b664e8
keywords:
- RPC, atributos transmit_as de chamada de procedimento remoto
- transmit_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08b885826aea302a16d8c23709de0ef0b07a848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366410"
---
# <a name="the-transmit_as-attribute"></a><span data-ttu-id="35fa6-105">O \_ atributo transmitir como</span><span class="sxs-lookup"><span data-stu-id="35fa6-105">The transmit\_as Attribute</span></span>

<span data-ttu-id="35fa6-106">O **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** oferece uma maneira de controlar o marshaling de dados sem se preocupar com o marshaling de dados em um nível baixo, ou seja, sem se preocupar com tamanhos de dados ou permutação de bytes em um ambiente heterogêneo.</span><span class="sxs-lookup"><span data-stu-id="35fa6-106">The **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute offers a way to control data marshaling without worrying about marshaling data at a low level—that is, without worrying about data sizes or byte swapping in a heterogeneous environment.</span></span> <span data-ttu-id="35fa6-107">Ao permitir que você reduza a quantidade de dados transmitidos pela rede, o atributo **\[ transmitir \_ como \]** pode tornar seu aplicativo mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="35fa6-107">By letting you reduce the amount of data transmitted over the network, the **\[transmit\_as\]** attribute can make your application more efficient.</span></span>

<span data-ttu-id="35fa6-108">Use o atributo **\[ transmitir \_ como \]** para especificar um tipo de dados que os stubs RPC transmitirá pela rede em vez de usar o tipo de dados fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35fa6-108">You use the **\[transmit\_as\]** attribute to specify a data type that the RPC stubs will transmit over the network instead of using the data type provided by the application.</span></span> <span data-ttu-id="35fa6-109">Você fornece rotinas que convertem o tipo de dados de e para o tipo que é usado para transmissão.</span><span class="sxs-lookup"><span data-stu-id="35fa6-109">You supply routines that convert the data type to and from the type that is used for transmission.</span></span> <span data-ttu-id="35fa6-110">Você também deve fornecer rotinas para liberar a memória usada para o tipo de dados e o tipo transmitido.</span><span class="sxs-lookup"><span data-stu-id="35fa6-110">You must also supply routines to free the memory used for the data type and the transmitted type.</span></span> <span data-ttu-id="35fa6-111">Por exemplo, o seguinte define **o \_ tipo de transmissão** como o tipo de dados transmitido para todos os dados de aplicativo especificados como sendo do tipo **\_ espec**:</span><span class="sxs-lookup"><span data-stu-id="35fa6-111">For example, the following defines **xmit\_type** as the data type transmitted for all application data specified as being of type **type\_spec**:</span></span>

``` syntax
typedef [transmit_as (xmit_type)] type_spec type;
```

<span data-ttu-id="35fa6-112">A tabela a seguir descreve os quatro nomes de rotina fornecidos pelo programador.</span><span class="sxs-lookup"><span data-stu-id="35fa6-112">The following table describes the four programmer-supplied routine names.</span></span> <span data-ttu-id="35fa6-113">**Type** é o tipo de dados conhecido pelo aplicativo, e **o \_ tipo de transmissão** é o tipo de dados usado para transmissão.</span><span class="sxs-lookup"><span data-stu-id="35fa6-113">**Type** is the data type known to the application, and **xmit\_type** is the data type used for transmission.</span></span>



| <span data-ttu-id="35fa6-114">Rotina</span><span class="sxs-lookup"><span data-stu-id="35fa6-114">Routine</span></span>                                                 | <span data-ttu-id="35fa6-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="35fa6-115">Description</span></span>                                                                                                                                     |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35fa6-116">**tipo \_ para \_ transmissão**</span><span class="sxs-lookup"><span data-stu-id="35fa6-116">**type\_to\_xmit**</span></span>](the-type-to-xmit-function.md)     | <span data-ttu-id="35fa6-117">Aloca um objeto do tipo transmitido e converte do tipo de aplicativo para o tipo transmitido pela rede (chamador e objeto chamado).</span><span class="sxs-lookup"><span data-stu-id="35fa6-117">Allocates an object of the transmitted type and converts from application type to type transmitted over the network (caller and object called).</span></span> |
| [<span data-ttu-id="35fa6-118">**Tipo \_ de \_ transmissão**</span><span class="sxs-lookup"><span data-stu-id="35fa6-118">**Type\_from\_xmit**</span></span>](the-type-from-xmit-function.md) | <span data-ttu-id="35fa6-119">Converte do tipo transmitido para o tipo de aplicativo (chamador e objeto chamado).</span><span class="sxs-lookup"><span data-stu-id="35fa6-119">Converts from transmitted type to application type (caller and object called).</span></span>                                                                  |
| [<span data-ttu-id="35fa6-120">**Digite \_ \_ InStr gratuito**</span><span class="sxs-lookup"><span data-stu-id="35fa6-120">**Type\_free\_inst**</span></span>](the-type-free-inst-function.md) | <span data-ttu-id="35fa6-121">Libera recursos usados pelo tipo de aplicativo (objeto chamado somente).</span><span class="sxs-lookup"><span data-stu-id="35fa6-121">Frees resources used by the application type (object called only).</span></span>                                                                              |
| [<span data-ttu-id="35fa6-122">**\_Transmissão gratuita de tipo \_**</span><span class="sxs-lookup"><span data-stu-id="35fa6-122">**Type\_free\_xmit**</span></span>](the-type-free-xmit-function.md) | <span data-ttu-id="35fa6-123">Libera o armazenamento retornado pelo tipo para a rotina de \*\*\*\*\*\_\*\*\* \_ transmissão\*\* (chamador e objeto chamado).</span><span class="sxs-lookup"><span data-stu-id="35fa6-123">Frees storage returned by the **type ***\_*** to\_xmit** routine (caller and object called).</span></span>                                                      |



 

<span data-ttu-id="35fa6-124">Além dessas quatro funções fornecidas pelo programador, o tipo transmitido não é manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35fa6-124">Other than by these four programmer-supplied functions, the transmitted type is not manipulated by the application.</span></span> <span data-ttu-id="35fa6-125">O tipo transmitido é definido somente para mover dados pela rede.</span><span class="sxs-lookup"><span data-stu-id="35fa6-125">The transmitted type is defined only to move data over the network.</span></span> <span data-ttu-id="35fa6-126">Depois que os dados são convertidos no tipo usado pelo aplicativo, a memória usada pelo tipo transmitido é liberada.</span><span class="sxs-lookup"><span data-stu-id="35fa6-126">After the data is converted to the type used by the application, the memory used by the transmitted type is freed.</span></span>

<span data-ttu-id="35fa6-127">Essas rotinas fornecidas pelo programador são fornecidas pelo cliente ou pelo aplicativo de servidor com base nos atributos direcionais.</span><span class="sxs-lookup"><span data-stu-id="35fa6-127">These programmer-supplied routines are provided by either the client or the server application based on the directional attributes.</span></span> <span data-ttu-id="35fa6-128">Se o parâmetro for **\[** [](/windows/desktop/Midl/in) **\]** somente, o cliente transmitirá para o servidor.</span><span class="sxs-lookup"><span data-stu-id="35fa6-128">If the parameter is **\[**[**in**](/windows/desktop/Midl/in)**\]** only, the client transmits to the server.</span></span> <span data-ttu-id="35fa6-129">O cliente precisa do **tipo \_ para \_ transmissão** e tipo de funções de **\_ \_ transmissão gratuita** .</span><span class="sxs-lookup"><span data-stu-id="35fa6-129">The client needs the **type\_to\_xmit** and **type\_free\_xmit** functions.</span></span> <span data-ttu-id="35fa6-130">O servidor precisa do **tipo \_ de \_ transmissão** e **digitar \_ funções \_ Inst gratuitas** .</span><span class="sxs-lookup"><span data-stu-id="35fa6-130">The server needs the **type\_from\_xmit** and **type\_free\_inst** functions.</span></span> <span data-ttu-id="35fa6-131">Para um **\[** [](/windows/desktop/Midl/out-idl) **\]** parâmetro somente out, o servidor transmite para o cliente.</span><span class="sxs-lookup"><span data-stu-id="35fa6-131">For an **\[**[**out**](/windows/desktop/Midl/out-idl)**\]**-only parameter, the server transmits to the client.</span></span> <span data-ttu-id="35fa6-132">O aplicativo de servidor deve implementar o **tipo \_ para \_ transmissão** e digitar funções de **\_ \_ transmissão gratuitas** , enquanto o programa cliente deve fornecer o **tipo da função \_ de \_ transmissão** .</span><span class="sxs-lookup"><span data-stu-id="35fa6-132">The server application must implement the **type\_to\_xmit** and **type\_free\_xmit** functions, while the client program must supply the **type\_from\_xmit** function.</span></span> <span data-ttu-id="35fa6-133">Para os objetos **de \_ tipo de transmissão** temporários, o stub chamará a \*\*\*\*\*\_\*\*\* \_ transmissão gratuita de tipo\*\* para liberar qualquer memória alocada por uma chamada de **tipo \_ para \_ transmissão**.</span><span class="sxs-lookup"><span data-stu-id="35fa6-133">For the temporary **xmit\_type** objects, the stub will call **type ***\_*** free\_xmit** to free any memory allocated by a call to **type\_to\_xmit**.</span></span>

<span data-ttu-id="35fa6-134">Certas diretrizes se aplicam à instância do tipo de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35fa6-134">Certain guidelines apply to the application type instance.</span></span> <span data-ttu-id="35fa6-135">Se o tipo de aplicativo for um ponteiro ou contiver um ponteiro, o **tipo** \_ **da rotina de \_ transmissão** deverá alocar memória para os dados aos quais os ponteiros apontam (o próprio objeto de tipo de aplicativo é manipulado pelo stub da maneira usual).</span><span class="sxs-lookup"><span data-stu-id="35fa6-135">If the application type is a pointer or contains a pointer, then the **type**\_**from\_xmit** routine must allocate memory for the data that the pointers point to (the application type object itself is manipulated by the stub in the usual way).</span></span>

<span data-ttu-id="35fa6-136">Para parâmetros **de saída e \[ saída, ou um de seus componentes, de um tipo que contém o atributo transmitir como, o tipo de rotina Inst gratuita é chamado automaticamente para os objetos de dados que têm o atributo. \]** **\[ \_ \]** **\[ \] \]**  \_ **\_**</span><span class="sxs-lookup"><span data-stu-id="35fa6-136">For **\[out\]** and **\[in, out\] out\]** parameters, or one of their components, of a type that contains the **\[transmit\_as\]** attribute, the **type**\_**free\_inst** routine is automatically called for the data objects that have the attribute.</span></span> <span data-ttu-id="35fa6-137">Para parâmetros **in** , a  \_ rotina **\_ Inst gratuita** do tipo será chamada somente se o atributo **\[ transmitir \_ como \]** tiver sido aplicado ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="35fa6-137">For **in** parameters, the **type**\_**free\_inst** routine is called only if the **\[transmit\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="35fa6-138">Se o atributo tiver sido aplicado aos componentes do parâmetro, a  \_ rotina **\_ Inst gratuita** de tipo não será chamada.</span><span class="sxs-lookup"><span data-stu-id="35fa6-138">If the attribute has been applied to the components of the parameter, the **type**\_**free\_inst** routine is not called.</span></span> <span data-ttu-id="35fa6-139">Não há chamadas de liberação para os dados inseridos e uma chamada na maioria-uma (relacionada ao atributo de nível superior) para um parâmetro **in** only.</span><span class="sxs-lookup"><span data-stu-id="35fa6-139">There are no freeing calls for the embedded data and at-most-one call (related to the top-level attribute) for an **in** only parameter.</span></span>

<span data-ttu-id="35fa6-140">Em vigor com o MIDL 2,0, tanto o cliente quanto o servidor devem fornecer todas as quatro funções.</span><span class="sxs-lookup"><span data-stu-id="35fa6-140">Effective with MIDL 2.0, both client and server must supply all four functions.</span></span> <span data-ttu-id="35fa6-141">Por exemplo, uma lista vinculada pode ser transmitida como uma matriz dimensionada.</span><span class="sxs-lookup"><span data-stu-id="35fa6-141">For example, a linked list can be transmitted as a sized array.</span></span> <span data-ttu-id="35fa6-142">O **tipo \_ para \_** a rotina de transmissão percorre a lista vinculada e copia os dados ordenados em uma matriz.</span><span class="sxs-lookup"><span data-stu-id="35fa6-142">The **type\_to\_xmit** routine walks the linked list and copies the ordered data into an array.</span></span> <span data-ttu-id="35fa6-143">Os elementos da matriz são ordenados para que os vários ponteiros associados à estrutura da lista não precisem ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="35fa6-143">The array elements are ordered so that the many pointers associated with the list structure do not have to be transmitted.</span></span> <span data-ttu-id="35fa6-144">O **tipo \_ da rotina de \_ transmissão** lê a matriz e coloca seus elementos em uma estrutura de lista vinculada.</span><span class="sxs-lookup"><span data-stu-id="35fa6-144">The **type\_from\_xmit** routine reads the array and puts its elements into a linked-list structure.</span></span>

<span data-ttu-id="35fa6-145">A lista de links duplos ( \_ lista de vínculos duplas \_ ) inclui dados e ponteiros para os elementos de lista anteriores e seguintes:</span><span class="sxs-lookup"><span data-stu-id="35fa6-145">The double-linked list (DOUBLE\_LINK\_LIST) includes data and pointers to the previous and next list elements:</span></span>

``` syntax
typedef struct _DOUBLE_LINK_LIST 
{
    short sNumber;
    struct _DOUBLE_LINK_LIST * pNext;
    struct _DOUBLE_LINK_LIST * pPrevious;
} DOUBLE_LINK_LIST;
```

<span data-ttu-id="35fa6-146">Em vez de enviar a estrutura complexa, o **\[** atributo [**transmitir \_ como**](/windows/desktop/Midl/transmit-as) **\]** pode ser usado para enviá-la pela rede como uma matriz.</span><span class="sxs-lookup"><span data-stu-id="35fa6-146">Rather than shipping the complex structure, the **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** attribute can be used to send it over the network as an array.</span></span> <span data-ttu-id="35fa6-147">A sequência de itens na matriz retém a ordem dos elementos na lista com um custo menor:</span><span class="sxs-lookup"><span data-stu-id="35fa6-147">The sequence of items in the array retains the ordering of the elements in the list at a lower cost:</span></span>

``` syntax
typedef struct _DOUBLE_XMIT_TYPE 
{
    short sSize;
    [size_is(sSize)] short asNumber[];
} DOUBLE_XMIT_TYPE;
```

<span data-ttu-id="35fa6-148">O atributo **\[ transmitir \_ como \]** aparece no arquivo IDL:</span><span class="sxs-lookup"><span data-stu-id="35fa6-148">The **\[transmit\_as\]** attribute appears in the IDL file:</span></span>

``` syntax
typedef [transmit_as(DOUBLE_XMIT_TYPE)]  DOUBLE_LINK_LIST DOUBLE_LINK_TYPE;
```

<span data-ttu-id="35fa6-149">No exemplo a seguir, **ModifyListProc** define o parâmetro do tipo link duplo tipo \_ \_ como um parâmetro **\[ in, \] out** :</span><span class="sxs-lookup"><span data-stu-id="35fa6-149">In the following example, **ModifyListProc** defines the parameter of type DOUBLE\_LINK\_TYPE as an **\[in, out\]** parameter:</span></span>

``` syntax
void ModifyListProc([in, out] DOUBLE_LINK_TYPE * pHead)
```

<span data-ttu-id="35fa6-150">As quatro funções definidas pelo programador usam o nome do tipo nos nomes de função e usam os tipos apresentados e transmitidos como tipos de parâmetro, conforme necessário:</span><span class="sxs-lookup"><span data-stu-id="35fa6-150">The four programmer-defined functions use the name of the type in the function names, and use the presented and transmitted types as parameter types, as required:</span></span>

``` syntax
void __RPC_USER DOUBLE_LINK_TYPE_to_xmit ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList, 
    DOUBLE_XMIT_TYPE __RPC_FAR * __RPC_FAR * ppArray);

void __RPC_USER DOUBLE_LINK_TYPE_from_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray,
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_inst ( 
    DOUBLE_LINK_TYPE __RPC_FAR * pList);

void __RPC_USER DOUBLE_LINK_TYPE_free_xmit ( 
    DOUBLE_XMIT_TYPE __RPC_FAR * pArray);
```

 

 