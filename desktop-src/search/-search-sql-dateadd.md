---
description: A função DATEADD executa cálculos de data e hora para propriedades correspondentes com tipos de data. Use a função DATEADD para obter datas e horas em um período de tempo especificado antes da apresentação.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Função DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090071"
---
# <a name="dateadd-function"></a><span data-ttu-id="6c1ee-104">Função DATEADD</span><span class="sxs-lookup"><span data-stu-id="6c1ee-104">DATEADD Function</span></span>

<span data-ttu-id="6c1ee-105">A função DATEADD executa cálculos de data e hora para propriedades correspondentes com tipos de data.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="6c1ee-106">Use a função DATEADD para obter datas e horas em um período de tempo especificado antes da apresentação.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c1ee-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6c1ee-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="6c1ee-108">Argumentos</span><span class="sxs-lookup"><span data-stu-id="6c1ee-108">Arguments</span></span>

<span data-ttu-id="6c1ee-109">*DateTimeUnits*</span><span class="sxs-lookup"><span data-stu-id="6c1ee-109">*DateTimeUnits*</span></span>

<span data-ttu-id="6c1ee-110">Especifica as unidades do parâmetro de *data e hora* : ano, trimestre, mês, semana, dia, hora, minuto ou segundo.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="6c1ee-111">Esse valor diferencia maiúsculas de minúsculas e aspas não são necessárias em todo o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="6c1ee-112">*Deslocamento*</span><span class="sxs-lookup"><span data-stu-id="6c1ee-112">*OffsetValue*</span></span>

<span data-ttu-id="6c1ee-113">Especifica o deslocamento de tempo, nas unidades especificadas pelo parâmetro *DateTimeUnits* .</span><span class="sxs-lookup"><span data-stu-id="6c1ee-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="6c1ee-114">**OffsetValue** deve ser um número inteiro negativo.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="6c1ee-115">Não há suporte para valores positivos.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-115">Positive values are not supported.</span></span>

<span data-ttu-id="6c1ee-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="6c1ee-116">*DateTime*</span></span>

<span data-ttu-id="6c1ee-117">Especifica um carimbo de data/hora do qual calcular o deslocamento.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="6c1ee-118">Isso não pode ser um literal de data.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-118">This cannot be a date literal.</span></span> <span data-ttu-id="6c1ee-119">Ele deve ser GETGMTDATE ou o resultado de outra função DATEADD.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1ee-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c1ee-120">Remarks</span></span>

<span data-ttu-id="6c1ee-121">A função DATEADD pode ser usada somente em comparações de valor literal e somente no lado direito do operador de comparação.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="6c1ee-122">A função GETGMTDATE retorna a data e a hora atuais no Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="6c1ee-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="6c1ee-123">Lembre-se de que esse valor pode não ser o mesmo que o horário local do computador.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="6c1ee-124">Não use o operador de comparação Equals (=) porque a representação de tempo interna pode produzir erros de arredondamento que resultam em resultados de correspondência inesperados.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="6c1ee-125">Você pode usar várias funções de DATEADD para combinar unidades de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="6c1ee-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="6c1ee-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6c1ee-126">Examples</span></span>

<span data-ttu-id="6c1ee-127">A cláusula WHERE de exemplo a seguir corresponde aos documentos que foram modificados nos últimos cinco dias:</span><span class="sxs-lookup"><span data-stu-id="6c1ee-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="6c1ee-128">A cláusula WHERE de exemplo a seguir corresponde aos documentos que foram modificados nos últimos dois dias e quatro horas:</span><span class="sxs-lookup"><span data-stu-id="6c1ee-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="6c1ee-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c1ee-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6c1ee-130">**Referência**</span><span class="sxs-lookup"><span data-stu-id="6c1ee-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6c1ee-131">Comparação de valor literal</span><span class="sxs-lookup"><span data-stu-id="6c1ee-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="6c1ee-132">Comparações de vários valores (matriz)</span><span class="sxs-lookup"><span data-stu-id="6c1ee-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="6c1ee-133">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="6c1ee-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6c1ee-134">Predicados de texto completo</span><span class="sxs-lookup"><span data-stu-id="6c1ee-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="6c1ee-135">Predicados de texto não completo</span><span class="sxs-lookup"><span data-stu-id="6c1ee-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



