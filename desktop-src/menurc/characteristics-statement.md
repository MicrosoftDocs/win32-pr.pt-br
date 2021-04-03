---
title: Instrução de características
description: Define informações sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de definição de recursos.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menus de instruções de características e outros recursos
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006524"
---
# <a name="characteristics-statement"></a><span data-ttu-id="cb1bc-104">Instrução de características</span><span class="sxs-lookup"><span data-stu-id="cb1bc-104">CHARACTERISTICS statement</span></span>

<span data-ttu-id="cb1bc-105">Define informações sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de definição de recursos.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-105">Defines information about a resource that can be used by tools that read and write resource-definition files.</span></span> <span data-ttu-id="cb1bc-106">O valor **DWORD** especificado aparece com o recurso no arquivo. res compilado.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-106">The specified **DWORD** value appears with the resource in the compiled .res file.</span></span> <span data-ttu-id="cb1bc-107">No entanto, o valor não é armazenado no arquivo executável e não tem significado para o sistema.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="cb1bc-108">A instrução **características** é exibida antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**diálogo**](dialog-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="cb1bc-108">The **CHARACTERISTICS** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOG**](dialog-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="cb1bc-109">O valor especificado aplica-se somente a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-109">The specified value applies only to that resource.</span></span>

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span data-ttu-id="cb1bc-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="cb1bc-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="cb1bc-111">Valor **DWORD** definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cb1bc-111">User-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="cb1bc-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb1bc-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb1bc-113">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="cb1bc-114">**'**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-114">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="cb1bc-115">**LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="cb1bc-116">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="cb1bc-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="cb1bc-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="cb1bc-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




