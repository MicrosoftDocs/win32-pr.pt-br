---
title: Propriedade VoiceCaption (objeto Commands)
description: Propriedade VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644144"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="24009-103">Propriedade VoiceCaption (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="24009-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="24009-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24009-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="24009-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="24009-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="24009-106">Retorna ou define o texto exibido para o objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) na janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="24009-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="24009-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="24009-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="24009-108">\*Caracteres Agent. \***("**_characterid_\*_"). String Commands. VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="24009-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="24009-109">Parte</span><span class="sxs-lookup"><span data-stu-id="24009-109">Part</span></span>     | <span data-ttu-id="24009-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="24009-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="24009-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="24009-111">*string*</span></span> | <span data-ttu-id="24009-112">Uma expressão de cadeia de caracteres que é avaliada como o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="24009-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24009-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="24009-113">Remarks</span></span>

<span data-ttu-id="24009-114">Se você definir a propriedade de [**voz**](voice-property.md) da coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , normalmente também definirá sua propriedade **VoiceCaption** .</span><span class="sxs-lookup"><span data-stu-id="24009-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="24009-115">A configuração texto de **VoiceCaption** aparece na janela comandos de voz quando o aplicativo cliente é de entrada-ativo e o caractere é visível.</span><span class="sxs-lookup"><span data-stu-id="24009-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="24009-116">Se essa propriedade não for definida, a configuração da propriedade [**Caption**](caption-property.md) da coleção de **comandos** determinará o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="24009-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="24009-117">Quando a propriedade **VoiceCaption** ou **Caption** for definida, os comandos na coleção aparecerão na janela de comandos de voz em "(comando indefinido)" quando o aplicativo cliente se tornar entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="24009-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="24009-118">A configuração **VoiceCaption** também determina o texto exibido na dica de escuta para indicar os comandos para os quais o caractere escuta.</span><span class="sxs-lookup"><span data-stu-id="24009-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="24009-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="24009-119">See Also</span></span>

[<span data-ttu-id="24009-120">Propriedade Caption</span><span class="sxs-lookup"><span data-stu-id="24009-120">Caption property</span></span>](caption-property.md)


 

 
