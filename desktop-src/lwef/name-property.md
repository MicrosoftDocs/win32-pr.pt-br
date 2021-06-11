---
title: Propriedade Name (objeto Characters)
description: Saiba mais sobre a propriedade Name do objeto Characters. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7365550d5d4d4071cf4292e505f16e7047628cf1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989321"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="be379-104">Propriedade Name (objeto Characters)</span><span class="sxs-lookup"><span data-stu-id="be379-104">Name Property (Characters Object)</span></span>

<span data-ttu-id="be379-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="be379-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="be379-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be379-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="be379-107">Retorna ou define uma cadeia de caracteres que especifica o nome padrão do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="be379-107">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="be379-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="be379-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="be379-109">*agent\***. Caracteres ("**_CharacterID_*_"). Cadeia de_ \*  \[  =  *caracteres de nome*\]</span><span class="sxs-lookup"><span data-stu-id="be379-109">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="be379-110">Parte</span><span class="sxs-lookup"><span data-stu-id="be379-110">Part</span></span>     | <span data-ttu-id="be379-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="be379-111">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be379-112">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="be379-112">*string*</span></span> | <span data-ttu-id="be379-113">Um valor de cadeia de caracteres correspondente ao nome do caractere (na configuração de idioma atual).</span><span class="sxs-lookup"><span data-stu-id="be379-113">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be379-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="be379-114">Remarks</span></span>

<span data-ttu-id="be379-115">O Nome de um **caractere** pode depender da configuração [**LanguageID do**](languageid-property.md) caractere.</span><span class="sxs-lookup"><span data-stu-id="be379-115">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="be379-116">O nome de um caractere em um idioma pode ser diferente ou usar caracteres diferentes de outro.</span><span class="sxs-lookup"><span data-stu-id="be379-116">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="be379-117">O Nome padrão do caractere **para** um idioma específico é definido quando o caractere é compilado com o Editor de Caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="be379-117">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="be379-118">Evite renomear um caractere, especialmente ao usá-lo em um cenário em que outros aplicativos cliente podem usar o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="be379-118">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="be379-119">Além disso, o Agent usa o Nome **do** caractere para criar comandos automaticamente para ocultar e mostrar o caractere.</span><span class="sxs-lookup"><span data-stu-id="be379-119">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




