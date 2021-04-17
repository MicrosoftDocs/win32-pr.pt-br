---
description: Define alguns ou todos os atributos de caractere, glifos, larguras avançadas, posições x e y, mapeamentos de caractere para glifo e assim por diante, para uma cadeia de caracteres.
ms.assetid: aa93d631-3cfc-449d-9d04-c1f851129c6c
title: SCRIPT_STRING_ANALYSIS (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ef9bf7e2a3a592a279b593d986220350a3d8f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748992"
---
# <a name="script_string_analysis"></a><span data-ttu-id="5460b-103">\_análise de cadeia de script \_</span><span class="sxs-lookup"><span data-stu-id="5460b-103">SCRIPT\_STRING\_ANALYSIS</span></span>

<span data-ttu-id="5460b-104">Define alguns ou todos os atributos de caractere, glifos, larguras avançadas, posições x e y, mapeamentos de caractere para glifo e assim por diante, para uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5460b-104">Defines some or all of the character attributes, glyphs, advance widths, x and y positions, character-to-glyph mappings, and so forth, for a string.</span></span>


```C++
typedef void* SCRIPT_STRING_ANALYSIS;
```



## <a name="remarks"></a><span data-ttu-id="5460b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="5460b-105">Remarks</span></span>

<span data-ttu-id="5460b-106">Essa é uma estrutura opaca que é alocada dinamicamente e recuperada pelo [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span><span class="sxs-lookup"><span data-stu-id="5460b-106">This is an opaque structure that is allocated dynamically and retrieved by [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse).</span></span> <span data-ttu-id="5460b-107">Ele também é necessário para todas as outras funções \**ScriptString \** _.</span><span class="sxs-lookup"><span data-stu-id="5460b-107">It is required for all other \**ScriptString\** _ functions, as well.</span></span>

<span data-ttu-id="5460b-108">Como a análise pode ser grande, é importante que seu aplicativo chame [_ *ScriptStringFree* \*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) assim que terminar com a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5460b-108">Since the analysis can be large, it is important for your application to call [_ *ScriptStringFree*\*](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree) as soon as it has finished with the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="5460b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5460b-109">Requirements</span></span>



| <span data-ttu-id="5460b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5460b-110">Requirement</span></span> | <span data-ttu-id="5460b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5460b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5460b-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5460b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5460b-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5460b-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5460b-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5460b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5460b-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5460b-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5460b-116">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5460b-116">Redistributable</span></span><br/>          | <span data-ttu-id="5460b-117">Internet Explorer 5 ou posterior no Windows me/98/95</span><span class="sxs-lookup"><span data-stu-id="5460b-117">Internet Explorer 5 or later onWindows Me/98/95</span></span><br/>                         |
| <span data-ttu-id="5460b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5460b-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5460b-119"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5460b-119"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5460b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5460b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5460b-121">Cancelar</span><span class="sxs-lookup"><span data-stu-id="5460b-121">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="5460b-122">Estruturas do Uniscribe</span><span class="sxs-lookup"><span data-stu-id="5460b-122">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="5460b-123">**ScriptStringAnalyse**</span><span class="sxs-lookup"><span data-stu-id="5460b-123">**ScriptStringAnalyse**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)
</dt> <dt>

[<span data-ttu-id="5460b-124">**ScriptStringFree**</span><span class="sxs-lookup"><span data-stu-id="5460b-124">**ScriptStringFree**</span></span>](script-string-analysis.md)
</dt> </dl>

 

 




