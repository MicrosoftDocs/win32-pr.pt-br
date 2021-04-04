---
title: O atributo represent_as
description: O atributo \ representa \_ como \ permite que você especifique como um tipo de dados transmititable específico é representado ao aplicativo.
ms.assetid: 6f07ab90-b5bb-48ae-870c-5abaf80ce0e5
keywords:
- RPC, atributos represent_as de chamada de procedimento remoto
- represent_as
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7121925f1407cb3390c3ef1e7e5f2f6430506071
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084835"
---
# <a name="the-represent_as-attribute"></a><span data-ttu-id="40bc0-105">O atributo de representar \_ como</span><span class="sxs-lookup"><span data-stu-id="40bc0-105">The represent\_as Attribute</span></span>

<span data-ttu-id="40bc0-106">O \[ atributo " [representar \_ como](/windows/desktop/Midl/represent-as) " \] permite especificar como um tipo de dados de transmissão específico é representado ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-106">The \[ [represent\_as](/windows/desktop/Midl/represent-as)\] attribute lets you specify how a particular transmittable data type is represented to the application.</span></span> <span data-ttu-id="40bc0-107">Isso é feito especificando o nome do tipo representado para um tipo de transmissões conhecido e fornecendo as rotinas de conversão.</span><span class="sxs-lookup"><span data-stu-id="40bc0-107">This is done by specifying the name of the represented type for a known transmittable type and supplying the conversion routines.</span></span> <span data-ttu-id="40bc0-108">Você também deve fornecer as rotinas para liberar a memória usada pelos objetos de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="40bc0-108">You must also supply the routines to free the memory used by the data type objects.</span></span>

<span data-ttu-id="40bc0-109">Use o atributo " **\[ representar \_ como \]** " para apresentar um aplicativo com um tipo de dados diferente, possivelmente não transmitido, em vez do tipo que é realmente transmitido entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="40bc0-109">Use the **\[represent\_as\]** attribute to present an application with a different, possibly untransmittable, data type rather than the type that is actually transmitted between the client and server.</span></span> <span data-ttu-id="40bc0-110">Também é possível que o tipo manipulado pelo aplicativo possa ser desconhecido no momento da compilação MIDL.</span><span class="sxs-lookup"><span data-stu-id="40bc0-110">It is also possible that the type the application manipulates can be unknown at the time of MIDL compilation.</span></span> <span data-ttu-id="40bc0-111">Quando você escolhe um tipo de transmissãotable bem definido, não precisa se preocupar com a representação de dados no ambiente heterogêneo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-111">When you choose a well-defined transmittable type, you need not be concerned about data representation in the heterogeneous environment.</span></span> <span data-ttu-id="40bc0-112">O atributo " **\[ representar \_ como \]** " pode tornar seu aplicativo mais eficiente, reduzindo a quantidade de dados transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="40bc0-112">The **\[represent\_as\]** attribute can make your application more efficient by reducing the amount of data transmitted over the network.</span></span>

<span data-ttu-id="40bc0-113">O atributo **\[ representar \_ \] como** é semelhante ao atributo \[ [transmitir \_ como](/windows/desktop/Midl/transmit-as) \] .</span><span class="sxs-lookup"><span data-stu-id="40bc0-113">The **\[represent\_as\]** attribute is similar to the \[ [transmit\_as](/windows/desktop/Midl/transmit-as)\] attribute.</span></span> <span data-ttu-id="40bc0-114">No entanto, embora a **\[ transmissão \_ como \]** permita que você especifique um tipo de dados que será usado para transmissão, **\[ represente \_ como \]** permite especificar como um tipo de dados é representado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-114">However, while **\[transmit\_as\]** lets you specify a data type that will be used for transmission, **\[represent\_as\]** lets you specify how a data type is represented for the application.</span></span> <span data-ttu-id="40bc0-115">O tipo representado não precisa ser definido nos arquivos de MIDL processados; Ele pode ser definido no momento em que os stubs são compilados com o compilador C.</span><span class="sxs-lookup"><span data-stu-id="40bc0-115">The represented type need not be defined in the MIDL processed files; it can be defined at the time the stubs are compiled with the C compiler.</span></span> <span data-ttu-id="40bc0-116">Para fazer isso, use a diretiva include no [arquivo de configuração de aplicativo (ACF)](the-application-configuration-file-acf-.md) para compilar o arquivo de cabeçalho apropriado.</span><span class="sxs-lookup"><span data-stu-id="40bc0-116">To do this, use the include directive in the [application configuration file (ACF)](the-application-configuration-file-acf-.md) to compile the appropriate header file.</span></span> <span data-ttu-id="40bc0-117">Por exemplo, o ACF a seguir define um tipo local para o aplicativo **, \_ tipo repr**, para o tipo nomeado de transmittable **\_ :**</span><span class="sxs-lookup"><span data-stu-id="40bc0-117">For example, the following ACF defines a type local to the application, **repr\_type**, for the transmittable type **named\_type:**</span></span>

