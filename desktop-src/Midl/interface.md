---
title: atributo de interface
description: A palavra-chave interface especifica o nome da interface. O nome da interface deve ser fornecido no arquivo IDL e no ACF.
ms.assetid: 239b782e-57de-493c-b2f4-310d1859a9ae
keywords:
- atributo de interface MIDL
topic_type:
- apiref
api_name:
- interface
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852c29b2ba7b43e9d8b15863e60db8ad2fbde33f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823699"
---
# <a name="interface-attribute"></a><span data-ttu-id="594ac-105">atributo de interface</span><span class="sxs-lookup"><span data-stu-id="594ac-105">interface attribute</span></span>

<span data-ttu-id="594ac-106">A palavra-chave **interface** especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="594ac-106">The **interface** keyword specifies the name of the interface.</span></span> <span data-ttu-id="594ac-107">O nome da interface deve ser fornecido no arquivo IDL e no ACF.</span><span class="sxs-lookup"><span data-stu-id="594ac-107">The interface name must be provided in both the IDL file and the ACF.</span></span>

``` syntax
[ 
    interface-attribute-list 
] 
interface interface-name [ : base-interface ]
{
}

typedef interface interface-name declarator-list
```

## <a name="parameters"></a><span data-ttu-id="594ac-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="594ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="594ac-109">*interface-atributo-lista*</span><span class="sxs-lookup"><span data-stu-id="594ac-109">*interface-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="594ac-110">Especifica os atributos que se aplicam à interface como um todo.</span><span class="sxs-lookup"><span data-stu-id="594ac-110">Specifies attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="594ac-111">Atributos de interface válidos para um arquivo IDL incluem **\[** [**ponto de extremidade**](endpoint.md) **\]** , **\[** [**local**](local.md) **\]** , **\[** [**objeto**](object.md) **\]** , **\[** [**\_ padrão de ponteiro**](pointer-default.md) **\]** , **\[** [**UUID**](uuid.md) **\]** e **\[** [**versão**](version.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="594ac-111">Valid interface attributes for an IDL file include **\[**[**endpoint**](endpoint.md)**\]**, **\[**[**local**](local.md)**\]**, **\[**[**object**](object.md)**\]**, **\[**[**pointer\_default**](pointer-default.md)**\]**, **\[**[**uuid**](uuid.md)**\]**, and **\[**[**version**](version.md)**\]**.</span></span> <span data-ttu-id="594ac-112">Atributos de interface válidos para um ACF incluem **\[** [**codificação**](encode.md) **\]** , **\[** [**decodificação**](decode.md) **\]** , **\[** [**\_ identificador automático**](auto-handle.md) **\]** ou **\[** [**\_ identificador implícito**](implicit-handle.md) **\]** e **\[** [**código**](code.md) **\]** ou **\[** [**Nocode**](nocode.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="594ac-112">Valid interface attributes for an ACF include **\[**[**encode**](encode.md)**\]**, **\[**[**decode**](decode.md)**\]**, either **\[**[**auto\_handle**](auto-handle.md)**\]** or **\[**[**implicit\_handle**](implicit-handle.md)**\]**, and either **\[**[**code**](code.md)**\]** or **\[**[**nocode**](nocode.md)**\]**.</span></span>

</dd> <dt>

<span data-ttu-id="594ac-113">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="594ac-113">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="594ac-114">Especifica o nome da interface.</span><span class="sxs-lookup"><span data-stu-id="594ac-114">Specifies the name of the interface.</span></span> <span data-ttu-id="594ac-115">O nome da interface deve ser um nome exclusivo e deve começar com um caractere alfabético ou de sublinhado.</span><span class="sxs-lookup"><span data-stu-id="594ac-115">The interface name must be a unique name and must start with an alphabetic or underscore character.</span></span>

</dd> <dt>

<span data-ttu-id="594ac-116">*interface base*</span><span class="sxs-lookup"><span data-stu-id="594ac-116">*base-interface*</span></span> 
</dt> <dd>

<span data-ttu-id="594ac-117">Especifica o nome de uma interface da qual essa interface derivada herda funções de membro, códigos de status e atributos de interface.</span><span class="sxs-lookup"><span data-stu-id="594ac-117">Specifies the name of an interface from which this derived interface inherits member functions, status codes, and interface attributes.</span></span> <span data-ttu-id="594ac-118">A interface derivada não herda definições de tipo.</span><span class="sxs-lookup"><span data-stu-id="594ac-118">The derived interface does not inherit type definitions.</span></span> <span data-ttu-id="594ac-119">Para fazer isso, use a palavra-chave [**Import**](import.md) para importar o arquivo IDL da interface base.</span><span class="sxs-lookup"><span data-stu-id="594ac-119">To do this, use the [**import**](import.md) keyword to import the IDL file of the base interface.</span></span>

</dd> <dt>

<span data-ttu-id="594ac-120">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="594ac-120">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="594ac-121">Especifica os declaradores padrão C, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="594ac-121">Specifies standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="594ac-122">Para obter mais informações, consulte [matriz e Sized-Pointer atributos](array-and-sized-pointer-attributes.md), [**matrizes**](arrays-1.md)e [matrizes e ponteiros](/windows/desktop/Rpc/arrays-and-pointers).</span><span class="sxs-lookup"><span data-stu-id="594ac-122">For more information, see [Array and Sized-Pointer Attributes](array-and-sized-pointer-attributes.md), [**arrays**](arrays-1.md)., and [Arrays and Pointers](/windows/desktop/Rpc/arrays-and-pointers).</span></span> <span data-ttu-id="594ac-123">A *lista de declaradores* consiste em um ou mais declaradores, separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="594ac-123">The *declarator-list* consists of one or more declarators, separated by commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="594ac-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="594ac-124">Remarks</span></span>

