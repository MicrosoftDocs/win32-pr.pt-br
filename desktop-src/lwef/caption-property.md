---
title: Propriedade Caption (objeto Command)
description: Propriedade Caption
ms.assetid: 8dcdf3e0-3111-438b-9d39-ba9a36437ad2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0595444bd2e49ca0207c5a6a9fd459e919573958
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105771669"
---
# <a name="caption-property-command-object"></a><span data-ttu-id="8ea94-103">Propriedade Caption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="8ea94-103">Caption Property (Command Object)</span></span>

<span data-ttu-id="8ea94-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ea94-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="8ea94-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="8ea94-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="8ea94-106">Determina o texto exibido para um [**comando**](/windows/desktop/lwef/the-command-object) no menu pop-up do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="8ea94-106">Determines the text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in the specified character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="8ea94-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="8ea94-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="8ea94-108">\*Agente \***. Caracteres ("**_characterid_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Cadeia de caracteres* de legenda\]</span><span class="sxs-lookup"><span data-stu-id="8ea94-108">*agent\***.Characters ("**_CharacterID_*_").Commands("_*_name_*_").Caption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="8ea94-109">Parte</span><span class="sxs-lookup"><span data-stu-id="8ea94-109">Part</span></span>     | <span data-ttu-id="8ea94-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ea94-110">Description</span></span>                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea94-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="8ea94-111">*string*</span></span> | <span data-ttu-id="8ea94-112">Uma expressão de cadeia de caracteres que é avaliada como o texto exibido como a legenda do **comando**.</span><span class="sxs-lookup"><span data-stu-id="8ea94-112">A string expression that evaluates to the text displayed as the caption for the **Command**.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ea94-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ea94-113">Remarks</span></span>

<span data-ttu-id="8ea94-114">Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere.</span><span class="sxs-lookup"><span data-stu-id="8ea94-114">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="8ea94-115">Se você não definir um **VoiceCaption** para o comando, sua configuração de **legenda** será usada.</span><span class="sxs-lookup"><span data-stu-id="8ea94-115">If you don't define a **VoiceCaption** for your command, your **Caption** setting will be used.</span></span>

 

 
