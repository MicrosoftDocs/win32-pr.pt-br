---
title: Propriedade VoiceCaption (objeto Command)
description: Propriedade VoiceCaption
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1077c8d65a52bc8f0cfa329fdceb740e30e6784
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105812371"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="34714-103">Propriedade VoiceCaption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="34714-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="34714-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="34714-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="34714-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="34714-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="34714-106">Define ou retorna o texto exibido para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) na janela comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="34714-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="34714-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="34714-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="34714-108">\*Caracteres Agent. \***("**_characterid_*_"). Comandos ("_*_Name_\*_")._ \*  \[  =  *Cadeia de caracteres* VoiceCaption\]</span><span class="sxs-lookup"><span data-stu-id="34714-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="34714-109">Parte</span><span class="sxs-lookup"><span data-stu-id="34714-109">Part</span></span>     | <span data-ttu-id="34714-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="34714-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="34714-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="34714-111">*string*</span></span> | <span data-ttu-id="34714-112">Uma expressão de cadeia de caracteres que é avaliada como o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="34714-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34714-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34714-113">Remarks</span></span>

<span data-ttu-id="34714-114">Se você definir um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](https://www.bing.com/search?q=**Commands**) e definir sua propriedade de [**voz**](voice-property.md) , normalmente também definirá sua propriedade [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="34714-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="34714-115">Esse texto será exibido na janela de comandos de voz quando o aplicativo cliente for de entrada-ativo e o caractere estiver visível.</span><span class="sxs-lookup"><span data-stu-id="34714-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="34714-116">Se essa propriedade não for definida, a configuração da propriedade [**Caption**](caption-property.md) determinará o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="34714-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="34714-117">Quando nem a propriedade **VoiceCaption** nem **Caption** é definida, o comando não aparece na janela de comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="34714-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="34714-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="34714-118">See Also</span></span>

[<span data-ttu-id="34714-119">**Propriedade Caption**</span><span class="sxs-lookup"><span data-stu-id="34714-119">**Caption property**</span></span>](caption-property.md)


 

 
