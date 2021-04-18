---
title: Propriedade SRModeID
description: Propriedade SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105786259"
---
# <a name="srmodeid-property"></a><span data-ttu-id="350d5-103">Propriedade SRModeID</span><span class="sxs-lookup"><span data-stu-id="350d5-103">SRModeID Property</span></span>

<span data-ttu-id="350d5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="350d5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="350d5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="350d5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="350d5-106">Retorna ou define o mecanismo de reconhecimento de fala usado pelo caractere.</span><span class="sxs-lookup"><span data-stu-id="350d5-106">Returns or sets the speech recognition engine the character uses.</span></span>

</dd> <dt>

<span data-ttu-id="350d5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="350d5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="350d5-108">\*agente do ***. Caracteres ("*** characterid \* \* *").* \*  \[  =  *Modeid* SRModeID\]</span><span class="sxs-lookup"><span data-stu-id="350d5-108">*agent ***.Characters("*** CharacterID\*\*\*").SRModeID*\* \[ = *ModeID*\]</span></span>



| <span data-ttu-id="350d5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="350d5-109">Part</span></span>     | <span data-ttu-id="350d5-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="350d5-110">Description</span></span>                                                             |
|----------|-------------------------------------------------------------------------|
| <span data-ttu-id="350d5-111">*Modeid*</span><span class="sxs-lookup"><span data-stu-id="350d5-111">*ModeID*</span></span> | <span data-ttu-id="350d5-112">Uma expressão de cadeia de caracteres que corresponde à ID de modo de um mecanismo de fala.</span><span class="sxs-lookup"><span data-stu-id="350d5-112">A string expression that corresponds to the mode ID of a speech engine.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="350d5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="350d5-113">Remarks</span></span>

<span data-ttu-id="350d5-114">A propriedade determina o mecanismo de reconhecimento de fala usado pelo caractere para entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="350d5-114">The property determines the speech recognition engine used by the character for speech input.</span></span> <span data-ttu-id="350d5-115">A ID de modo para um mecanismo de reconhecimento de fala é uma cadeia de caracteres formatada definida pelo fornecedor de fala que identifica exclusivamente o mecanismo.</span><span class="sxs-lookup"><span data-stu-id="350d5-115">The mode ID for a speech recognition engine is a formatted string defined by the speech vendor that uniquely identifies the engine.</span></span> <span data-ttu-id="350d5-116">Para obter mais informações, consulte [acessando um mecanismo de fala em seu código](accessing-a-speech-engine-in-your-code.md).</span><span class="sxs-lookup"><span data-stu-id="350d5-116">For more information, see [Accessing a Speech Engine In Your Code](accessing-a-speech-engine-in-your-code.md).</span></span>

<span data-ttu-id="350d5-117">Se você especificar uma ID de modo para um mecanismo de fala que não está instalado, se o usuário tiver desabilitado o reconhecimento de fala (na folha de propriedades do Microsoft Agent) ou se o idioma do mecanismo de fala especificado não corresponder à configuração de [**LanguageID**](languageid-property.md) do caractere, o servidor gerará um erro.</span><span class="sxs-lookup"><span data-stu-id="350d5-117">If you specify a mode ID for a speech engine that isn't installed, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or if the language of the specified speech engine doesn't match the character's [**LanguageID**](languageid-property.md) setting, the server raises an error.</span></span>

<span data-ttu-id="350d5-118">Se você consultar essa propriedade e ainda não tiver (com êxito) definir o mecanismo de reconhecimento de fala, o servidor retornará a ID de modo do mecanismo que o SAPI retorna com base na configuração [**LanguageID**](languageid-property.md) do caractere.</span><span class="sxs-lookup"><span data-stu-id="350d5-118">If you query this property and haven't already (successfully) set the speech recognition engine, the server returns the mode ID of the engine that SAPI returns based on the character's [**LanguageID**](languageid-property.md) setting.</span></span> <span data-ttu-id="350d5-119">Se você não tiver definido a **LanguageID** do caractere, o Agent retornará a ID de modo do mecanismo que o SAPI retorna com base na configuração de ID de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="350d5-119">If you haven't set the character's **LanguageID**, then Agent returns the mode ID of the engine that SAPI returns based on the user's default language ID setting.</span></span> <span data-ttu-id="350d5-120">Se não houver nenhum mecanismo correspondente, o servidor retornará uma cadeia de caracteres vazia ("").</span><span class="sxs-lookup"><span data-stu-id="350d5-120">If there is no matching engine, the server returns an empty string ("").</span></span> <span data-ttu-id="350d5-121">A consulta dessa propriedade não exige que [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) seja definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="350d5-121">Querying this property does not require that [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) be set to **True**.</span></span> <span data-ttu-id="350d5-122">No entanto, se você consultar a propriedade quando a entrada de fala estiver desabilitada, o servidor retornará uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="350d5-122">However, if you query the property when speech input is disabled, the server returns an empty string.</span></span>

<span data-ttu-id="350d5-123">Quando a entrada de fala está habilitada (na janela Opções de caractere avançado), a consulta ou a configuração dessa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="350d5-123">When speech input is enabled (in the Advanced Character Options window), querying or setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="350d5-124">Ou seja, a chave de escuta está disponível e a dica de escuta é exibível.</span><span class="sxs-lookup"><span data-stu-id="350d5-124">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="350d5-125">(A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.</span><span class="sxs-lookup"><span data-stu-id="350d5-125">(The Listening key and Listening Tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="350d5-126">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="350d5-126">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="350d5-127">Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="350d5-127">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="350d5-128">Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.</span><span class="sxs-lookup"><span data-stu-id="350d5-128">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

> [!Note]  
> <span data-ttu-id="350d5-129">Essa propriedade também retornará a cadeia de caracteres vazia se você não tiver nenhum suporte de som compatível instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="350d5-129">This property also returns the empty string if you have no compatible sound support installed on your system.</span></span>

 

> [!Note]  
> <span data-ttu-id="350d5-130">A consulta dessa propriedade normalmente não retorna um erro.</span><span class="sxs-lookup"><span data-stu-id="350d5-130">Querying this property does not typically return an error.</span></span> <span data-ttu-id="350d5-131">No entanto, se o mecanismo de fala demorar muito tempo para ser carregado, você poderá receber um erro indicando que a consulta atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="350d5-131">However, if the speech engine takes an abnormally long time to load, you may get an error indicating that the query timed out.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="350d5-132">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="350d5-132">See Also</span></span>

[<span data-ttu-id="350d5-133">**Propriedade LanguageID**</span><span class="sxs-lookup"><span data-stu-id="350d5-133">**LanguageID property**</span></span>](languageid-property.md)


 

 




