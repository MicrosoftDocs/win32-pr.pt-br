---
title: Propriedade Enabled (objeto AudioOutput)
description: Saiba mais sobre a propriedade de objeto AudioOutput habilitada. O Microsoft Agent foi preterido a partir do Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b807b4cadcc9a0157b4efa400dd9d0e3cb5cf21a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407339"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="09dfc-104">Propriedade Enabled (objeto AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="09dfc-104">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="09dfc-105">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09dfc-105">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="09dfc-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="09dfc-106"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="09dfc-107">Retorna um valor booleano que indica se a saída de áudio (falada) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="09dfc-107">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="09dfc-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="09dfc-108"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="09dfc-109">*Agent \* \* *. AudioOutput. Enabled**</span><span class="sxs-lookup"><span data-stu-id="09dfc-109">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="09dfc-110">Valor</span><span class="sxs-lookup"><span data-stu-id="09dfc-110">Value</span></span>     | <span data-ttu-id="09dfc-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="09dfc-111">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="09dfc-112">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="09dfc-112">**True**</span></span>  | <span data-ttu-id="09dfc-113">Os A saída de áudio falada está habilitada.</span><span class="sxs-lookup"><span data-stu-id="09dfc-113">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="09dfc-114">**Falso**</span><span class="sxs-lookup"><span data-stu-id="09dfc-114">**False**</span></span> | <span data-ttu-id="09dfc-115">A saída de áudio falada está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="09dfc-115">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09dfc-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="09dfc-116">Remarks</span></span>

<span data-ttu-id="09dfc-117">Essa propriedade reflete a opção reproduzir saída de áudio na página saída da folha de propriedades do agente (opções avançadas de caractere).</span><span class="sxs-lookup"><span data-stu-id="09dfc-117">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="09dfc-118">Quando a propriedade [**Enabled**](enabled-property.md) retornar **true**, o método [**Speak**](speak-method.md) produzirá a saída de áudio se um mecanismo de TTS compatível estiver instalado ou se você usar arquivos de som para saída falada.</span><span class="sxs-lookup"><span data-stu-id="09dfc-118">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="09dfc-119">Quando retorna **false**, isso significa que a saída de fala não está instalada ou foi desabilitada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="09dfc-119">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="09dfc-120">A configuração de propriedade aplica-se a todos os caracteres do agente e é somente leitura; somente o usuário pode definir esse valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="09dfc-120">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="09dfc-121">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="09dfc-121">See Also</span></span>

[<span data-ttu-id="09dfc-122">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="09dfc-122">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




