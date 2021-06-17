---
title: Propriedade Caption (objeto Command)
description: Saiba mais sobre a propriedade Caption do objeto Command. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0eb41def3b183fe4185b9c66a9ca5cd172372fb
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262548"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="d9434-104">Propriedade Caption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="d9434-104">Caption Property (Command Object)</span></span>

<span data-ttu-id="d9434-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9434-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d9434-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d9434-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d9434-107">Determina o texto exibido para um [**Comando**](/windows/desktop/lwef/the-command-object) no menu pop-up do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="d9434-107">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="d9434-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="d9434-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d9434-109">*agent\***. Caracteres ("**_CharacterID_*_"). Commands("_*_name_*_"). Cadeia de_ \*  \[  =  *caracteres* de legenda\]</span><span class="sxs-lookup"><span data-stu-id="d9434-109">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="d9434-110">Parte</span><span class="sxs-lookup"><span data-stu-id="d9434-110">Part</span></span>     | <span data-ttu-id="d9434-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d9434-111">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9434-112">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="d9434-112">*string*</span></span> | <span data-ttu-id="d9434-113">Uma expressão de cadeia de caracteres que é avaliada para o texto exibido como a legenda do **Comando**.</span><span class="sxs-lookup"><span data-stu-id="d9434-113">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9434-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9434-114">Remarks</span></span>

<span data-ttu-id="d9434-115">Para especificar uma chave de acesso (mnemônico não emlindado) para a **Legenda**, inclua um caractere & (entese) antes desse caractere.</span><span class="sxs-lookup"><span data-stu-id="d9434-115">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="d9434-116">Se você não definir uma **VoiceCaption para** seu comando, a **configuração Legenda** será usada.</span><span class="sxs-lookup"><span data-stu-id="d9434-116">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
