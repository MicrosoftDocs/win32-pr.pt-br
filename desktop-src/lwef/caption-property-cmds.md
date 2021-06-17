---
title: Propriedade Caption (objeto de coleção de comandos)
description: Saiba mais sobre a propriedade Caption do objeto de coleção de comandos. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 7182c21e-1ff0-4dce-9571-534b7576c082
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34ae7bd6da1fc6cc60f882cc231af5730a1077e
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262048"
---
# <a name="caption-property-commands-collection-object"></a><span data-ttu-id="ecece-104">Propriedade Caption (objeto de coleção de comandos)</span><span class="sxs-lookup"><span data-stu-id="ecece-104">Caption Property (Commands Collection Object)</span></span>

<span data-ttu-id="ecece-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ecece-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="ecece-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="ecece-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="ecece-107">Determina o texto exibido para um objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="ecece-107">Determines the text displayed for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the character's pop-up menu.</span></span>

</dd> <dt>

<span data-ttu-id="ecece-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="ecece-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="ecece-109">\*Agente \***. Caracteres ("**_characterid_\*_")._ \* Cadeia de caracteres [Commands. Caption](caption-property.md) \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="ecece-109">*agent\***.Characters ("**_CharacterID_*_")._\*[Commands.Caption](caption-property.md) \[ = *string*\]</span></span>



| <span data-ttu-id="ecece-110">Parte</span><span class="sxs-lookup"><span data-stu-id="ecece-110">Part</span></span>     | <span data-ttu-id="ecece-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="ecece-111">Description</span></span>                                                              |
|----------|--------------------------------------------------------------------------|
| <span data-ttu-id="ecece-112">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="ecece-112">*string*</span></span> | <span data-ttu-id="ecece-113">Uma expressão de cadeia de caracteres que é avaliada como o texto exibido como a legenda.</span><span class="sxs-lookup"><span data-stu-id="ecece-113">A string expression that evaluates to the text displayed as the caption.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecece-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecece-114">Remarks</span></span>

<span data-ttu-id="ecece-115">Definir a propriedade [**Caption**](caption-property.md) para sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) define como ela será exibida no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) é definida como true e seu aplicativo não é o cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="ecece-115">Setting the [**Caption**](caption-property.md) property for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection defines how it will appear on the character's pop-up menu when its [**Visible**](visible-property.md) property is set to True and your application is not the input-active client.</span></span> <span data-ttu-id="ecece-116">Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere.</span><span class="sxs-lookup"><span data-stu-id="ecece-116">To specify an access key (unlined mnemonic) for your **Caption**, include an ampersand (&) character before that character.</span></span>

<span data-ttu-id="ecece-117">Se você definir comandos para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tenha uma [**legenda**](caption-property.md), normalmente também definirá uma **legenda** para sua coleção de **comandos** associada.</span><span class="sxs-lookup"><span data-stu-id="ecece-117">If you define commands for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection that has a [**Caption**](caption-property.md), you typically also define a **Caption** for its associated **Commands** collection.</span></span>

 

 
