---
title: Instrução de versão
description: Define informações de versão sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menus de instrução de versão e outros recursos
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638572"
---
# <a name="version-statement"></a><span data-ttu-id="c2b32-104">Instrução de versão</span><span class="sxs-lookup"><span data-stu-id="c2b32-104">VERSION statement</span></span>

<span data-ttu-id="c2b32-105">Define informações de versão sobre um recurso que pode ser usado por ferramentas que lêem e gravam arquivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2b32-105">Defines version information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="c2b32-106">O valor *DWORD* especificado aparece com o recurso no compilado. Arquivo RES.</span><span class="sxs-lookup"><span data-stu-id="c2b32-106">The specified *dword* value appears with the resource in the compiled .RES file.</span></span> <span data-ttu-id="c2b32-107">No entanto, o valor não é armazenado no arquivo executável e não tem significado para o sistema.</span><span class="sxs-lookup"><span data-stu-id="c2b32-107">However, the value is not stored in the executable file and has no significance to the system.</span></span>

<span data-ttu-id="c2b32-108">A instrução de **versão** aparece antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) .</span><span class="sxs-lookup"><span data-stu-id="c2b32-108">The **VERSION** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition.</span></span> <span data-ttu-id="c2b32-109">O valor especificado aplica-se somente a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="c2b32-109">The specified value applies only to that resource.</span></span>

``` syntax
VERSION dword
```

<dl> <dt>

<span data-ttu-id="c2b32-110"><span id="dword"></span><span id="DWORD"></span>*DWORD*</span><span class="sxs-lookup"><span data-stu-id="c2b32-110"><span id="dword"></span><span id="DWORD"></span>*dword*</span></span>
</dt> <dd>

<span data-ttu-id="c2b32-111">Um valor **DWORD** definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c2b32-111">A user-defined **DWORD** value.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="c2b32-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2b32-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b32-113">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="c2b32-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="c2b32-114">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="c2b32-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="c2b32-115">**IDIOMA**</span><span class="sxs-lookup"><span data-stu-id="c2b32-115">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="c2b32-116">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="c2b32-116">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="c2b32-117">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="c2b32-117">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="c2b32-118">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="c2b32-118">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> </dl>

 

 




