---
title: Propriedade VoiceCaption (objeto Commands)
description: Saiba mais sobre a Propriedade VoiceCaption do objeto Commands, que retorna ou define o texto exibido para o objeto Comandos na janela Comandos de Voz.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396121"
---
# <a name="voicecaption-property-commands-object"></a><span data-ttu-id="1ba2c-103">Propriedade VoiceCaption (objeto Commands)</span><span class="sxs-lookup"><span data-stu-id="1ba2c-103">VoiceCaption Property (Commands Object)</span></span>

<span data-ttu-id="1ba2c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1ba2c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="1ba2c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1ba2c-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="1ba2c-106">Retorna ou define o texto exibido para o objeto [**Comandos**](/windows/desktop/lwef/the-commands-collection-object) na Janela Comandos de Voz.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-106">Returns or sets the text displayed for the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="1ba2c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="1ba2c-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="1ba2c-108">*agent.\***Characters("**_CharacterID_*_"). Cadeia de caracteres Commands.VoiceCaption_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="1ba2c-108">*agent.\***Characters("**_CharacterID_*_").Commands.VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="1ba2c-109">Parte</span><span class="sxs-lookup"><span data-stu-id="1ba2c-109">Part</span></span>     | <span data-ttu-id="1ba2c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ba2c-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="1ba2c-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="1ba2c-111">*string*</span></span> | <span data-ttu-id="1ba2c-112">Uma expressão de cadeia de caracteres que é avaliada para o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ba2c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba2c-113">Remarks</span></span>

<span data-ttu-id="1ba2c-114">Se você definir a [**propriedade Voz**](voice-property.md) da coleção [**Comandos,**](/windows/desktop/lwef/the-commands-collection-object) normalmente também definirá sua **propriedade VoiceCaption.**</span><span class="sxs-lookup"><span data-stu-id="1ba2c-114">If you set the [**Voice**](voice-property.md) property of your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection, you will typically also set its **VoiceCaption** property.</span></span> <span data-ttu-id="1ba2c-115">A **configuração de texto VoiceCaption** aparece na Janela Comandos de Voz quando o aplicativo cliente está ativo de entrada e o caractere está visível.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-115">The **VoiceCaption** text setting appears in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="1ba2c-116">Se essa propriedade não estiver definida, a configuração da propriedade [**Legenda**](caption-property.md) da coleção **Comandos** determinará o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-116">If this property is not set, the setting for the **Commands** collection's [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="1ba2c-117">Quando a propriedade **VoiceCaption** ou **Caption** não estiver definida, os comandos na coleção aparecerão na Janela comandos de voz em "(comando indefinido)" quando o aplicativo cliente se tornar input-active.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-117">When neither the **VoiceCaption** or **Caption** property is set, then commands in the collection appear in the Voice Commands Window under "(undefined command)" when your client application becomes input-active.</span></span>

<span data-ttu-id="1ba2c-118">A **configuração VoiceCaption** também determina o texto exibido na Dica de Escuta para indicar os comandos para os quais o caractere escuta.</span><span class="sxs-lookup"><span data-stu-id="1ba2c-118">The **VoiceCaption** setting also determines the text displayed in the Listening Tip to indicate the commands for which the character listens.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ba2c-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1ba2c-119">See Also</span></span>

[<span data-ttu-id="1ba2c-120">Propriedade Caption</span><span class="sxs-lookup"><span data-stu-id="1ba2c-120">Caption property</span></span>](caption-property.md)


 

 