``` syntax
typedef [represent_as(repr_type) [, type_attribute_list] named_type;
```

<span data-ttu-id="40bc0-118">A tabela a seguir descreve as quatro rotinas fornecidas pelo programador.</span><span class="sxs-lookup"><span data-stu-id="40bc0-118">The following table describes the four programmer-supplied routines.</span></span>



| <span data-ttu-id="40bc0-119">Rotina</span><span class="sxs-lookup"><span data-stu-id="40bc0-119">Routine</span></span>                      | <span data-ttu-id="40bc0-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="40bc0-120">Description</span></span>                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40bc0-121">**\_tipo nomeado \_ do \_ local**</span><span class="sxs-lookup"><span data-stu-id="40bc0-121">**named\_type\_from\_local**</span></span> | <span data-ttu-id="40bc0-122">Aloca uma instância do tipo de rede e converte do tipo local para o tipo de rede.</span><span class="sxs-lookup"><span data-stu-id="40bc0-122">Allocates an instance of the network type and converts from the local type to the network type.</span></span>      |
| <span data-ttu-id="40bc0-123">**\_tipo nomeado \_ para \_ local**</span><span class="sxs-lookup"><span data-stu-id="40bc0-123">**named\_type\_to\_local**</span></span>   | <span data-ttu-id="40bc0-124">Converte o tipo de rede para o tipo local.</span><span class="sxs-lookup"><span data-stu-id="40bc0-124">Converts from the network type to the local type.</span></span>                                                    |
| <span data-ttu-id="40bc0-125">**\_tipo nomeado \_ \_ local gratuito**</span><span class="sxs-lookup"><span data-stu-id="40bc0-125">**named\_type\_free\_local**</span></span> | <span data-ttu-id="40bc0-126">Libera a memória alocada por uma chamada para **o \_ tipo nomeado para a rotina \_ \_ local** , mas não para o próprio tipo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-126">Frees memory allocated by a call to the **named\_type\_to\_local** routine, but not the type itself.</span></span> |
| <span data-ttu-id="40bc0-127">**Inst. de \_ tipo nomeado \_ \_**</span><span class="sxs-lookup"><span data-stu-id="40bc0-127">**named\_type\_free\_inst**</span></span>  | <span data-ttu-id="40bc0-128">Libera o armazenamento para o tipo de rede (ambos os lados).</span><span class="sxs-lookup"><span data-stu-id="40bc0-128">Frees storage for the network type (both sides).</span></span>                                                     |



 

<span data-ttu-id="40bc0-129">Além dessas quatro rotinas fornecidas pelo programador, o tipo nomeado não é manipulado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-129">Other than by these four programmer-supplied routines, the named type is not manipulated by the application.</span></span> <span data-ttu-id="40bc0-130">O único tipo visível para o aplicativo é o tipo representado.</span><span class="sxs-lookup"><span data-stu-id="40bc0-130">The only type visible to the application is the represented type.</span></span> <span data-ttu-id="40bc0-131">O aplicativo usa o nome do tipo representado em vez do nome do tipo transmitido nos protótipos e stubs gerados pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="40bc0-131">The application uses the represented type name instead of the transmitted type name in the prototypes and stubs generated by the compiler.</span></span> <span data-ttu-id="40bc0-132">Você deve fornecer o conjunto de rotinas para ambos os lados.</span><span class="sxs-lookup"><span data-stu-id="40bc0-132">You must supply the set of routines for both sides.</span></span>

<span data-ttu-id="40bc0-133">Para objetos **de \_ tipo nomeado** temporário, o stub chamará o **\_ tipo nomeado \_ \_ Inst gratuitamente** para liberar qualquer memória alocada por uma chamada para o **\_ tipo nomeado \_ de \_ local**.</span><span class="sxs-lookup"><span data-stu-id="40bc0-133">For temporary **named\_type** objects, the stub will call **named\_type\_free\_inst** to free any memory allocated by a call to **named\_type\_from\_local**.</span></span>

