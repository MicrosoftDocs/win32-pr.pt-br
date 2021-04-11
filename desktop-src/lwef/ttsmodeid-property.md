---
title: Propriedade TTSModeID
description: Propriedade TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160276"
---
# <a name="ttsmodeid-property"></a><span data-ttu-id="fb147-103">Propriedade TTSModeID</span><span class="sxs-lookup"><span data-stu-id="fb147-103">TTSModeID Property</span></span>

<span data-ttu-id="fb147-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb147-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="fb147-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="fb147-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="fb147-106">Retorna ou define o modo do mecanismo de TTS usado para o caractere.</span><span class="sxs-lookup"><span data-stu-id="fb147-106">Returns or sets the TTS engine mode used for the character.</span></span>

</dd> <dt>

<span data-ttu-id="fb147-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="fb147-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="fb147-108">\*agente do ***. Caracteres ("*** characterid \* \* *").* \*  \[  =  *Modeid* TTSModeID\]</span><span class="sxs-lookup"><span data-stu-id="fb147-108">*agent ***.Characters ("*** CharacterID\*\*\*").TTSModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="fb147-109">Parte</span><span class="sxs-lookup"><span data-stu-id="fb147-109">Part</span></span>     | <span data-ttu-id="fb147-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb147-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb147-111">*Modeid*</span><span class="sxs-lookup"><span data-stu-id="fb147-111">*ModeID*</span></span> | <span data-ttu-id="fb147-112">Uma expressão de cadeia de caracteres que corresponde à ID de modo de um mecanismo de fala.</span><span class="sxs-lookup"><span data-stu-id="fb147-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb147-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fb147-113">Remarks</span></span>

<span data-ttu-id="fb147-114">Esta propriedade determina a ID do modo de mecanismo de TTS (conversão de texto em fala) para a saída falada de um caractere.</span><span class="sxs-lookup"><span data-stu-id="fb147-114">This property determines the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="fb147-115">A ID de modo para um mecanismo de TTS é uma cadeia de caracteres formatada definida pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="fb147-115">The mode ID for a TTS engine is a formatted string defined by the speech vendor that uniquely identifies the engine's mode.</span></span> <span data-ttu-id="fb147-116">Para obter mais informações, consulte [acessando um mecanismo de fala em seu código](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="fb147-116">For more information, see [Accessing a Speech Engine in Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="fb147-117">Definir essa propriedade substitui a tentativa do servidor de carregar um mecanismo com base na configuração de TTS compilada do caractere e na configuração [**LanguageID**](languageid-property.md) atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="fb147-117">Setting this property overrides the server's attempt to load an engine based on the character's compiled TTS setting and the character's current [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="fb147-118">No entanto, se você especificar uma ID de modo para um mecanismo que não está instalado ou se o usuário tiver desabilitado a saída de fala na folha de propriedades do Microsoft Agent (**AudioOutput. Enabled = False**), o servidor gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="fb147-118">However, if you specify a mode ID for an engine that isn't installed or if the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the server raises an error.</span></span>

<span data-ttu-id="fb147-119">Se você não tiver definido (ou não com êxito) uma ID de modo TTS para o caractere, o servidor verificará se a configuração do modo TTS compilado do caractere corresponde à configuração [**LanguageID**](languageid-property.md) do caractere e se o mecanismo de TTS associado está instalado.</span><span class="sxs-lookup"><span data-stu-id="fb147-119">If you do not (or have not successfully) set a TTS mode ID for the character, the server checks to see if the character's compiled TTS mode setting matches the character's [**LanguageID**](languageid-property.md) setting, and that the associated TTS engine is installed.</span></span> <span data-ttu-id="fb147-120">Nesse caso, o modo TTS usado pelo caractere para a saída falada e essa propriedade retorna essa ID de modo.</span><span class="sxs-lookup"><span data-stu-id="fb147-120">If so, the TTS mode used by the character for spoken output and this property returns that mode ID.</span></span> <span data-ttu-id="fb147-121">Caso contrário, o servidor solicitará um mecanismo de fala de SAPI compatível que corresponda à **LanguageID** do caractere, bem como o gênero e a idade definidos para a ID do modo compilado do caractere.</span><span class="sxs-lookup"><span data-stu-id="fb147-121">If not, the server requests a compatible SAPI speech engine that matches the **LanguageID** of the character, as well as the gender and age set for the character's compiled mode ID.</span></span> <span data-ttu-id="fb147-122">Se você não tiver definido o **LanguageID** do caractere, sua **LanguageID** será o idioma atual do usuário.</span><span class="sxs-lookup"><span data-stu-id="fb147-122">If you have not set the character's **LanguageID**, its **LanguageID** is the current user language.</span></span> <span data-ttu-id="fb147-123">Se nenhum mecanismo de correspondência puder ser encontrado, a consulta para essa propriedade retornará uma cadeia de caracteres vazia para a ID de modo do mecanismo.</span><span class="sxs-lookup"><span data-stu-id="fb147-123">If no matching engine can be found, querying for this property returns an empty string for the engine's mode ID.</span></span> <span data-ttu-id="fb147-124">Da mesma forma, se você consultar essa propriedade quando o usuário tiver desabilitado a saída de fala na folha de propriedades do Microsoft Agent (**AudioOutput. Enabled = False**), o valor será uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="fb147-124">Similarly, if you query this property when the user has disabled speech output in the Microsoft Agent property sheet (**AudioOutput.Enabled = False**), the value will be an empty string.</span></span>

<span data-ttu-id="fb147-125">Consultar ou definir essa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado).</span><span class="sxs-lookup"><span data-stu-id="fb147-125">Querying or setting this property will load the associated engine (if it is not already loaded).</span></span> <span data-ttu-id="fb147-126">No entanto, se o mecanismo especificado na configuração TTS compilada do caractere estiver instalado e corresponder à configuração de ID de idioma do caractere, o mecanismo será carregado quando o caractere for carregado.</span><span class="sxs-lookup"><span data-stu-id="fb147-126">However, if the engine specified in the character's compiled TTS setting is installed and matches the character's language ID setting, the engine will be loaded when the character loads.</span></span>

<span data-ttu-id="fb147-127">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="fb147-127">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="fb147-128">Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="fb147-128">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="fb147-129">Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.</span><span class="sxs-lookup"><span data-stu-id="fb147-129">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="fb147-130">Essa propriedade também retornará a cadeia de caracteres vazia se você não tiver nenhum suporte de som compatível instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="fb147-130">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb147-131">A configuração do **TTSModeID** pode falhar se o Speech.dll não estiver instalado e o mecanismo especificado não corresponder à configuração do modo TTS compilado do caractere.</span><span class="sxs-lookup"><span data-stu-id="fb147-131">Setting the **TTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

> [!Note]  
> <span data-ttu-id="fb147-132">A consulta dessa propriedade normalmente não retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="fb147-132">Querying this property does not typically return an error.</span></span> <span data-ttu-id="fb147-133">No entanto, se o mecanismo de fala demorar muito tempo para ser carregado, você poderá receber um erro indicando que a consulta atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="fb147-133">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="fb147-134">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fb147-134">See Also</span></span>

[<span data-ttu-id="fb147-135">**Propriedade LanguageID**</span><span class="sxs-lookup"><span data-stu-id="fb147-135">**LanguageID property**</span></span>](languageid-property.md)


 

 




