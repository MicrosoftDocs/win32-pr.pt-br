---
title: Propriedade VoiceCaption (objeto Command)
description: Saiba mais sobre a Propriedade VoiceCaption do objeto Command, que define ou retorna o texto exibido para o objeto Command na janela Comandos de Voz.
ms.assetid: 97a3015c-6c39-42d5-b6bd-7563bd444b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d700b5d29b4c493be7382d45de55f44e6d02646c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396161"
---
# <a name="voicecaption-property-command-object"></a><span data-ttu-id="39b7e-103">Propriedade VoiceCaption (objeto Command)</span><span class="sxs-lookup"><span data-stu-id="39b7e-103">VoiceCaption Property (Command Object)</span></span>

<span data-ttu-id="39b7e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="39b7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="39b7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39b7e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="39b7e-106">Define ou retorna o texto exibido para o [**objeto Command**](/windows/desktop/lwef/the-command-object) na Janela Comandos de Voz.</span><span class="sxs-lookup"><span data-stu-id="39b7e-106">Sets or returns the text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window.</span></span>

</dd> <dt>

<span data-ttu-id="39b7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="39b7e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="39b7e-108">*agent.\***Characters("**_CharacterID_*_"). Commands("_*_Name_*_"). Cadeia de caracteres_ \*  \[  =  *VoiceCaption*\]</span><span class="sxs-lookup"><span data-stu-id="39b7e-108">*agent.\***Characters("**_CharacterID_*_").Commands("_*_Name_*_").VoiceCaption_\* \[ = *string*\]</span></span>



| <span data-ttu-id="39b7e-109">Parte</span><span class="sxs-lookup"><span data-stu-id="39b7e-109">Part</span></span>     | <span data-ttu-id="39b7e-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="39b7e-110">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="39b7e-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="39b7e-111">*string*</span></span> | <span data-ttu-id="39b7e-112">Uma expressão de cadeia de caracteres que é avaliada para o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="39b7e-112">A string expression that evaluates to the text displayed.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39b7e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="39b7e-113">Remarks</span></span>

<span data-ttu-id="39b7e-114">Se você definir um [**objeto Command**](/windows/desktop/lwef/the-command-object) em uma coleção [**Commands**](https://www.bing.com/search?q=**Commands**) e definir sua propriedade [**Voice,**](voice-property.md) normalmente também definirá sua [**propriedade VoiceCaption.**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="39b7e-114">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](https://www.bing.com/search?q=**Commands**) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="39b7e-115">Esse texto será exibido na Janela Comandos de Voz quando o aplicativo cliente estiver ativo de entrada e o caractere estiver visível.</span><span class="sxs-lookup"><span data-stu-id="39b7e-115">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="39b7e-116">Se essa propriedade não estiver definida, a configuração da propriedade [**Legenda**](caption-property.md) determinará o texto exibido.</span><span class="sxs-lookup"><span data-stu-id="39b7e-116">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="39b7e-117">Quando a **propriedade VoiceCaption** nem **Caption** não é definida, o comando não aparece na janela Comandos de Voz.</span><span class="sxs-lookup"><span data-stu-id="39b7e-117">When neither the **VoiceCaption** nor **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

### <a name="see-also"></a><span data-ttu-id="39b7e-118">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="39b7e-118">See Also</span></span>

[<span data-ttu-id="39b7e-119">**Propriedade Caption**</span><span class="sxs-lookup"><span data-stu-id="39b7e-119">**Caption property**</span></span>](caption-property.md)


 

 
