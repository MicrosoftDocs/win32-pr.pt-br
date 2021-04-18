---
title: atributo não extensível
description: O atributo \ extensível \ especifica que a implementação de IDispatch inclui apenas as propriedades e os métodos listados na descrição da interface e não pode ser estendido com membros adicionais em tempo de execução.
ms.assetid: 5fcffa65-4f0c-4180-a6c2-f68d63ff99ae
keywords:
- MIDL de atributo não extensível
topic_type:
- apiref
api_name:
- nonextensible
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e591ea4ab0647449ca9296b3b14a4aab9fff6991
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105752059"
---
# <a name="nonextensible-attribute"></a><span data-ttu-id="d00d0-104">atributo não extensível</span><span class="sxs-lookup"><span data-stu-id="d00d0-104">nonextensible attribute</span></span>

<span data-ttu-id="d00d0-105">O atributo **extensível \[ \]** especifica que a implementação de [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) inclui apenas as propriedades e os métodos listados na descrição da interface e não pode ser estendido com membros adicionais em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="d00d0-105">The **\[nonextensible\]** attribute specifies that the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementation includes only the properties and methods listed in the interface description and cannot be extended with additional members at run time.</span></span> <span data-ttu-id="d00d0-106">(Por padrão, a automação pressupõe que as interfaces podem adicionar membros em tempo de execução; ou seja, elas pressupõem que são extensíveis.)</span><span class="sxs-lookup"><span data-stu-id="d00d0-106">(By default, Automation assumes that interfaces may add members at run time; that is, it assumes they are extensible.)</span></span>

``` syntax
[
    uuid(uuid-number), 
    nonextensible 
    [, optional-attribute-list]
] 
interface | dispinterface interface-name 
{
    interface-definition
}
```

## <a name="parameters"></a><span data-ttu-id="d00d0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d00d0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d00d0-108">*UUID-número*</span><span class="sxs-lookup"><span data-stu-id="d00d0-108">*uuid-number*</span></span> 
</dt> <dd>

<span data-ttu-id="d00d0-109">Especifica um número de identificação universalmente exclusivo para a [**interface**](interface.md).</span><span class="sxs-lookup"><span data-stu-id="d00d0-109">Specifies a universally unique identification number for the [**interface**](interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="d00d0-110">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="d00d0-110">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="d00d0-111">Especifica uma lista de zero ou mais atributos de interface MIDL.</span><span class="sxs-lookup"><span data-stu-id="d00d0-111">Specifies a list of zero or more MIDL interface attributes.</span></span>

</dd> <dt>

<span data-ttu-id="d00d0-112">*nome da interface*</span><span class="sxs-lookup"><span data-stu-id="d00d0-112">*interface-name*</span></span> 
</dt> <dd>

<span data-ttu-id="d00d0-113">Especifica o nome da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="d00d0-113">Specifies the name of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> <dt>

<span data-ttu-id="d00d0-114">*interface-definição*</span><span class="sxs-lookup"><span data-stu-id="d00d0-114">*interface-definition*</span></span> 
</dt> <dd>

<span data-ttu-id="d00d0-115">Especifica as instruções IDL que formam a definição da [**interface**](interface.md) ou [**dispinterface**](dispinterface.md).</span><span class="sxs-lookup"><span data-stu-id="d00d0-115">Specifies IDL statements that form the definition of the [**interface**](interface.md) or [**dispinterface**](dispinterface.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d00d0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d00d0-116">Remarks</span></span>

<span data-ttu-id="d00d0-117">Você pode aplicar o atributo **\[ extensível \]** a uma interface ou uma dispinterface.</span><span class="sxs-lookup"><span data-stu-id="d00d0-117">You can apply the **\[nonextensible\]** attribute to either an interface or a dispinterface.</span></span> <span data-ttu-id="d00d0-118">No entanto, uma interface também deve ter os **\[** atributos [**Dual**](dual.md) **\]** e **\[** [**oleautomation**](oleautomation.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="d00d0-118">However, an interface must also have the **\[**[**dual**](dual.md)**\]** and **\[**[**oleautomation**](oleautomation.md)**\]** attributes.</span></span>

### <a name="flags"></a><span data-ttu-id="d00d0-119">Flags</span><span class="sxs-lookup"><span data-stu-id="d00d0-119">Flags</span></span>

<span data-ttu-id="d00d0-120">TYPEFLAG \_ FNONEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="d00d0-120">TYPEFLAG\_FNONEXTENSIBLE</span></span>

## <a name="examples"></a><span data-ttu-id="d00d0-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d00d0-121">Examples</span></span>

``` syntax
library Hello
{
    [
        uuid(12345678-1234-1234-1234-123456789ABC), 
        helpstring("A helpful description."),
        oleautomation, 
        dual, 
        nonextensible
    ] 
    interface IHello : IDispatch
    {
        // Interface definition statements.
    }
}
```

## <a name="see-also"></a><span data-ttu-id="d00d0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d00d0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00d0-123">Conteúdo de uma biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d00d0-123">Contents of a Type Library</span></span>](/previous-versions/windows/desktop/automat/contents-of-a-type-library)
</dt> <dt>

[<span data-ttu-id="d00d0-124">**dispinterface**</span><span class="sxs-lookup"><span data-stu-id="d00d0-124">**dispinterface**</span></span>](dispinterface.md)
</dt> <dt>

[<span data-ttu-id="d00d0-125">**simplifica**</span><span class="sxs-lookup"><span data-stu-id="d00d0-125">**dual**</span></span>](dual.md)
</dt> <dt>

[<span data-ttu-id="d00d0-126">Gerando uma biblioteca de tipos com MIDL</span><span class="sxs-lookup"><span data-stu-id="d00d0-126">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[<span data-ttu-id="d00d0-127">**interface**</span><span class="sxs-lookup"><span data-stu-id="d00d0-127">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="d00d0-128">Sintaxe do arquivo ODL</span><span class="sxs-lookup"><span data-stu-id="d00d0-128">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="d00d0-129">**oleautomation**</span><span class="sxs-lookup"><span data-stu-id="d00d0-129">**oleautomation**</span></span>](oleautomation.md)
</dt> <dt>

[<span data-ttu-id="d00d0-130">**TYPEFLAGS**</span><span class="sxs-lookup"><span data-stu-id="d00d0-130">**TYPEFLAGS**</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 