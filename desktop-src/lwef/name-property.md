---
title: Propriedade Name (objeto characters)
description: Propriedade Name
ms.assetid: vs|msagent|~\pacontrol_2bxm.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e7b4a8872952cce0ae68445ec22a5599891674
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454520"
---
# <a name="name-property-characters-object"></a><span data-ttu-id="978c5-103">Propriedade Name (objeto characters)</span><span class="sxs-lookup"><span data-stu-id="978c5-103">Name Property (Characters Object)</span></span>

<span data-ttu-id="978c5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="978c5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="978c5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="978c5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="978c5-106">Retorna ou define uma cadeia de caracteres que especifica o nome padrão do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="978c5-106">Returns or sets a string that specifies the default name of the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="978c5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="978c5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="978c5-108">\*Agente \***. Caracteres ("**_characterid_\*_")._ \*  \[  =  *Cadeia de caracteres* de nome\]</span><span class="sxs-lookup"><span data-stu-id="978c5-108">*agent\***.Characters ("**_CharacterID_*_").Name_\* \[ = *string*\]</span></span>



| <span data-ttu-id="978c5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="978c5-109">Part</span></span>     | <span data-ttu-id="978c5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="978c5-110">Description</span></span>                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="978c5-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="978c5-111">*string*</span></span> | <span data-ttu-id="978c5-112">Um valor de cadeia de caracteres correspondente ao nome do caractere (na configuração de idioma atual).</span><span class="sxs-lookup"><span data-stu-id="978c5-112">A string value corresponding to the character's name (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="978c5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="978c5-113">Remarks</span></span>

<span data-ttu-id="978c5-114">O **nome** de um caractere pode depender da configuração [**LanguageID**](languageid-property.md) do caractere.</span><span class="sxs-lookup"><span data-stu-id="978c5-114">A character's **Name** may depend on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="978c5-115">O nome de um caractere em um idioma pode ser diferente ou usar caracteres diferentes do que em outro.</span><span class="sxs-lookup"><span data-stu-id="978c5-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="978c5-116">O **nome** padrão do caractere para um idioma específico é definido quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="978c5-116">The character's default **Name** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="978c5-117">Evite renomear um caractere, especialmente ao usá-lo em um cenário em que outros aplicativos cliente possam usar o mesmo caractere.</span><span class="sxs-lookup"><span data-stu-id="978c5-117">Avoid renaming a character, especially when using it in a scenario where other client applications may use the same character.</span></span> <span data-ttu-id="978c5-118">Além disso, o Agent usa o **nome** do caractere para criar automaticamente comandos para ocultar e mostrar o caractere.</span><span class="sxs-lookup"><span data-stu-id="978c5-118">Also, Agent uses the character's **Name** to automatically create commands for hiding and showing the character.</span></span>

 

 




