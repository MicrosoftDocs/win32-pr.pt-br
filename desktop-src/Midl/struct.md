---
title: atributo de struct
description: A palavra-chave struct é usada em um especificador de tipo de estrutura.
ms.assetid: 89e18f0e-185a-408e-812d-3d11f228b473
keywords:
- MIDL do atributo struct
topic_type:
- apiref
api_name:
- struct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5c97ca9a2dbbfeddc5416b517e85e0926434c5d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105770389"
---
# <a name="struct-attribute"></a><span data-ttu-id="3248e-104">atributo de struct</span><span class="sxs-lookup"><span data-stu-id="3248e-104">struct attribute</span></span>

<span data-ttu-id="3248e-105">A palavra-chave **struct** é usada em um especificador de tipo de estrutura.</span><span class="sxs-lookup"><span data-stu-id="3248e-105">The **struct** keyword is used in a structure type specifier.</span></span>

``` syntax
struct [[ struct-tag ]] 
{
  [[ [ field-attribute-list ] ]] type-specifier declarator-list;
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="3248e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3248e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3248e-107">*struct-tag*</span><span class="sxs-lookup"><span data-stu-id="3248e-107">*struct-tag*</span></span> 
</dt> <dd>

<span data-ttu-id="3248e-108">Especifica uma marca opcional para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="3248e-108">Specifies an optional tag for the structure.</span></span>

</dd> <dt>

<span data-ttu-id="3248e-109">*lista de atributos de campo*</span><span class="sxs-lookup"><span data-stu-id="3248e-109">*field-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3248e-110">Especifica zero ou mais atributos de campo que se aplicam ao membro da estrutura.</span><span class="sxs-lookup"><span data-stu-id="3248e-110">Specifies zero or more field attributes that apply to the structure member.</span></span> <span data-ttu-id="3248e-111">Os atributos de campo válidos incluem **\[** [**primeiro \_**](first-is.md) **\]** , **\[** o [**último é \_**](last-is.md) **\]** , **\[** [**length \_ is**](length-is.md), **\]** **\[** [**Max \_ is**](max-is.md) **\]** e **\[** [**Size \_ is**](size-is.md) **\]** ; a cadeia de caracteres de atributos de uso **\[** [](string.md) **\]** e **\[** [**ignore**](ignore.md) **\]** ; o atributo de ponteiro **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** ou **\[** [**PTR**](ptr.md) **\]** ; e o **\[** [**\_ tipo de opção**](switch-type.md)de atributo Union **\]** .</span><span class="sxs-lookup"><span data-stu-id="3248e-111">Valid field attributes include **\[**[**first\_is**](first-is.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, and **\[**[**size\_is**](size-is.md)**\]**; the usage attributes **\[**[**string**](string.md)**\]** and **\[**[**ignore**](ignore.md)**\]**; the pointer attribute **\[**[**ref**](ref.md)**\]**, **\[**[**unique**](unique.md)**\]**, or **\[**[**ptr**](ptr.md)**\]**; and the union attribute **\[**[**switch\_type**](switch-type.md)**\]**.</span></span> <span data-ttu-id="3248e-112">Separe vários atributos de campo com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3248e-112">Separate multiple field attributes with commas.</span></span>

</dd> <dt>

<span data-ttu-id="3248e-113">*especificador de tipo*</span><span class="sxs-lookup"><span data-stu-id="3248e-113">*type-specifier*</span></span> 
</dt> <dd>

<span data-ttu-id="3248e-114">Especifica um tipo de [base](midl-base-types.md), **struct**, [**Union**](union.md)ou tipo de [**Enumeração**](enum.md) ou identificador de tipo.</span><span class="sxs-lookup"><span data-stu-id="3248e-114">Specifies a [base type](midl-base-types.md), **struct**, [**union**](union.md), or [**enum**](enum.md) type or type identifier.</span></span> <span data-ttu-id="3248e-115">Uma especificação de armazenamento opcional pode preceder o *especificador de tipo*.</span><span class="sxs-lookup"><span data-stu-id="3248e-115">An optional storage specification can precede *type-specifier*.</span></span>

</dd> <dt>

<span data-ttu-id="3248e-116">*Declarador-lista*</span><span class="sxs-lookup"><span data-stu-id="3248e-116">*declarator-list*</span></span> 
</dt> <dd>

<span data-ttu-id="3248e-117">Especifica um ou mais declaradores C padrão, como identificadores, declaradores de ponteiro e declaradores de matriz.</span><span class="sxs-lookup"><span data-stu-id="3248e-117">Specifies one or more standard C declarators, such as identifiers, pointer declarators, and array declarators.</span></span> <span data-ttu-id="3248e-118">(Os declaradores de função e as declarações de campo de bits não são permitidas em estruturas que são transmitidas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3248e-118">(Function declarators and bit-field declarations are not allowed in structures that are transmitted in remote procedure calls.</span></span> <span data-ttu-id="3248e-119">Esses declaradores são permitidos em estruturas que não são transmitidas.) Separe vários declaradores com vírgulas.</span><span class="sxs-lookup"><span data-stu-id="3248e-119">These declarators are allowed in structures that are not transmitted.) Separate multiple declarators with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3248e-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3248e-120">Remarks</span></span>

<span data-ttu-id="3248e-121">O especificador de tipo de estrutura IDL, **struct**, difere do especificador de tipo C padrão das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="3248e-121">The IDL structure type specifier, **struct**, differs from the standard C type specifier in the following ways:</span></span>

-   <span data-ttu-id="3248e-122">Cada membro da estrutura pode ser associado a atributos de campo opcionais que descrevem características desse membro da estrutura para fins de uma chamada de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3248e-122">Each structure member can be associated with optional field attributes that describe characteristics of that structure member for the purposes of a remote procedure call.</span></span>
-   <span data-ttu-id="3248e-123">Os campos de bits e os declaradores de função não são permitidos em estruturas que são usadas em chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="3248e-123">Bit fields and function declarators are not allowed in structures that are used in remote procedure calls.</span></span> <span data-ttu-id="3248e-124">Essas construções de Declarador C padrão só poderão ser usadas se a estrutura não for transmitida na rede.</span><span class="sxs-lookup"><span data-stu-id="3248e-124">These standard C declarator constructs can be used only if the structure is not transmitted on the network.</span></span>

<span data-ttu-id="3248e-125">A forma das estruturas deve ser a mesma entre as plataformas para garantir a interconectividade.</span><span class="sxs-lookup"><span data-stu-id="3248e-125">The shape of structures must be the same across platforms to ensure interconnectivity.</span></span>

## <a name="examples"></a><span data-ttu-id="3248e-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3248e-126">Examples</span></span>

``` syntax
typedef struct _PITCHER_RECORD_TYPE 
{ 
    short flag; 
    [switch_is(flag)] union PITCHER_STATISTICS_TYPE p; 
} PITCHER_RECORD_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="3248e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="3248e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3248e-128">**Storage**</span><span class="sxs-lookup"><span data-stu-id="3248e-128">**arrays**</span></span>](arrays-1.md)
</dt> <dt>

