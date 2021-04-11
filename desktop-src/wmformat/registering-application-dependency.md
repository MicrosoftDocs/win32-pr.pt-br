---
title: Registrando a dependência do aplicativo (SDK do Windows Media Format 11)
description: Registrando dependência de aplicativo
ms.assetid: 09f63519-5c65-4784-9ea4-4fbecfa6d4aa
keywords:
- SDK do Windows Media Format, registrando dependências do aplicativo
- registrando dependências de aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090cf61d32597800b52e2bc112d2bee1cc1b7cd7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008674"
---
# <a name="registering-application-dependency-windows-media-format-11-sdk"></a><span data-ttu-id="ea1ea-105">Registrando a dependência do aplicativo (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="ea1ea-105">Registering Application Dependency (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="ea1ea-106">Os aplicativos que usam APIs fornecidas pelo SDK do Windows Media Format ou do Windows Media Player dependem dos componentes de tempo de execução dessas tecnologias.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-106">Applications that use APIs provided by the Windows Media Format SDK or Windows Media Player SDK are dependent upon the run-time components of those technologies.</span></span> <span data-ttu-id="ea1ea-107">Você pode registrar seu aplicativo como dependente desses componentes como parte da instalação do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-107">You can register your application as being dependent on those components as part of your application setup.</span></span>

<span data-ttu-id="ea1ea-108">Ao registrar seu aplicativo, você pode escolher um dos dois níveis de dependência: bloqueio ou dependente.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-108">When you register your application, you can choose one of two levels of dependency: blocking, or dependent.</span></span> <span data-ttu-id="ea1ea-109">Quando um ou mais aplicativos são registrados com uma dependência de bloqueio em um dos componentes de tempo de execução, o componente será bloqueado de uma reversão para uma versão anterior.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-109">When one or more applications are registered with a blocking dependency on one of the run-time components, the component will be blocked from a rollback to a previous version.</span></span> <span data-ttu-id="ea1ea-110">Os aplicativos dependentes que não estão registrados como bloqueios não bloqueiam a reversão.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-110">Dependent applications that are not registered as blocking, do not block rollback.</span></span> <span data-ttu-id="ea1ea-111">Em vez disso, antes da reversão ser executada, o usuário receberá uma mensagem informando que os aplicativos dependem do componente.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-111">Instead, before the rollback is performed, the user is prompted with a message stating that applications are dependent on the component.</span></span>

<span data-ttu-id="ea1ea-112">Para registrar seu aplicativo, você deve definir um valor no registro que identifica seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-112">To register your application, you must set a value in the registry that identifies your application.</span></span> <span data-ttu-id="ea1ea-113">O valor do registro a ser definido depende do componente no qual seu aplicativo é dependente.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-113">The registry value to set depends on the component on which your application is dependent.</span></span> <span data-ttu-id="ea1ea-114">Você também pode definir dois valores adicionais por dependência para fornecer informações extras sobre seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-114">You can also set two additional values per dependency to provide extra information about your application.</span></span>

<span data-ttu-id="ea1ea-115">Os seguintes valores de registro são usados para registrar a dependência no tempo de execução do SDK do Windows Media Format:</span><span class="sxs-lookup"><span data-stu-id="ea1ea-115">The following registry values are used to register dependence on the Windows Media Format SDK runtime:</span></span>

-   <span data-ttu-id="ea1ea-116">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-116">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="ea1ea-117">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ descritor, "*app*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-117">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="ea1ea-118">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMF*"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-118">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMF\_VERSION*"</span></span>

<span data-ttu-id="ea1ea-119">O seguinte valor de registro é usado para registrar a dependência no tempo de execução do SDK do Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="ea1ea-119">The following registry value are used to register dependence on Windows Media Player SDK runtime:</span></span>

-   <span data-ttu-id="ea1ea-120">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *\_ tipo de referência* \\ aplicativo, "*app*", "*app \_ String*"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-120">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\App, "*APP*", "*APP\_STRING*"</span></span>
-   <span data-ttu-id="ea1ea-121">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *referência de \_ tipo ref* \\ , "*app*", "*ref \_ Descriptor*"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-121">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Descriptor, "*APP*", "*REF\_DESCRIPTOR*"</span></span>
-   <span data-ttu-id="ea1ea-122">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ MediaPlayer \\ instalação \\ *\_ tipo de referência* \\ versão, "*aplicativo*",*" \_ versão do WMP*"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-122">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\MediaPlayer\\Setup\\*REF\_TYPE*\\Version, "*APP*", "*WMP\_VERSION*"</span></span>

