---
title: Propriedade SoundEffects
description: Propriedade SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca45d373d39d479c62149a131f2a6678e5ecdf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105791360"
---
# <a name="soundeffects-property"></a><span data-ttu-id="f515d-103">Propriedade SoundEffects</span><span class="sxs-lookup"><span data-stu-id="f515d-103">SoundEffects Property</span></span>

<span data-ttu-id="f515d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f515d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f515d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="f515d-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f515d-106">Retorna um valor booleano que indica se os efeitos de som (. WAV) os arquivos configurados como parte das ações de um caractere serão reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="f515d-106">Returns a Boolean indicating whether sound effects (.WAV) files configured as part of a character's actions will play.</span></span>

</dd> <dt>

<span data-ttu-id="f515d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="f515d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f515d-108">*Agent \* \* *. AudioOutput.SoundEffects**</span><span class="sxs-lookup"><span data-stu-id="f515d-108">*agent\*\*\*.AudioOutput.SoundEffects*\*</span></span>



| <span data-ttu-id="f515d-109">Valor</span><span class="sxs-lookup"><span data-stu-id="f515d-109">Value</span></span>     | <span data-ttu-id="f515d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="f515d-110">Description</span></span>                          |
|-----------|--------------------------------------|
| <span data-ttu-id="f515d-111">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="f515d-111">**True**</span></span>  | <span data-ttu-id="f515d-112">Os efeitos de som de caractere estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="f515d-112">Character sound effects are enabled.</span></span> |
| <span data-ttu-id="f515d-113">**Falso**</span><span class="sxs-lookup"><span data-stu-id="f515d-113">**False**</span></span> | <span data-ttu-id="f515d-114">O efeito de som de caractere está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f515d-114">Character sound effect are disabled.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f515d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f515d-115">Remarks</span></span>

<span data-ttu-id="f515d-116">Essa propriedade reflete a opção de efeitos sonoros de caractere de reprodução na página saída da folha de propriedades do agente (opções avançadas de caractere).</span><span class="sxs-lookup"><span data-stu-id="f515d-116">This property reflects the Play Character Sound Effects option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="f515d-117">Quando a propriedade **SoundEffects** retorna **true**, os efeitos sonoros incluídos na definição de um caractere serão reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="f515d-117">When the **SoundEffects** property returns **True**, sound effects included in a character's definition will be played.</span></span> <span data-ttu-id="f515d-118">Quando **for falso**, os efeitos sonoros não serão reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="f515d-118">When **False**, the sound effects will not be played.</span></span> <span data-ttu-id="f515d-119">A configuração da propriedade afeta todos os caracteres e é somente leitura; somente o usuário pode definir esse valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="f515d-119">The property setting affects all characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="f515d-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f515d-120">See Also</span></span>

[<span data-ttu-id="f515d-121">**Evento AgentPropertyChange**</span><span class="sxs-lookup"><span data-stu-id="f515d-121">**AgentPropertyChange event**</span></span>](agentpropertychange-event.md)


 

 




