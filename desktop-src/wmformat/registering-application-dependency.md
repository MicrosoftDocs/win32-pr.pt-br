---
title: Registrando a dependência do aplicativo (Windows Media Format SDK 11)
description: Saiba como registrar seu aplicativo com componentes de runtime das APIs fornecidas pelo SDK Windows Media Format 11.
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- Windows Media Format SDK, registrando dependências de aplicativo
- registrando dependências de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cd546ee9b162652f00a131e87561a7e34f7e3a2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406159"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="6cb38-105">Registrando a dependência do aplicativo (Windows Media Format SDK 11)</span><span class="sxs-lookup"><span data-stu-id="6cb38-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="6cb38-106">Os aplicativos que usam APIs fornecidas pelo SDK Windows Media Format ou Windows Media Player SDK do Windows Media Player dependem dos componentes de tempo de run time dessas tecnologias.</span><span class="sxs-lookup"><span data-stu-id="6cb38-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="6cb38-107">Você pode registrar seu aplicativo como dependente desses componentes como parte da configuração do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="6cb38-108">Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente.</span><span class="sxs-lookup"><span data-stu-id="6cb38-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="6cb38-109">Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de tempo de executar, o componente será bloqueado de uma reversões para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="6cb38-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="6cb38-110">Aplicativos dependentes que não estão registrados como bloqueio, não bloqueiam a replicação.</span><span class="sxs-lookup"><span data-stu-id="6cb38-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="6cb38-111">Em vez disso, antes que a replicação seja executada, o usuário será solicitado com uma mensagem informando que os aplicativos dependem do componente.</span><span class="sxs-lookup"><span data-stu-id="6cb38-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="6cb38-112">Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="6cb38-113">O valor do Registro a ser definido depende do componente do qual seu aplicativo depende.</span><span class="sxs-lookup"><span data-stu-id="6cb38-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="6cb38-114">Você também pode definir dois valores adicionais por dependência para fornecer informações adicionais sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="6cb38-115">Os seguintes valores do Registro são usados para registrar a dependência no runtime Windows Media Format SDK:</span><span class="sxs-lookup"><span data-stu-id="6cb38-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="6cb38-116">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="6cb38-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="6cb38-117">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Descritor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="6cb38-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="6cb38-118">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup REF \\ \\ *\_ TYPE* \\ Version, "*APP*", "*WMF \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="6cb38-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="6cb38-119">O seguinte valor do Registro é usado para registrar a dependência Windows Media Player runtime do SDK:</span><span class="sxs-lookup"><span data-stu-id="6cb38-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="6cb38-120">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ App, "*APP*", "*APP \_ STRING*"</span><span class="sxs-lookup"><span data-stu-id="6cb38-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="6cb38-121">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Descritor, "*APP*", "*REF \_ DESCRIPTOR*"</span><span class="sxs-lookup"><span data-stu-id="6cb38-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="6cb38-122">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ MediaPlayer \\ Setup REF \\ *\_ TYPE* \\ Version, "*APP*", "*WMP \_ VERSION*"</span><span class="sxs-lookup"><span data-stu-id="6cb38-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="6cb38-123">As seguintes variáveis são usadas nos valores do Registro listados acima:</span><span class="sxs-lookup"><span data-stu-id="6cb38-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="6cb38-124">*TIPO \_ REF*</span><span class="sxs-lookup"><span data-stu-id="6cb38-124">*REF\_TYPE*</span></span>

<span data-ttu-id="6cb38-125">Substitua por BlockingRefCounts para bloquear a dependência ou por DependentRefCounts para dependência sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="6cb38-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="6cb38-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="6cb38-126">*APP*</span></span>

<span data-ttu-id="6cb38-127">Nome ou descritor curto do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="6cb38-128">Essa cadeia de caracteres não será usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6cb38-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="6cb38-129">Esse valor é o identificador usado em todos os três valores do Registro associados a cada um dos componentes de tempo de run-time.</span><span class="sxs-lookup"><span data-stu-id="6cb38-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="6cb38-130">*CADEIA DE CARACTERES DO \_ APLICATIVO*</span><span class="sxs-lookup"><span data-stu-id="6cb38-130">*APP\_STRING*</span></span>

<span data-ttu-id="6cb38-131">Descritor do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-131">Descriptor of your application.</span></span> <span data-ttu-id="6cb38-132">Essa cadeia de caracteres pode ser usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="6cb38-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="6cb38-133">*DESCRITOR \_ REF*</span><span class="sxs-lookup"><span data-stu-id="6cb38-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="6cb38-134">Descrição de como seu aplicativo usa o componente.</span><span class="sxs-lookup"><span data-stu-id="6cb38-134">Description of how your application uses the component.</span></span> <span data-ttu-id="6cb38-135">Esse valor pode incluir um máximo de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="6cb38-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="6cb38-136">*VERSÃO DO \_ WMP*</span><span class="sxs-lookup"><span data-stu-id="6cb38-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="6cb38-137">Versão do Windows Media Player exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="6cb38-138">*VERSÃO \_ DO WMF*</span><span class="sxs-lookup"><span data-stu-id="6cb38-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="6cb38-139">Versão do Windows Media Format SDK exigido pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cb38-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="6cb38-140">Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="6cb38-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="6cb38-141">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ App, "SouthkeyVideo", "Southkey Video Player"</span><span class="sxs-lookup"><span data-stu-id="6cb38-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="6cb38-142">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Descriptor, "SouthkeyVideo", "Southkey Video Player uses the Windows Media Format SDK to play video files".</span><span class="sxs-lookup"><span data-stu-id="6cb38-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="6cb38-143">HKEY \_ CLASSES ROOT Software Microsoft \_ \\ \\ \\ WindowsMedia Setup \\ \\ DependentRefCounts \\ Version, "SouthkeyVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="6cb38-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="6cb38-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cb38-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cb38-145">**Considerações sobre o projeto**</span><span class="sxs-lookup"><span data-stu-id="6cb38-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




