---
title: Usando o PlaySound para reproduzir sons do sistema
description: Usando o PlaySound para reproduzir sons do sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- áudio de onda, função PlaySound
- áudio de formato de onda, tocando sons do sistema
- áudio de onda, eventos de som
- Função PlaySound, reproduzindo sons do sistema
- Função PlaySound, eventos de som
- reprodução de Wave-sons do sistema de áudio
- eventos de som
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823763"
---
# <a name="using-playsound-to-play-system-sounds"></a><span data-ttu-id="1f06e-110">Usando o PlaySound para reproduzir sons do sistema</span><span class="sxs-lookup"><span data-stu-id="1f06e-110">Using PlaySound to Play System Sounds</span></span>

<span data-ttu-id="1f06e-111">A função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) também emitirá sons referidos por um KeyName no registro.</span><span class="sxs-lookup"><span data-stu-id="1f06e-111">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function will also play sounds referred to by a keyname in the registry.</span></span> <span data-ttu-id="1f06e-112">Os usuários podem atribuir seus próprios sons a alertas e avisos do sistema ou a ações do usuário, como um clique no botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="1f06e-112">Users can assign their own sounds to system alerts and warnings, or to user actions, such as a mouse button click.</span></span> <span data-ttu-id="1f06e-113">Os sons associados a alertas do sistema e avisos são chamados de *eventos de som*.</span><span class="sxs-lookup"><span data-stu-id="1f06e-113">Sounds that are associated with system alerts and warnings are called *sound events*.</span></span>

<span data-ttu-id="1f06e-114">Para reproduzir um evento de som, chame o **PlaySound** com o parâmetro *pszSound* apontando para uma cadeia de caracteres que contém o nome da entrada do registro que identifica o som.</span><span class="sxs-lookup"><span data-stu-id="1f06e-114">To play a sound event, call **PlaySound** with the *pszSound* parameter pointing to a string containing the name of the registry entry that identifies the sound.</span></span> <span data-ttu-id="1f06e-115">Por exemplo, para reproduzir o som associado à entrada "MouseClick" e aguardar a conclusão do som antes de retornar, use a seguinte instrução:</span><span class="sxs-lookup"><span data-stu-id="1f06e-115">For example, to play the sound associated with the "MouseClick" entry and to wait for the sound to complete before returning, use the following statement:</span></span>


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



<span data-ttu-id="1f06e-116">Se a entrada do Registro especificada ou o arquivo de wave-áudio identificado não existir, ou se o arquivo não couber na memória disponível, o **PlaySound** reproduzirá o som do sistema padrão.</span><span class="sxs-lookup"><span data-stu-id="1f06e-116">If the specified registry entry or the waveform-audio file it identifies does not exist, or if the file does not fit into the available memory, **PlaySound** plays the default system sound.</span></span>

<span data-ttu-id="1f06e-117">Os eventos de som predefinidos pelo sistema podem variar com a plataforma.</span><span class="sxs-lookup"><span data-stu-id="1f06e-117">The sound events that are predefined by the system can vary with the platform.</span></span> <span data-ttu-id="1f06e-118">A lista a seguir fornece os eventos de som que são definidos para todas as implementações da API do Win32:</span><span class="sxs-lookup"><span data-stu-id="1f06e-118">The following list gives the sound events that are defined for all implementations of the Win32 API:</span></span>

-   <span data-ttu-id="1f06e-119">SystemAsterisk</span><span class="sxs-lookup"><span data-stu-id="1f06e-119">SystemAsterisk</span></span>
-   <span data-ttu-id="1f06e-120">SystemExclamation</span><span class="sxs-lookup"><span data-stu-id="1f06e-120">SystemExclamation</span></span>
-   <span data-ttu-id="1f06e-121">SystemExit</span><span class="sxs-lookup"><span data-stu-id="1f06e-121">SystemExit</span></span>
-   <span data-ttu-id="1f06e-122">SystemHand</span><span class="sxs-lookup"><span data-stu-id="1f06e-122">SystemHand</span></span>
-   <span data-ttu-id="1f06e-123">SystemQuestion</span><span class="sxs-lookup"><span data-stu-id="1f06e-123">SystemQuestion</span></span>
-   <span data-ttu-id="1f06e-124">SystemStart</span><span class="sxs-lookup"><span data-stu-id="1f06e-124">SystemStart</span></span>

<span data-ttu-id="1f06e-125">Se um aplicativo registrar seus próprios eventos de som, o usuário poderá configurar o evento de som usando a interface padrão do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="1f06e-125">If an application registers its own sound events, the user can configure the sound event by using the standard Control Panel interface.</span></span> <span data-ttu-id="1f06e-126">O aplicativo deve registrar o evento de som usando as funções de registro padrão; para obter mais informações, consulte [registro](../sysinfo/registry.md).</span><span class="sxs-lookup"><span data-stu-id="1f06e-126">The application should register the sound event by using the standard registry functions; for more information, see [Registry](../sysinfo/registry.md).</span></span> <span data-ttu-id="1f06e-127">As entradas pertencem à mesma posição na hierarquia do registro como o restante dos eventos de som.</span><span class="sxs-lookup"><span data-stu-id="1f06e-127">The entries belong at the same position in the registry hierarchy as the rest of the sound events.</span></span> <span data-ttu-id="1f06e-128">Essa posição varia de acordo com a implementação do Win32.</span><span class="sxs-lookup"><span data-stu-id="1f06e-128">This position varies with the Win32 implementation.</span></span> <span data-ttu-id="1f06e-129">O valor de dados apropriado também varia de acordo com a implementação.</span><span class="sxs-lookup"><span data-stu-id="1f06e-129">The appropriate data value also varies with the implementation.</span></span>

<span data-ttu-id="1f06e-130">A função [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) sempre pesquisa o registro em busca de um KeyName correspondente a *lpszSound* antes de tentar carregar um arquivo com esse nome.</span><span class="sxs-lookup"><span data-stu-id="1f06e-130">The [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) function always searches the registry for a keyname matching *lpszSound* before attempting to load a file with this name.</span></span> <span data-ttu-id="1f06e-131">A função [**PlaySound**](/previous-versions//dd743680(v=vs.85)) aceita sinalizadores que especificam o local do som.</span><span class="sxs-lookup"><span data-stu-id="1f06e-131">The [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function accepts flags that specify the location of the sound.</span></span>

 

 