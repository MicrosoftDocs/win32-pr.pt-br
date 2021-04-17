---
title: atributo helpstringcontext
description: O atributo \ helpstringcontext \ especifica um identificador de contexto de ajuda de 32 bits no arquivo de ajuda. Você pode aplicar o atributo \ helpstringcontextname a biblioteca, interface, dispinterface, módulo, coclasse, Instruções typedef, propriedades, parâmetros e métodos.
ms.assetid: 0ac41bd9-ccc6-4b5c-b925-63bff9254eed
keywords:
- helpstringcontext do atributo MIDL
topic_type:
- apiref
api_name:
- helpstringcontext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72ddded3beb768543f2f990aa9d656fba1fa8b98
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "105748787"
---
# <a name="helpstringcontext-attribute"></a><span data-ttu-id="59a46-105">atributo helpstringcontext</span><span class="sxs-lookup"><span data-stu-id="59a46-105">helpstringcontext attribute</span></span>

<span data-ttu-id="59a46-106">O atributo **\[ helpstringcontext \]** especifica um identificador de contexto de ajuda de 32 bits no arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="59a46-106">The **\[helpstringcontext\]** attribute specifies a 32-bit Help context identifier in the Help file.</span></span> <span data-ttu-id="59a46-107">Você pode aplicar o atributo **\[ \] helpstringcontext** a [**biblioteca**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**módulo**](module.md), [**coclass**](coclass.md), instruções [**typedef**](typedef.md) , propriedades, parâmetros e métodos.</span><span class="sxs-lookup"><span data-stu-id="59a46-107">You can apply the **\[helpstringcontext\]** attribute to [**library**](library.md), [**interface**](interface.md), [**dispinterface**](dispinterface.md), [**module**](module.md), [**coclass**](coclass.md), [**typedef**](typedef.md) statements, properties, parameters and methods.</span></span>

``` syntax
[  helpstringcontext(contextid)[, optional-attribute-list]] idl-statement
```

## <a name="parameters"></a><span data-ttu-id="59a46-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59a46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59a46-109">*ContextId*</span><span class="sxs-lookup"><span data-stu-id="59a46-109">*contextid*</span></span> 
</dt> <dd>

<span data-ttu-id="59a46-110">Um inteiro exclusivo que identifica o texto de ajuda associado à instrução MIDL atual.</span><span class="sxs-lookup"><span data-stu-id="59a46-110">A unique integer that identifies the help text associated with the current MIDL statement.</span></span>

</dd> <dt>

<span data-ttu-id="59a46-111">*lista de atributos opcionais*</span><span class="sxs-lookup"><span data-stu-id="59a46-111">*optional-attribute-list*</span></span> 
</dt> <dd>

<span data-ttu-id="59a46-112">Zero ou mais atributos MIDL.</span><span class="sxs-lookup"><span data-stu-id="59a46-112">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="59a46-113">*instrução IDL*</span><span class="sxs-lookup"><span data-stu-id="59a46-113">*idl-statement*</span></span> 
</dt> <dd>

<span data-ttu-id="59a46-114">A instrução MIDL à qual o atributo **\[ helpstringcontext \]** será aplicado.</span><span class="sxs-lookup"><span data-stu-id="59a46-114">The MIDL statement to which the **\[helpstringcontext\]** attribute will be applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59a46-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="59a46-115">Remarks</span></span>

<span data-ttu-id="59a46-116">Use as funções **GetDocumentation2** nas interfaces **ITypeLib2** e **ITypeInfo2** para recuperar a cadeia de caracteres de ajuda.</span><span class="sxs-lookup"><span data-stu-id="59a46-116">Use the **GetDocumentation2** functions in the **ITypeLib2** and **ITypeInfo2** interfaces to retrieve the help string.</span></span>

## <a name="examples"></a><span data-ttu-id="59a46-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="59a46-117">Examples</span></span>

``` syntax
[
    uuid(. . .),
    helpstringcontext(103),
    version(1.0)
]
library Lines
{
    [
        uuid(. . .), 
        helpstringcontext(102),
        oleautomation,
        dual
    ]
    interface ILine : IDispatch
    {
        [propget, helpstringcontext(100)] HRESULT Color([out, retval] long* ReturnVal); 
        [propput, helpstringcontext(101)] HRESULT Color([in] long rgb);
    }
};
```

 

 




