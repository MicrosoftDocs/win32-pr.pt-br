---
title: Instrução de linguagem
description: Define o idioma para todos os recursos até a próxima instrução de idioma ou para o final do arquivo.
ms.assetid: 175e27e2-903a-4aaf-89ef-532166b167e8
keywords:
- Menus de instrução de linguagem e outros recursos
topic_type:
- apiref
api_name:
- LANGUAGE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9563ba2ec00362a3b9caa3911a701919a81cae1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104499042"
---
# <a name="language-statement"></a><span data-ttu-id="b89b7-104">Instrução de linguagem</span><span class="sxs-lookup"><span data-stu-id="b89b7-104">LANGUAGE statement</span></span>

<span data-ttu-id="b89b7-105">Define o idioma para todos os recursos até a próxima instrução de **idioma** ou para o final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b89b7-105">Defines the language for all resources up to the next **LANGUAGE** statement or to the end of the file.</span></span>

<span data-ttu-id="b89b7-106">Quando a instrução de **idioma** aparece antes do início do corpo de uma definição de recurso de [**aceleradores**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)ou [**STRINGTABLE**](stringtable-resource.md) , o idioma especificado aplica-se somente a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="b89b7-106">When the **LANGUAGE** statement appears before the beginning of the body of an [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**MENU**](menu-resource.md), [**RCDATA**](rcdata-resource.md), or [**STRINGTABLE**](stringtable-resource.md) resource definition, the specified language applies only to that resource.</span></span>

``` syntax
LANGUAGE language, sublanguage
```

<dl> <dt>

<span data-ttu-id="b89b7-107"><span id="language"></span><span id="LANGUAGE"></span>*idioma*</span><span class="sxs-lookup"><span data-stu-id="b89b7-107"><span id="language"></span><span id="LANGUAGE"></span>*language*</span></span>
</dt> <dd>

<span data-ttu-id="b89b7-108">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="b89b7-108">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b89b7-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*subidioma*</span><span class="sxs-lookup"><span data-stu-id="b89b7-109"><span id="sublanguage"></span><span id="SUBLANGUAGE"></span>*sublanguage*</span></span>
</dt> <dd>

<span data-ttu-id="b89b7-110">Identificador de subidioma.</span><span class="sxs-lookup"><span data-stu-id="b89b7-110">Sublanguage identifier.</span></span>

</dd> </dl>

<span data-ttu-id="b89b7-111">Para obter mais informações, consulte [constantes e cadeias de caracteres de identificador de linguagem](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="b89b7-111">For more information, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="see-also"></a><span data-ttu-id="b89b7-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="b89b7-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89b7-113">**ACELERADORES**</span><span class="sxs-lookup"><span data-stu-id="b89b7-113">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b89b7-114">**CARACTERÍSTICAS**</span><span class="sxs-lookup"><span data-stu-id="b89b7-114">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="b89b7-115">**ADICIONARMENU**</span><span class="sxs-lookup"><span data-stu-id="b89b7-115">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b89b7-116">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="b89b7-116">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="b89b7-117">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b89b7-117">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b89b7-118">**Versão**</span><span class="sxs-lookup"><span data-stu-id="b89b7-118">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 