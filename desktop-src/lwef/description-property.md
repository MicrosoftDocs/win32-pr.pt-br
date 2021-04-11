---
title: Propriedade Description (recursos de ambiente herdado do Windows)
description: Propriedade Description
ms.assetid: 81ac4bc7-ef0c-4e7c-b57e-acc4ad315515
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b4fb60b20a57f56a914c7e44ced957d91bf7085
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008700"
---
# <a name="description-property-legacy-windows-environment-features"></a><span data-ttu-id="606ec-103">Propriedade Description (recursos de ambiente herdado do Windows)</span><span class="sxs-lookup"><span data-stu-id="606ec-103">Description Property (Legacy Windows Environment Features)</span></span>

<span data-ttu-id="606ec-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="606ec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="606ec-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="606ec-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="606ec-106">Retorna ou define uma cadeia de caracteres que especifica a descrição do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="606ec-106">Returns or sets a string that specifies the description for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="606ec-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="606ec-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="606ec-108">*agente* do. **Caracteres ("**_characterid_*_")._* \[  =  *Cadeia de caracteres* de descrição\]</span><span class="sxs-lookup"><span data-stu-id="606ec-108">*agent*.**Characters("**_CharacterID_*_").Description_* \[ = *string*\]</span></span>



| <span data-ttu-id="606ec-109">Parte</span><span class="sxs-lookup"><span data-stu-id="606ec-109">Part</span></span>     | <span data-ttu-id="606ec-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="606ec-110">Description</span></span>                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="606ec-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="606ec-111">*string*</span></span> | <span data-ttu-id="606ec-112">Um valor de cadeia de caracteres correspondente à descrição do caractere (na configuração de idioma atual).</span><span class="sxs-lookup"><span data-stu-id="606ec-112">A string value corresponding to the character's description (in the current language setting).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="606ec-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="606ec-113">Remarks</span></span>

<span data-ttu-id="606ec-114">A **Descrição** de um caractere pode depender da configuração **LanguageID** do caractere.</span><span class="sxs-lookup"><span data-stu-id="606ec-114">A character's **Description** may depend on the character's **LanguageID** setting.</span></span> <span data-ttu-id="606ec-115">O nome de um caractere em um idioma pode ser diferente ou usar caracteres diferentes do que em outro.</span><span class="sxs-lookup"><span data-stu-id="606ec-115">A character's name in one language may be different or use different characters than in another.</span></span> <span data-ttu-id="606ec-116">A **Descrição** padrão do caractere para um idioma específico é definida quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="606ec-116">The character's default **Description** for a specific language is defined when the character is compiled with the Microsoft Agent Character Editor.</span></span>

> [!Note]  
> <span data-ttu-id="606ec-117">A configuração da propriedade **Descrição** é opcional e pode não ser fornecida para todos os caracteres.</span><span class="sxs-lookup"><span data-stu-id="606ec-117">The **Description** property setting is optional and may not be supplied for all characters.</span></span>

 

 

 




