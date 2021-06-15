---
title: Propriedade FontName (objeto Commands)
description: Saiba mais sobre a propriedade de objeto FontName Commands. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 739fceae4e73788f408306f6af08713173c99843
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068252"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="f5817-104">Propriedade FontName (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="f5817-104">FontName Property (Commands Object)</span></span>

<span data-ttu-id="f5817-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5817-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f5817-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f5817-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f5817-107">Retorna ou define a fonte usada no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="f5817-107">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="f5817-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="f5817-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f5817-109">*agent.\***Characters("**_CharacterID_*_"). Fonte Commands.FontName_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="f5817-109">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="f5817-110">Parte</span><span class="sxs-lookup"><span data-stu-id="f5817-110">Part</span></span>   | <span data-ttu-id="f5817-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="f5817-111">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="f5817-112">*Fonte*</span><span class="sxs-lookup"><span data-stu-id="f5817-112">*Font*</span></span> | <span data-ttu-id="f5817-113">Um valor de cadeia de caracteres correspondente ao nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="f5817-113">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5817-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5817-114">Remarks</span></span>

<span data-ttu-id="f5817-115">A **propriedade FontName** define a fonte usada para exibir texto no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="f5817-115">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="f5817-116">O valor padrão para a configuração de fonte é baseado na configuração de fonte de menu para a configuração **LanguageID** do caractere ou , se isso não estiver definido, a configuração de ID de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="f5817-116">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="f5817-117">Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="f5817-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




