---
title: atributo propput
description: O atributo \ propput \ especifica uma função de configuração de propriedade. A propriedade deve ter o mesmo nome que a função.
ms.assetid: ffd8af15-42a4-4852-a29b-1fc66f673978
keywords:
- propput do atributo MIDL
topic_type:
- apiref
api_name:
- propput
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79bf5520a3f4f4872801145064f49a8108cf602a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084474"
---
# <a name="propput-attribute"></a><span data-ttu-id="67a45-105">atributo propput</span><span class="sxs-lookup"><span data-stu-id="67a45-105">propput attribute</span></span>

<span data-ttu-id="67a45-106">O atributo **\[ propput \]** especifica uma função de configuração de propriedade.</span><span class="sxs-lookup"><span data-stu-id="67a45-106">The **\[propput\]** attribute specifies a property-setting function.</span></span> <span data-ttu-id="67a45-107">A propriedade deve ter o mesmo nome que a função *.*</span><span class="sxs-lookup"><span data-stu-id="67a45-107">The property must have the same name as the function *.*</span></span>

``` syntax
[propput [,optional-property-attributes]] return-type function-name( parameters);
```

## <a name="parameters"></a><span data-ttu-id="67a45-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67a45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a45-109">*opcional-atributos de propriedade*</span><span class="sxs-lookup"><span data-stu-id="67a45-109">*optional-property-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="67a45-110">Zero ou mais atributos de propriedade.</span><span class="sxs-lookup"><span data-stu-id="67a45-110">Zero or more property attributes.</span></span>

</dd> <dt>

<span data-ttu-id="67a45-111">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="67a45-111">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="67a45-112">O tipo dos dados retornados pelo procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="67a45-112">The type of the data returned by the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="67a45-113">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="67a45-113">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="67a45-114">O nome do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="67a45-114">The name of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="67a45-115">*parameters*</span><span class="sxs-lookup"><span data-stu-id="67a45-115">*parameters*</span></span> 
</dt> <dd>

<span data-ttu-id="67a45-116">Zero ou mais parâmetros para o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="67a45-116">Zero or more parameters to the remote procedure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67a45-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="67a45-117">Remarks</span></span>

<span data-ttu-id="67a45-118">Uma função que tem o atributo **\[ propput \]** também deve ter, como seu último parâmetro, um parâmetro que tem o **\[** atributo [**in**](in.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="67a45-118">A function that has the **\[propput\]** attribute must also have, as its last parameter, a parameter that has the **\[**[**in**](in.md)**\]** attribute.</span></span>

<span data-ttu-id="67a45-119">No máximo, um de **\[** [**propget**](propget.md) **\]** , **\[ propput \]** e **\[** [**propputref**](propputref.md) **\]** podem ser especificados para uma função.</span><span class="sxs-lookup"><span data-stu-id="67a45-119">At most, one of **\[**[**propget**](propget.md)**\]**, **\[propput\]** and **\[**[**propputref**](propputref.md)**\]** can be specified for a function.</span></span>

<span data-ttu-id="67a45-120">Se o **\[** atributo [**LCID**](lcid.md) **\]** for usado na lista de parâmetros de uma função que contém um parâmetro com o atributo **\[ propput \]** , o parâmetro **\[ LCID \]** deverá ser segundo para o último.</span><span class="sxs-lookup"><span data-stu-id="67a45-120">If the **\[**[**lcid**](lcid.md)**\]** attribute is used in the parameter list of a function that contains a parameter with the **\[propput\]** attribute, the **\[lcid\]** parameter must be second to the last.</span></span>

### <a name="flags"></a><span data-ttu-id="67a45-121">Flags</span><span class="sxs-lookup"><span data-stu-id="67a45-121">Flags</span></span>

<span data-ttu-id="67a45-122">INVOCAr \_ PROPERTYPUT</span><span class="sxs-lookup"><span data-stu-id="67a45-122">INVOKE\_PROPERTYPUT</span></span>

## <a name="examples"></a><span data-ttu-id="67a45-123">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67a45-123">Examples</span></span>

``` syntax
interface InMyFace : IDispatch                         
{
    [propget, 
     helpstring("A meaningful comment.")] HRESULT Method1(
         [out, retval] int* ReturnVal); 

    [propput, 
     helpstring("Another meaningful comment.")] HRESULT Method1(
         [in] int Value);
}
```

## <a name="see-also"></a><span data-ttu-id="67a45-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="67a45-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a45-125">Diferenças entre MIDL e MKTYPLIB</span><span class="sxs-lookup"><span data-stu-id="67a45-125">Differences Between MIDL and MKTYPLIB</span></span>](differences-between-midl-and-mktyplib.md)
</dt> <dt>

[<span data-ttu-id="67a45-126">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="67a45-126">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="67a45-127">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="67a45-127">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="67a45-128">**propget**</span><span class="sxs-lookup"><span data-stu-id="67a45-128">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="67a45-129">**propputref**</span><span class="sxs-lookup"><span data-stu-id="67a45-129">**propputref**</span></span>](propputref.md)
</dt> <dt>

[<span data-ttu-id="67a45-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="67a45-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 