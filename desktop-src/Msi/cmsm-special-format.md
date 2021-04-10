---
description: Determinados valores usados com módulos de mesclagem configuráveis exigem manipulação de texto especial.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: CMSM formato especial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165241"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="7b59a-103">CMSM formato especial</span><span class="sxs-lookup"><span data-stu-id="7b59a-103">CMSM Special Format</span></span>

<span data-ttu-id="7b59a-104">Determinados valores usados com módulos de mesclagem configuráveis exigem manipulação de texto especial.</span><span class="sxs-lookup"><span data-stu-id="7b59a-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="7b59a-105">Uma cadeia de texto descrita como estando no "formato especial CMSM" trata o ponto e vírgula (;) e caracteres iguais (=) como caracteres reservados usados pela ferramenta de mesclagem do cliente ou Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="7b59a-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="7b59a-106">O formato especial CMSM é usado atualmente nos seguintes locais:</span><span class="sxs-lookup"><span data-stu-id="7b59a-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="7b59a-107">A coluna de linha da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b59a-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="7b59a-108">A coluna Value da [tabela ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="7b59a-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="7b59a-109">A coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md) quando o campo de bits é o valor na coluna de formato.</span><span class="sxs-lookup"><span data-stu-id="7b59a-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="7b59a-110">A coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md) quando Text é o valor na coluna Format e enum é o valor na coluna Type.</span><span class="sxs-lookup"><span data-stu-id="7b59a-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="7b59a-111">A coluna DefaultValue da [Tabela ModuleConfiguration](moduleconfiguration-table.md) quando Key é o valor na coluna Format.</span><span class="sxs-lookup"><span data-stu-id="7b59a-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="7b59a-112">Itens configuráveis no formato de chave usado pelo [**método ProvideTextData**](configuremodule-providetextdata.md).</span><span class="sxs-lookup"><span data-stu-id="7b59a-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="7b59a-113">Para inserir ponto e vírgulas literais ou caracteres iguais em um valor no formato especial CMSM, Prefixe o caractere com um caractere de barra invertida (' \\ ').</span><span class="sxs-lookup"><span data-stu-id="7b59a-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="7b59a-114">Uma barra invertida literal pode ser representada por duas barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="7b59a-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="7b59a-115">Um único caractere prefixado por uma única barra invertida é convertido em um único caractere, mesmo que o escape do caractere não seja necessário.</span><span class="sxs-lookup"><span data-stu-id="7b59a-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="7b59a-116">Se um ponto-e-vírgula ou caractere de igual não for prefixado por uma barra invertida, mas não tiver um comportamento definido no contexto do valor, a cadeia de caracteres resultante será indefinida.</span><span class="sxs-lookup"><span data-stu-id="7b59a-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="7b59a-117">Por exemplo, a coluna DefaultValue da Tabela ModuleConfiguration está no formato especial CMSM para todos os itens de chave porque o caractere ponto-e-vírgula é o delimitador de coluna.</span><span class="sxs-lookup"><span data-stu-id="7b59a-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="7b59a-118">Embora o caractere igual não tenha significado especial nessa cadeia de caracteres, os caracteres literais iguais ainda devem ser ignorados nessa cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="7b59a-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 



