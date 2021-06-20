---
title: Registrando a dependência do aplicativo (Windows Media Player SDK)
description: Saiba como registrar seu aplicativo com componentes de runtime das APIs fornecidas pelo SDK do Windows Media Player.
ms.assetid: 966683d6-e082-448d-8473-baae2311c082
keywords:
- Windows Media Player,configurações do registro de dependência do aplicativo
- Windows Media Player,configurações de registro de dependência
- Windows Media Player,Registro
- registro, configurações de dependência do aplicativo
- registro, configurações de dependência
- registry,settings for Windows Media Player
- configurações do registro de dependência
- configurações do registro de dependência do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b1692c6a4e1a8274472bbe9d718721c1ab4f1
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407359"
---
# <a name="registering-application-dependency-windows-media-player-sdk"></a><span data-ttu-id="bfa23-111">Registrando a dependência do aplicativo (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="bfa23-111">Registering Application Dependency (Windows Media Player SDK)</span></span>

<span data-ttu-id="bfa23-112">Os aplicativos que usam APIs fornecidas pelo SDK do Windows Media Player ou Windows Media Format SDK são dependentes dos componentes de runtime dessas tecnologias.</span><span class="sxs-lookup"><span data-stu-id="bfa23-112">Applications that use APIs provided by the Windows Media Player SDK or Windows Media Format SDK are dependent upon the runtime components of those technologies.</span></span> <span data-ttu-id="bfa23-113">Você pode registrar seu aplicativo como dependente desses componentes como parte da configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-113">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="bfa23-114">Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente.</span><span class="sxs-lookup"><span data-stu-id="bfa23-114">When you register your application, you can choose one of two levels of dependency: blocking or dependent.</span></span> <span data-ttu-id="bfa23-115">Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de runtime, o componente será bloqueado de uma reversões para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="bfa23-115">When one or more application is registered with a blocking dependency on one of the runtime components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="bfa23-116">Aplicativos dependentes que não estão registrados como bloqueio não bloqueiam a replicação.</span><span class="sxs-lookup"><span data-stu-id="bfa23-116">Dependent applications that are not registered as blocking do not block rollback.</span></span> <span data-ttu-id="bfa23-117">Em vez disso, antes que a replicação seja executada, é exibida uma mensagem informando que os aplicativos dependem do componente.</span><span class="sxs-lookup"><span data-stu-id="bfa23-117">Instead, before the rollback is performed, the user is displayed a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="bfa23-118">Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-118">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="bfa23-119">O valor do Registro a ser definido depende do componente do qual seu aplicativo depende.</span><span class="sxs-lookup"><span data-stu-id="bfa23-119">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="bfa23-120">Você também pode definir dois valores adicionais por dependência para fornecer informações adicionais sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-120">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="bfa23-121">Os seguintes valores de registro são usados para registrar a dependência Windows Media Player runtime do SDK:</span><span class="sxs-lookup"><span data-stu-id="bfa23-121">The following registry values are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="bfa23-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="bfa23-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="bfa23-123">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descritor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="bfa23-123">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="bfa23-124">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="bfa23-124">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="bfa23-125">Os seguintes valores do Registro são usados para registrar a dependência no runtime Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="bfa23-125">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="bfa23-126">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="bfa23-126">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="bfa23-127">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descritor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="bfa23-127">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="bfa23-128">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="bfa23-128">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\ *REF\_TYPE* \\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="bfa23-129">As seguintes variáveis são usadas nos valores do Registro listados acima:</span><span class="sxs-lookup"><span data-stu-id="bfa23-129">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="bfa23-130">*TIPO \_ REF*</span><span class="sxs-lookup"><span data-stu-id="bfa23-130">*REF\_TYPE*</span></span>

<span data-ttu-id="bfa23-131">Substitua por BlockingRefCounts para bloquear a dependência ou por DependentRefCounts para dependência sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="bfa23-131">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="bfa23-132">*APP*</span><span class="sxs-lookup"><span data-stu-id="bfa23-132">*APP*</span></span>

<span data-ttu-id="bfa23-133">Nome ou descritor curto do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-133">Name or short descriptor of your application.</span></span> <span data-ttu-id="bfa23-134">Essa cadeia de caracteres não será usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bfa23-134">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="bfa23-135">Esse valor é o identificador usado em todos os três valores do Registro associados a cada um dos componentes de runtime.</span><span class="sxs-lookup"><span data-stu-id="bfa23-135">This value is the identifier used in all three registry values associated with each of the runtime components.</span></span>

<span data-ttu-id="bfa23-136">*CADEIA DE CARACTERES DO \_ APLICATIVO*</span><span class="sxs-lookup"><span data-stu-id="bfa23-136">*APP\_STRING*</span></span>

<span data-ttu-id="bfa23-137">Descritor do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-137">Descriptor of your application.</span></span> <span data-ttu-id="bfa23-138">Essa cadeia de caracteres pode ser usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="bfa23-138">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="bfa23-139">*DESCRITOR \_ REF*</span><span class="sxs-lookup"><span data-stu-id="bfa23-139">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="bfa23-140">Descrição de como seu aplicativo usa o componente.</span><span class="sxs-lookup"><span data-stu-id="bfa23-140">Description of how your application uses the component.</span></span> <span data-ttu-id="bfa23-141">Esse valor pode incluir um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bfa23-141">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="bfa23-142">*VERSÃO DO \_ WMP*</span><span class="sxs-lookup"><span data-stu-id="bfa23-142">*WMP\_VERSION*</span></span>

<span data-ttu-id="bfa23-143">Versão do Windows Media Player exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-143">Version of Windows Media Player required by your application.</span></span> <span data-ttu-id="bfa23-144">Se nenhuma versão for especificada, o valor padrão será 9.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="bfa23-144">If no version is specified, the default value is assumed to be 9.0.0.0.</span></span>

<span data-ttu-id="bfa23-145">*VERSÃO \_ DO WMF*</span><span class="sxs-lookup"><span data-stu-id="bfa23-145">*WMF\_VERSION*</span></span>

<span data-ttu-id="bfa23-146">Versão do Windows Media Format SDK exigido pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bfa23-146">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="bfa23-147">Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="bfa23-147">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="bfa23-148">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ App, "SouthkeyVideo", "Southkey Video Player"</span><span class="sxs-lookup"><span data-stu-id="bfa23-148">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="bfa23-149">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Descriptor, "SouthkeyVideo", "Southkey Video Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="bfa23-149">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="bfa23-150">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup \\ DependentRefCounts \\ Version, "SouthkeyVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="bfa23-150">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfa23-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bfa23-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfa23-152">**Configurações do Registro**</span><span class="sxs-lookup"><span data-stu-id="bfa23-152">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




