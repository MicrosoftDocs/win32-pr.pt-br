---
title: atributo retval
description: O atributo \ retval \ designa o parâmetro que recebe o valor de retorno do membro.
ms.assetid: 3a5f1469-7828-4c38-b58f-195a47b2a66f
keywords:
- atributo retval MIDL
topic_type:
- apiref
api_name:
- retval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b53aa2b8ab66737bd4d97710fe942ee73bf0b8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823686"
---
# <a name="retval-attribute"></a><span data-ttu-id="b2328-104">atributo retval</span><span class="sxs-lookup"><span data-stu-id="b2328-104">retval attribute</span></span>

<span data-ttu-id="b2328-105">O atributo **\[ retval \]** designa o parâmetro que recebe o valor de retorno do membro.</span><span class="sxs-lookup"><span data-stu-id="b2328-105">The **\[retval\]** attribute designates the parameter that receives the return value of the member.</span></span>

``` syntax
return-type function-name(
    [out, retval [, optional-attributes]] data-type * param-name,
    ...);
```

## <a name="parameters"></a><span data-ttu-id="b2328-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2328-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2328-107">*tipo de retorno*</span><span class="sxs-lookup"><span data-stu-id="b2328-107">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b2328-108">O tipo de dados do valor de retorno do procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="b2328-108">The data type of the return value of the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="b2328-109">*nome da função*</span><span class="sxs-lookup"><span data-stu-id="b2328-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b2328-110">O nome usado para invocar o procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="b2328-110">The name used to invoke the remote procedure.</span></span>

</dd> <dt>

<span data-ttu-id="b2328-111">*opcional-atributos*</span><span class="sxs-lookup"><span data-stu-id="b2328-111">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="b2328-112">Zero ou mais atributos MIDL.</span><span class="sxs-lookup"><span data-stu-id="b2328-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="b2328-113">*tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="b2328-113">*data-type*</span></span> 
</dt> <dd>

<span data-ttu-id="b2328-114">O tipo dos dados passados pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b2328-114">The type of the data passed through the parameter.</span></span>

</dd> <dt>

<span data-ttu-id="b2328-115">*nome do parâmetro*</span><span class="sxs-lookup"><span data-stu-id="b2328-115">*param-name*</span></span> 
</dt> <dd>

<span data-ttu-id="b2328-116">O nome do identificador do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="b2328-116">The identifier name of the parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2328-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2328-117">Remarks</span></span>

<span data-ttu-id="b2328-118">Você pode usar o atributo **\[ retval \]** em parâmetros de membros de interface que descrevem métodos ou obter propriedades.</span><span class="sxs-lookup"><span data-stu-id="b2328-118">You can use the **\[retval\]** attribute on parameters of interface members that describe methods or get properties.</span></span> <span data-ttu-id="b2328-119">(O atributo é necessário no último parâmetro de um método que tem o **\[** [**propget**](propget.md) **\]** atributo.) O parâmetro deve ter o **\[** atributo [**out**](out-idl.md) **\]** e deve ser um tipo de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="b2328-119">(The attribute is required on the last parameter of a method that has the **\[**[**propget**](propget.md)**\]** attribute.) The parameter must have the **\[**[**out**](out-idl.md)**\]** attribute and must be a pointer type.</span></span>

<span data-ttu-id="b2328-120">Você não pode aplicar o **\[** atributo [**opcional**](optional.md) **\]** a um parâmetro **\[ \] retval** .</span><span class="sxs-lookup"><span data-stu-id="b2328-120">You cannot apply the **\[**[**optional**](optional.md)**\]** attribute to a **\[retval\]** parameter.</span></span>

<span data-ttu-id="b2328-121">O compilador MIDL aceita a seguinte ordenação de parâmetro (da esquerda para a direita):</span><span class="sxs-lookup"><span data-stu-id="b2328-121">The MIDL compiler accepts the following parameter ordering (from left-to-right):</span></span>

1.  <span data-ttu-id="b2328-122">Parâmetros obrigatórios (parâmetros que não têm os **\[** atributos [**DefaultValue**](defaultvalue.md) **\]** ou **\[** [**optional**](optional.md) **\]** ).</span><span class="sxs-lookup"><span data-stu-id="b2328-122">Required parameters (parameters that do not have the **\[**[**defaultvalue**](defaultvalue.md)**\]** or **\[**[**optional**](optional.md)**\]** attributes).</span></span>
2.  <span data-ttu-id="b2328-123">Parâmetros opcionais com ou sem o **\[** [](defaultvalue.md) **\]** atributo DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="b2328-123">Optional parameters with or without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
3.  <span data-ttu-id="b2328-124">Parâmetros com o **\[** atributo [**opcional**](optional.md) **\]** e sem o **\[** atributo [**DefaultValue**](defaultvalue.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="b2328-124">Parameters with the **\[**[**optional**](optional.md)**\]** attribute and without the **\[**[**defaultvalue**](defaultvalue.md)**\]** attribute.</span></span>
4.  <span data-ttu-id="b2328-125">**\[** parâmetro [**LCID**](lcid.md) **\]** , se houver.</span><span class="sxs-lookup"><span data-stu-id="b2328-125">**\[**[**lcid**](lcid.md)**\]** parameter, if any.</span></span>
5.  <span data-ttu-id="b2328-126">parâmetro **\[ retval \]** .</span><span class="sxs-lookup"><span data-stu-id="b2328-126">**\[retval\]** parameter.</span></span>

<span data-ttu-id="b2328-127">Os parâmetros com o atributo **\[ retval \]** não são exibidos em navegadores orientados ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b2328-127">Parameters with the **\[retval\]** attribute are not displayed in user-oriented browsers.</span></span>

### <a name="flags"></a><span data-ttu-id="b2328-128">Flags</span><span class="sxs-lookup"><span data-stu-id="b2328-128">Flags</span></span>

<span data-ttu-id="b2328-129">IDLFLAG \_ FRETVAL</span><span class="sxs-lookup"><span data-stu-id="b2328-129">IDLFLAG\_FRETVAL</span></span>

## <a name="examples"></a><span data-ttu-id="b2328-130">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2328-130">Examples</span></span>

``` syntax
HRESULT MyMethod([out, retval] InMyFace** ReturnVal);
HRESULT MyOtherMethod([out, retval] VARIANT_BOOL* ReturnVal);
```

## <a name="see-also"></a><span data-ttu-id="b2328-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2328-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2328-132">**ValorPadrão**</span><span class="sxs-lookup"><span data-stu-id="b2328-132">**defaultvalue**</span></span>](defaultvalue.md)
</dt> <dt>

[<span data-ttu-id="b2328-133">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="b2328-133">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="b2328-134">**LCID**</span><span class="sxs-lookup"><span data-stu-id="b2328-134">**lcid**</span></span>](lcid.md)
</dt> <dt>

[<span data-ttu-id="b2328-135">Exemplo de arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="b2328-135">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="b2328-136">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="b2328-136">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="b2328-137">**adicional**</span><span class="sxs-lookup"><span data-stu-id="b2328-137">**optional**</span></span>](optional.md)
</dt> <dt>

[<span data-ttu-id="b2328-138">**fora**</span><span class="sxs-lookup"><span data-stu-id="b2328-138">**out**</span></span>](out-idl.md)
</dt> <dt>

[<span data-ttu-id="b2328-139">**propget**</span><span class="sxs-lookup"><span data-stu-id="b2328-139">**propget**</span></span>](propget.md)
</dt> <dt>

[<span data-ttu-id="b2328-140">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="b2328-140">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 