<span data-ttu-id="40bc0-134">Se o tipo representado for um ponteiro ou contiver um ponteiro, **o \_ tipo nomeado \_ para rotina \_ local** deverá alocar memória para os dados aos quais os ponteiros apontam (o próprio objeto de tipo representado é manipulado pelo stub da maneira usual).</span><span class="sxs-lookup"><span data-stu-id="40bc0-134">If the represented type is a pointer or contains a pointer, the **named\_type\_to\_local** routine must allocate memory for the data to which the pointers point (the represented type object itself is manipulated by the stub in the usual way).</span></span> <span data-ttu-id="40bc0-135">Para \[ [](/windows/desktop/Midl/out-idl) \] os parâmetros out e \[ [in](/windows/desktop/Midl/in), out \] de um tipo que contém **\[ representar \_ como** ou um de seus componentes, a rotina **\_ \_ \_ local gratuita de tipo nomeado** é chamada automaticamente para os objetos de dados que contêm o atributo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-135">For \[ [out](/windows/desktop/Midl/out-idl)\] and \[ [in](/windows/desktop/Midl/in), out\] parameters of a type that contain **\[represent\_as** or one of its components, the **named\_type\_free\_local** routine is automatically called for the data objects that contain the attribute.</span></span> <span data-ttu-id="40bc0-136">Para parâmetros **\[ in \]** , a **rotina \_ \_ \_ local gratuita de tipo nomeado** será chamada somente se o atributo **\[ representar \_ como \]** tiver sido aplicado ao parâmetro.</span><span class="sxs-lookup"><span data-stu-id="40bc0-136">For **\[in\]** parameters, the **named\_type\_free\_local** routine is called only if the **\[represent\_as\]** attribute has been applied to the parameter.</span></span> <span data-ttu-id="40bc0-137">Se o atributo tiver sido aplicado aos componentes do parâmetro, a rotina *\* \*\*\* \_ \_ local \* gratuita* não será chamada.</span><span class="sxs-lookup"><span data-stu-id="40bc0-137">If the attribute has been applied to the components of the parameter, the *\*\*\*\*\_free\_local*\* routine is not called.</span></span> <span data-ttu-id="40bc0-138">As rotinas de liberação não são chamadas para os dados inseridos e para a chamada no máximo uma vez (relacionadas ao atributo de nível superior) para um parâmetro **\[ in \]** only.</span><span class="sxs-lookup"><span data-stu-id="40bc0-138">Freeing routines are not called for the embedded data and at-most-once call (related to the top-level attribute) for an **\[in\]** only parameter.</span></span>

> [!Note]  
> <span data-ttu-id="40bc0-139">É possível aplicar a **\[ transmissão \_ como \]** e **\[ representar \_ como \]** atributos para o mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="40bc0-139">It is possible to apply both the **\[transmit\_as\]** and **\[represent\_as\]** attributes to the same type.</span></span> <span data-ttu-id="40bc0-140">Ao realizar o marshaling de dados, o **\[ representar \_ como \]** conversão de tipo é aplicado primeiro e, em seguida, a **\[ transmissão \_ como \]** conversão é aplicada.</span><span class="sxs-lookup"><span data-stu-id="40bc0-140">When marshaling data, the **\[represent\_as\]** type conversion is applied first and then the **\[transmit\_as\]** conversion is applied.</span></span> <span data-ttu-id="40bc0-141">O pedido é invertido ao desempacotar dados.</span><span class="sxs-lookup"><span data-stu-id="40bc0-141">The order is reversed when unmarshaling data.</span></span> <span data-ttu-id="40bc0-142">Assim, quando o marshaling, \* **\_ de \_ local** aloca uma instância de um tipo nomeado e a traduz de um objeto de tipo local para o objeto de tipo nomeado temporário.</span><span class="sxs-lookup"><span data-stu-id="40bc0-142">Thus, when marshaling, \***\_from\_local** allocates an instance of a named type and translates it from a local type object to the temporary named type object.</span></span> <span data-ttu-id="40bc0-143">Esse objeto é o objeto de tipo apresentado usado para a rotina de \* **\_ \_ transmissão** .</span><span class="sxs-lookup"><span data-stu-id="40bc0-143">This object is the presented type object used for the \***\_to\_xmit** routine.</span></span> <span data-ttu-id="40bc0-144">A \* rotina **\_ to \_ transmissão** aloca um objeto de tipo transmitido e o traduz do objeto apresentado (nomeado) para o objeto transmitido.</span><span class="sxs-lookup"><span data-stu-id="40bc0-144">The \***\_to\_xmit** routine then allocates a transmitted type object and translates it from the presented (named) object to the transmitted object.</span></span>

 

<span data-ttu-id="40bc0-145">Uma matriz de inteiros longos pode ser usada para representar uma lista vinculada.</span><span class="sxs-lookup"><span data-stu-id="40bc0-145">An array of long integers can be used to represent a linked list.</span></span> <span data-ttu-id="40bc0-146">Dessa forma, o aplicativo manipula a lista e a transmissão usa uma matriz de inteiros longos quando uma lista desse tipo é transmitida.</span><span class="sxs-lookup"><span data-stu-id="40bc0-146">In this way, the application manipulates the list, and the transmission uses an array of long integers when a list of this type is transmitted.</span></span> <span data-ttu-id="40bc0-147">Você pode começar com uma matriz, mas usar uma construção com uma matriz aberta de inteiros longos é mais conveniente.</span><span class="sxs-lookup"><span data-stu-id="40bc0-147">You can begin with an array, but using a construct with an open array of long integers is more convenient.</span></span> <span data-ttu-id="40bc0-148">O exemplo a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="40bc0-148">The following example shows how to do this.</span></span>

``` syntax
/* IDL definitions */
 
typedef struct_lbox 
{
    long        data;
    struct_lbox *        pNext;
} LOC_BOX, * PLOC_BOX;
 
/* The definition of the local type visible to the application, 
as shown above, can be omitted in the IDL file. See the include 
in the ACF file. */
 
typedef struct_xmit_lbox 
{
    short        Size;
    [size_is(Size)] long DaraArr[];
} LONGARR;
 
void WireTheList( [in,out] LONGARR * pData );
 
/* ACF definitions */
 
/* If the IDL file does not have a definition for PLOC_BOX, you 
can still ready it for C compilation with the following include 
statement (notice that this is not a C include): 
include "local.h";*/
 
typedef [represent_as(PLOC_BOX)] LONGARR;
```

<span data-ttu-id="40bc0-149">Observe que os protótipos das rotinas que usam o tipo **LONGARR** são realmente exibidos nos arquivos stub. h como **PLOC \_ Box** no lugar do tipo **LONGARR** .</span><span class="sxs-lookup"><span data-stu-id="40bc0-149">Note that the prototypes of the routines that use the **LONGARR** type are actually displayed in the Stub.h files as **PLOC\_BOX** in place of the **LONGARR** type.</span></span> <span data-ttu-id="40bc0-150">O mesmo é verdadeiro para os stubs apropriados no arquivo de stub \_ c. c.</span><span class="sxs-lookup"><span data-stu-id="40bc0-150">The same is true of the appropriate stubs in the Stub\_c.c file.</span></span>

<span data-ttu-id="40bc0-151">Você deve fornecer as quatro funções a seguir:</span><span class="sxs-lookup"><span data-stu-id="40bc0-151">You must supply the following four functions:</span></span>

``` syntax
void __RPC_USER
LONGARR_from_local(
    PLOC_BOX __RPC_FAR * pList,
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr );
 
void __RPC_USER
LONGARR_to_local(
    LONGARR __RPC_FAR * _RPC_FAR * ppDataArr,
    PLOC_BOX __RPC_FAR * pList );
 
void __RPC_USER
LONGARR_free_inst(
    LONGARR __RPC_FAR * pDataArr);
 
void __RPC_USER
LONGARR_free_local(
    PLOC_BOX __RPC_FAR * pList );
```

<span data-ttu-id="40bc0-152">As rotinas mostradas acima fazem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="40bc0-152">The routines shown above do the following:</span></span>

-   <span data-ttu-id="40bc0-153">O **LONGARR \_ da rotina \_ local** conta os nós da lista, aloca um objeto LONGARR com o tamanho de **sizeof**(**LONGARR**) + contagem \* **sizeof**(**Long**), define o campo **tamanho** como contagem e copia os dados para o campo **DataArr** .</span><span class="sxs-lookup"><span data-stu-id="40bc0-153">The **LONGARR\_from\_local** routine counts the nodes of the list, allocates a LONGARR object with the size **sizeof**(**LONGARR**) + Count\***sizeof**(**long**), sets the **Size** field to Count, and copies the data to the **DataArr** field.</span></span>
-   <span data-ttu-id="40bc0-154">A rotina **LONGARR \_ to \_ local** cria uma lista com nós de tamanho e transfere a matriz para os nós apropriados.</span><span class="sxs-lookup"><span data-stu-id="40bc0-154">The **LONGARR\_to\_local** routine creates a list with Size nodes and transfers the array to the appropriate nodes.</span></span>
-   <span data-ttu-id="40bc0-155">A **rotina \_ \_ Inst LONGARR Free** libera nada nesse caso.</span><span class="sxs-lookup"><span data-stu-id="40bc0-155">The **LONGARR\_free\_inst** routine frees nothing in this case.</span></span>
-   <span data-ttu-id="40bc0-156">A **rotina \_ \_ local gratuita LONGARR** libera todos os nós da lista.</span><span class="sxs-lookup"><span data-stu-id="40bc0-156">The **LONGARR\_free\_local** routine frees all the nodes of the list.</span></span>

 

 