[<span data-ttu-id="3248e-129">Matrizes e ponteiros</span><span class="sxs-lookup"><span data-stu-id="3248e-129">Arrays and Pointers</span></span>](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[<span data-ttu-id="3248e-130">Atributos de matriz e de Sized-Pointer</span><span class="sxs-lookup"><span data-stu-id="3248e-130">Array and Sized-Pointer Attributes</span></span>](array-and-sized-pointer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3248e-131">Tipos base de MIDL</span><span class="sxs-lookup"><span data-stu-id="3248e-131">MIDL Base Types</span></span>](midl-base-types.md)
</dt> <dt>

[<span data-ttu-id="3248e-132">**/c \_ ext**</span><span class="sxs-lookup"><span data-stu-id="3248e-132">**/c\_ext**</span></span>](-c-ext.md)
</dt> <dt>

[<span data-ttu-id="3248e-133">**identificador de contexto \_**</span><span class="sxs-lookup"><span data-stu-id="3248e-133">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="3248e-134">**enumera**</span><span class="sxs-lookup"><span data-stu-id="3248e-134">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="3248e-135">**primeiro \_ é**</span><span class="sxs-lookup"><span data-stu-id="3248e-135">**first\_is**</span></span>](first-is.md)
</dt> <dt>

[<span data-ttu-id="3248e-136">Arquivo de definição de interface (IDL)</span><span class="sxs-lookup"><span data-stu-id="3248e-136">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="3248e-137">**ignorar**</span><span class="sxs-lookup"><span data-stu-id="3248e-137">**ignore**</span></span>](ignore.md)
</dt> <dt>

[<span data-ttu-id="3248e-138">**último \_ é**</span><span class="sxs-lookup"><span data-stu-id="3248e-138">**last\_is**</span></span>](last-is.md)
</dt> <dt>

[<span data-ttu-id="3248e-139">**comprimento \_ é**</span><span class="sxs-lookup"><span data-stu-id="3248e-139">**length\_is**</span></span>](length-is.md)
</dt> <dt>

[<span data-ttu-id="3248e-140">**máximo \_ é**</span><span class="sxs-lookup"><span data-stu-id="3248e-140">**max\_is**</span></span>](max-is.md)
</dt> <dt>

[<span data-ttu-id="3248e-141">**/osf**</span><span class="sxs-lookup"><span data-stu-id="3248e-141">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="3248e-142">**ptr**</span><span class="sxs-lookup"><span data-stu-id="3248e-142">**ptr**</span></span>](ptr.md)
</dt> <dt>

[<span data-ttu-id="3248e-143">**ref**</span><span class="sxs-lookup"><span data-stu-id="3248e-143">**ref**</span></span>](ref.md)
</dt> <dt>

[<span data-ttu-id="3248e-144">**o tamanho \_ é**</span><span class="sxs-lookup"><span data-stu-id="3248e-144">**size\_is**</span></span>](size-is.md)
</dt> <dt>

[<span data-ttu-id="3248e-145">**string**</span><span class="sxs-lookup"><span data-stu-id="3248e-145">**string**</span></span>](string.md)
</dt> <dt>

[<span data-ttu-id="3248e-146">**tipo de comutador \_**</span><span class="sxs-lookup"><span data-stu-id="3248e-146">**switch\_type**</span></span>](switch-type.md)
</dt> <dt>

[<span data-ttu-id="3248e-147">**unida**</span><span class="sxs-lookup"><span data-stu-id="3248e-147">**union**</span></span>](union.md)
</dt> <dt>

[<span data-ttu-id="3248e-148">**diferente**</span><span class="sxs-lookup"><span data-stu-id="3248e-148">**unique**</span></span>](unique.md)
</dt> </dl>

 

 