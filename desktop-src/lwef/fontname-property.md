---
title: Propriedade FontName (objeto Commands)
description: Propriedade FontName
ms.assetid: 7de3653e-9b4d-4a31-82d5-243f10e2743b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4b04fa386958a75b55f9cfc50a9149de454d48f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085089"
---
# <a name="fontname-property-commands-object"></a><span data-ttu-id="5d654-103">Propriedade FontName (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="5d654-103">FontName Property (Commands Object)</span></span>

<span data-ttu-id="5d654-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5d654-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5d654-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="5d654-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5d654-106">Retorna ou define a fonte usada no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="5d654-106">Returns or sets the font used in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="5d654-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="5d654-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5d654-108">\*Caracteres Agent. \***("**_characterid_\*_"). Fonte Commands. NomeDaFonte_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="5d654-108">*agent.\***Characters("**_CharacterID_*_").Commands.FontName_\* \[ = *Font*\]</span></span>



| <span data-ttu-id="5d654-109">Parte</span><span class="sxs-lookup"><span data-stu-id="5d654-109">Part</span></span>   | <span data-ttu-id="5d654-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5d654-110">Description</span></span>                                      |
|--------|--------------------------------------------------|
| <span data-ttu-id="5d654-111">*Fonte*</span><span class="sxs-lookup"><span data-stu-id="5d654-111">*Font*</span></span> | <span data-ttu-id="5d654-112">Um valor de cadeia de caracteres correspondente ao nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="5d654-112">A string value corresponding to the font's name.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d654-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d654-113">Remarks</span></span>

<span data-ttu-id="5d654-114">A propriedade **FontName** define a fonte usada para exibir o texto no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="5d654-114">The **FontName** property defines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="5d654-115">O valor padrão para a configuração fonte é baseado na configuração de fonte do menu para a configuração **LanguageID** do caractere ou, se não estiver definido, a configuração de ID de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="5d654-115">The default value for the font setting is based on the menu font setting for the character's **LanguageID** setting, or -- if that's not set -- the user default language ID setting.</span></span>

<span data-ttu-id="5d654-116">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="5d654-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 