<span data-ttu-id="594ac-125">Os nomes de interface no arquivo IDL e ACF devem ser os mesmos, exceto quando você usa o switch do compilador MIDL [**/ACF**](-acf.md).</span><span class="sxs-lookup"><span data-stu-id="594ac-125">The interface names in the IDL file and ACF must be the same, except when you use the MIDL compiler switch [**/acf**](-acf.md).</span></span>

<span data-ttu-id="594ac-126">O nome da interface forma a primeira parte do nome de estruturas de dados de identificador de interface que são parâmetros para as funções de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="594ac-126">The interface name forms the first part of the name of interface-handle data structures that are parameters to the RPC run-time functions.</span></span> <span data-ttu-id="594ac-127">Para obter mais informações, consulte [**RPC \_ If \_ Handle**](/windows/desktop/Rpc/rpc-if-handle).</span><span class="sxs-lookup"><span data-stu-id="594ac-127">For more information, see [**RPC\_IF\_HANDLE**](/windows/desktop/Rpc/rpc-if-handle).</span></span>

<span data-ttu-id="594ac-128">Se o cabeçalho da interface incluir o **\[** atributo [**Object**](object.md) **\]** para indicar uma interface com, ele também deverá incluir o **\[** atributo [**UUID**](uuid.md) **\]** e deverá especificar a interface com base da qual ele é derivado.</span><span class="sxs-lookup"><span data-stu-id="594ac-128">If the interface header includes the **\[**[**object**](object.md)**\]** attribute to indicate a COM interface, it must also include the **\[**[**uuid**](uuid.md)**\]** attribute and must specify the base COM interface from which it is derived.</span></span> <span data-ttu-id="594ac-129">Para obter mais informações sobre interfaces COM, consulte **\[** [**Object**](object.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="594ac-129">For more information about COM interfaces, see **\[**[**object**](object.md)**\]**.</span></span>

<span data-ttu-id="594ac-130">Você também pode usar a palavra-chave **interface** com a palavra-chave [**typedef**](typedef.md) para definir um tipo de dados de interface.</span><span class="sxs-lookup"><span data-stu-id="594ac-130">You can also use the **interface** keyword with the [**typedef**](typedef.md) keyword to define an interface data type.</span></span>

## <a name="examples"></a><span data-ttu-id="594ac-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="594ac-131">Examples</span></span>

``` syntax
/* use of interface keyword in IDL file for an RPC interface */ 
[ 
    uuid (00000000-0000-0000-0000-000000000000), 
    version (1.0) 
] 
interface remote_if_2 
{  
    // Interface definition statements.
} 
 
/* use of interface keyword in ACF for an RPC interface */ 
[
    implicit_handle( handle_t xa_bhandle ) 
] 
interface remote_if_2 
{ 
    // Attribute configuration statements.
} 
 
/* use of interface keyword in IDL file for a COM interface */ 
[ 
    object, uuid (00000000-0000-0000-0000-000000000000) 
] 
interface IDerivedInterface : IBaseInterface 
{  
    import "base.idl" 
    Save(); 
} 
 
/* use of interface keyword to define an interface pointer type */ 
typedef interface IStorage *LPSTORAGE;
```

## <a name="see-also"></a><span data-ttu-id="594ac-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="594ac-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="594ac-133">Arquivo de configuração de aplicativo (ACF)</span><span class="sxs-lookup"><span data-stu-id="594ac-133">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="594ac-134">**extremidade**</span><span class="sxs-lookup"><span data-stu-id="594ac-134">**endpoint**</span></span>](endpoint.md)
</dt> <dt>

[<span data-ttu-id="594ac-135">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="594ac-135">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="594ac-136">**local**</span><span class="sxs-lookup"><span data-stu-id="594ac-136">**local**</span></span>](local.md)
</dt> <dt>

[<span data-ttu-id="594ac-137">**objeto**</span><span class="sxs-lookup"><span data-stu-id="594ac-137">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="594ac-138">**padrão de ponteiro \_**</span><span class="sxs-lookup"><span data-stu-id="594ac-138">**pointer\_default**</span></span>](pointer-default.md)
</dt> <dt>

[<span data-ttu-id="594ac-139">**RPC \_ se o \_ identificador**</span><span class="sxs-lookup"><span data-stu-id="594ac-139">**RPC\_IF\_HANDLE**</span></span>](/windows/desktop/Rpc/rpc-if-handle)
</dt> <dt>

[<span data-ttu-id="594ac-140">**typedef**</span><span class="sxs-lookup"><span data-stu-id="594ac-140">**typedef**</span></span>](typedef.md)
</dt> <dt>

[<span data-ttu-id="594ac-141">**personalizado**</span><span class="sxs-lookup"><span data-stu-id="594ac-141">**uuid**</span></span>](uuid.md)
</dt> <dt>

[<span data-ttu-id="594ac-142">**Versão**</span><span class="sxs-lookup"><span data-stu-id="594ac-142">**version**</span></span>](version.md)
</dt> </dl>

 

 