<span data-ttu-id="ea1ea-123">As seguintes variáveis são usadas nos valores de registro listados acima:</span><span class="sxs-lookup"><span data-stu-id="ea1ea-123">The following variables are used in the registry values listed above:</span></span>

<span data-ttu-id="ea1ea-124">*tipo de referência \_*</span><span class="sxs-lookup"><span data-stu-id="ea1ea-124">*REF\_TYPE*</span></span>

<span data-ttu-id="ea1ea-125">Substituir por BlockingRefCounts para dependência de bloqueio ou com DependentRefCounts para dependência sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-125">Replace with BlockingRefCounts for blocking dependency, or with DependentRefCounts for non-blocking dependency.</span></span>

<span data-ttu-id="ea1ea-126">*APP*</span><span class="sxs-lookup"><span data-stu-id="ea1ea-126">*APP*</span></span>

<span data-ttu-id="ea1ea-127">Nome ou descritor curto do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-127">Name or short descriptor of your application.</span></span> <span data-ttu-id="ea1ea-128">Essa cadeia de caracteres não será usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-128">This string will not be used in messages displayed for the user.</span></span> <span data-ttu-id="ea1ea-129">Esse valor é o identificador usado em todos os três valores de registro associados a cada um dos componentes de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-129">This value is the identifier used in all three registry values associated with each of the run-time components.</span></span>

<span data-ttu-id="ea1ea-130">*Cadeia de caracteres do aplicativo \_*</span><span class="sxs-lookup"><span data-stu-id="ea1ea-130">*APP\_STRING*</span></span>

<span data-ttu-id="ea1ea-131">Descritor do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-131">Descriptor of your application.</span></span> <span data-ttu-id="ea1ea-132">Essa cadeia de caracteres pode ser usada em mensagens exibidas para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-132">This string may be used in messages displayed for the user.</span></span>

<span data-ttu-id="ea1ea-133">*\_descritor de referência*</span><span class="sxs-lookup"><span data-stu-id="ea1ea-133">*REF\_DESCRIPTOR*</span></span>

<span data-ttu-id="ea1ea-134">Descrição de como seu aplicativo usa o componente.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-134">Description of how your application uses the component.</span></span> <span data-ttu-id="ea1ea-135">Esse valor pode incluir no máximo 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-135">This value can include a maximum of 256 characters.</span></span>

<span data-ttu-id="ea1ea-136">*versão do WMP \_*</span><span class="sxs-lookup"><span data-stu-id="ea1ea-136">*WMP\_VERSION*</span></span>

<span data-ttu-id="ea1ea-137">Versão do Windows Media Player exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-137">Version of Windows Media Player required by your application.</span></span>

<span data-ttu-id="ea1ea-138">*versão do WMF \_*</span><span class="sxs-lookup"><span data-stu-id="ea1ea-138">*WMF\_VERSION*</span></span>

<span data-ttu-id="ea1ea-139">Versão do SDK do Windows Media Format exigida pelo seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ea1ea-139">Version of the Windows Media Format SDK required by your application.</span></span>

<span data-ttu-id="ea1ea-140">Os três valores de registro de exemplo a seguir demonstram como configurar os valores para seu aplicativo:</span><span class="sxs-lookup"><span data-stu-id="ea1ea-140">The following three example registry values demonstrate how to configure the values for your application:</span></span>

-   <span data-ttu-id="ea1ea-141">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ app, "SouthridgeVideo", "Southridge Video Player"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-141">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\App, "SouthridgeVideo", "Southridge Video Player"</span></span>
-   <span data-ttu-id="ea1ea-142">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ descritor, "SouthridgeVideo", "SOUTHRIDGE Video Player usa o Windows Media Format SDK para reproduzir arquivos de vídeo".</span><span class="sxs-lookup"><span data-stu-id="ea1ea-142">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Descriptor, "SouthridgeVideo", "Southridge Video Player uses the Windows Media Format SDK to play video files."</span></span>
-   <span data-ttu-id="ea1ea-143">HKEY \_ classes \_ raiz \\ software \\ Microsoft \\ WindowsMedia \\ Setup \\ DependentRefCounts \\ versão, "SouthridgeVideo", "9.0.0.2600"</span><span class="sxs-lookup"><span data-stu-id="ea1ea-143">HKEY\_CLASSES\_ROOT\\Software\\Microsoft\\WindowsMedia\\Setup\\DependentRefCounts\\Version, "SouthridgeVideo", "9.0.0.2600"</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea1ea-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea1ea-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea1ea-145">**Considerações sobre o projeto**</span><span class="sxs-lookup"><span data-stu-id="ea1ea-145">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




