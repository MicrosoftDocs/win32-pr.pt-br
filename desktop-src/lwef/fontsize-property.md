---
title: Propriedade FontSize (objeto Commands)
description: Saiba mais sobre a propriedade de objeto de comandos FontSize. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: a1113a3a-5da8-4077-8565-168963c503d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05d4e32bf57d129e7bf1d7b45f97846a1fe90756
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068203"
---
# <a name="fontsize-property-commands-object"></a><span data-ttu-id="4051a-104">Propriedade FontSize (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="4051a-104">FontSize Property (Commands Object)</span></span>

<span data-ttu-id="4051a-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4051a-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="4051a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="4051a-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="4051a-107">Retorna ou define o tamanho da fonte usado no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="4051a-107">Returns or sets the font size used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="4051a-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="4051a-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4051a-109">\*Caracteres Agent. \***("**_characterid_\*_"). Pontos de comandos. FontSize_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="4051a-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontSize_\* \[ = *Points*\]</span></span>



| <span data-ttu-id="4051a-110">Parte</span><span class="sxs-lookup"><span data-stu-id="4051a-110">Part</span></span>     | <span data-ttu-id="4051a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="4051a-111">Description</span></span>                                              |
|----------|----------------------------------------------------------|
| <span data-ttu-id="4051a-112">*Faixas*</span><span class="sxs-lookup"><span data-stu-id="4051a-112">*Points*</span></span> | <span data-ttu-id="4051a-113">Um valor inteiro longo que especifica o tamanho da fonte em pontos.</span><span class="sxs-lookup"><span data-stu-id="4051a-113">A Long integer value specifying the font size in points.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4051a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4051a-114">Remarks</span></span>

<span data-ttu-id="4051a-115">A propriedade **FontSize** define o tamanho do ponto da fonte usada para exibir o texto no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="4051a-115">The **FontSize** property defines the point size of the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="4051a-116">O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração **LanguageID** do caractere ou — se isso não for definido — a configuração de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="4051a-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or—if that's not set—the user default language setting.</span></span>

<span data-ttu-id="4051a-117">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="4051a-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




