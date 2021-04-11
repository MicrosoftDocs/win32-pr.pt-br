---
title: Propriedade Enabled (objeto AudioOutput)
description: Propriedade Enabled
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008766"
---
# <a name="enabled-property-audiooutput-object"></a><span data-ttu-id="611dd-103">Propriedade Enabled (objeto AudioOutput)</span><span class="sxs-lookup"><span data-stu-id="611dd-103">Enabled Property (AudioOutput Object)</span></span>

<span data-ttu-id="611dd-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="611dd-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="611dd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="611dd-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-106">Retorna um valor booleano que indica se a saída de áudio (falada) está habilitada.</span><span class="sxs-lookup"><span data-stu-id="611dd-106">Returns a Boolean indicating whether audio (spoken) output is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="611dd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="611dd-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="611dd-108">*Agent \* \* *. AudioOutput. Enabled**</span><span class="sxs-lookup"><span data-stu-id="611dd-108">*agent\*\*\*.AudioOutput.Enabled*\*</span></span>



| <span data-ttu-id="611dd-109">Valor</span><span class="sxs-lookup"><span data-stu-id="611dd-109">Value</span></span>     | <span data-ttu-id="611dd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="611dd-110">Description</span></span>                               |
|-----------|-------------------------------------------|
| <span data-ttu-id="611dd-111">**Verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="611dd-111">**True**</span></span>  | <span data-ttu-id="611dd-112">Os A saída de áudio falada está habilitada.</span><span class="sxs-lookup"><span data-stu-id="611dd-112">(Default) Spoken audio output is enabled.</span></span> |
| <span data-ttu-id="611dd-113">**Falso**</span><span class="sxs-lookup"><span data-stu-id="611dd-113">**False**</span></span> | <span data-ttu-id="611dd-114">A saída de áudio falada está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="611dd-114">Spoken audio output is disabled.</span></span>          |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="611dd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="611dd-115">Remarks</span></span>

<span data-ttu-id="611dd-116">Essa propriedade reflete a opção reproduzir saída de áudio na página saída da folha de propriedades do agente (opções avançadas de caractere).</span><span class="sxs-lookup"><span data-stu-id="611dd-116">This property reflects the Play Audio Output option on the Output page of the Agent property sheet (Advanced Character Options).</span></span> <span data-ttu-id="611dd-117">Quando a propriedade [**Enabled**](enabled-property.md) retornar **true**, o método [**Speak**](speak-method.md) produzirá a saída de áudio se um mecanismo de TTS compatível estiver instalado ou se você usar arquivos de som para saída falada.</span><span class="sxs-lookup"><span data-stu-id="611dd-117">When the [**Enabled**](enabled-property.md) property returns **True**, the [**Speak**](speak-method.md) method produces audio output if a compatible TTS engine is installed or you use sound files for spoken output.</span></span> <span data-ttu-id="611dd-118">Quando retorna **false**, isso significa que a saída de fala não está instalada ou foi desabilitada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="611dd-118">When it returns **False**, it means that speech output is not installed or has been disabled by the user.</span></span> <span data-ttu-id="611dd-119">A configuração de propriedade aplica-se a todos os caracteres do agente e é somente leitura; somente o usuário pode definir esse valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="611dd-119">The property setting applies to all Agent characters and is read-only; only the user can set this property value.</span></span>

## <a name="see-also"></a><span data-ttu-id="611dd-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="611dd-120">See Also</span></span>

[<span data-ttu-id="611dd-121">Evento AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="611dd-121">AgentPropertyChange Event</span></span>](agentpropertychange-event.md)


 

 




