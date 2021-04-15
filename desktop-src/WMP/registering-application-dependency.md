---
title: Registrando dependência de aplicativo (SDK do Windows Media Player)
description: Registrando dependência de aplicativo
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player, configurações de registro de dependência de aplicativo
- Windows Media Player, configurações do registro de dependência
- Windows Media Player, registro
- registro, configurações de dependência de aplicativo
- registro, configurações de dependência
- registro, configurações do Windows Media Player
- configurações do registro de dependência
- configurações do registro de dependência do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67aac78417f5ec8e4347b97a5c2b5f37db20183e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454569"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="ae0ca-111">Registrando dependência de aplicativo (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="ae0ca-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="ae0ca-112">Os aplicativos que usam as APIs fornecidas pelo SDK do Windows Media Player ou pelo SDK do Windows Media Format dependem dos componentes de tempo de execução dessas tecnologias.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="ae0ca-113">Você pode registrar seu aplicativo como dependente desses componentes como parte da instalação do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="ae0ca-114">Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="ae0ca-115">Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de tempo de execução, o componente será bloqueado de uma reversão para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="ae0ca-116">Os aplicativos dependentes que não estão registrados como bloqueios não bloqueiam a reversão.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="ae0ca-117">Em vez disso, antes da reversão ser executada, o usuário é exibido uma mensagem informando que os aplicativos dependem do componente.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="ae0ca-118">Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="ae0ca-119">O valor do registro a ser definido depende do componente no qual seu aplicativo é dependente.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="ae0ca-120">Você também pode definir dois valores adicionais por dependência para fornecer informações extras sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="ae0ca-121">Os seguintes valores de registro são usados para registrar a dependência no tempo de execução do SDK do Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="ae0ca-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="ae0ca-122">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="ae0ca-123">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *referência de \_ tipo ref* \\ , "*app*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="ae0ca-124">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMP*"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="ae0ca-125">Os seguintes valores de registro são usados para registrar a dependência no tempo de execução do SDK do Windows Media Format:</span><span class="sxs-lookup"><span data-stu-id="ae0ca-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="ae0ca-126">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="ae0ca-127">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ descritor, "*app*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="ae0ca-128">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMF*"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="ae0ca-129">As seguintes variáveis são usadas nos valores de registro listados acima:</span><span class="sxs-lookup"><span data-stu-id="ae0ca-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="ae0ca-130">*tipo de referência \_*</span><span class="sxs-lookup"><span data-stu-id="ae0ca-130">*REF\_TYPE*</span></span>

<span data-ttu-id="ae0ca-131">Substituir por BlockingRefCounts para dependência de bloqueio ou com DependentRefCounts para dependência sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="ae0ca-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="ae0ca-132">*APP*</span></span>

<span data-ttu-id="ae0ca-133">Nome ou descritor curto do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="ae0ca-134">Essa cadeia de caracteres não será usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="ae0ca-135">Esse valor é o identificador usado em todos os três valores de registro associados a cada um dos componentes de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="ae0ca-136">*Cadeia de caracteres do aplicativo \_*</span><span class="sxs-lookup"><span data-stu-id="ae0ca-136">*APP\_STRING*</span></span>

<span data-ttu-id="ae0ca-137">Descritor do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-137">Descriptor of your application.</span></span> <span data-ttu-id="ae0ca-138">Essa cadeia de caracteres pode ser usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="ae0ca-139">*\_descritor de referência*</span><span class="sxs-lookup"><span data-stu-id="ae0ca-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="ae0ca-140">Descrição de como seu aplicativo usa o componente.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-140">Description of how your application uses the component.</span></span> <span data-ttu-id="ae0ca-141">Esse valor pode incluir no máximo 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="ae0ca-142">*versão do WMP \_*</span><span class="sxs-lookup"><span data-stu-id="ae0ca-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="ae0ca-143">Versão do Windows Media Player exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="ae0ca-144">Se nenhuma versão for especificada, o valor padrão será considerado como 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="ae0ca-145">*versão do WMF \_*</span><span class="sxs-lookup"><span data-stu-id="ae0ca-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="ae0ca-146">Versão do SDK do Windows Media Format exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae0ca-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="ae0ca-147">Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ae0ca-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="ae0ca-148">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ DependentRefCounts \\ aplicativo, "SouthridgeVideo", "Player de vídeo Southridge"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="ae0ca-149">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ DependentRefCounts \\ Descriptor, "SouthridgeVideo", "Southridge player de vídeo usa o Windows Media Format SDK para reproduzir arquivos de vídeo".</span><span class="sxs-lookup"><span data-stu-id="ae0ca-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="ae0ca-150">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ DependentRefCounts \\ versão, "SouthridgeVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="ae0ca-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae0ca-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae0ca-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae0ca-152">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="ae0ca-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




