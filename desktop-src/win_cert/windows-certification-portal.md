---
title: Certificar seu aplicativo de desktop
description: Siga estas etapas para obter seu aplicativo de desktop certificado para Windows 7, Windows 8, Windows 8.1 e Windows 10. se você quiser converter seu aplicativo de área de trabalho para ser compatível com o Plataforma Universal do Windows e a Windows Store, você usará a ponte de área de trabalho do Windows, caso em que você deve seguir as diretrizes de ponte de desktop para as etapas de certificação. Se você estiver desenvolvendo e certificando um aplicativo UWP desde o início, consulte Diretrizes para certificação de aplicativo do Windows em UWP para obter informações sobre certificação.
ms.assetid: d77d9f1c-1738-4f44-a351-1985ffc21707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52eb0f1040c438cb61f4729923c8928116447e8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "103642914"
---
# <a name="certify-your-desktop-application"></a><span data-ttu-id="024a1-103">Certificar seu aplicativo de desktop</span><span class="sxs-lookup"><span data-stu-id="024a1-103">Certify your desktop application</span></span>

> [!IMPORTANT]
> <span data-ttu-id="024a1-104">A certificação para aplicativos da área de trabalho Win32 foi [preterida](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span><span class="sxs-lookup"><span data-stu-id="024a1-104">Certification for Win32 desktop apps is [deprecated](https://techcommunity.microsoft.com/t5/windows-hardware-certification/win32-logo-certification-deprecation/ba-p/364920).</span></span> <span data-ttu-id="024a1-105">Em vez disso, [envie arquivos aqui](https://www.microsoft.com/wdsi/filesubmission/).</span><span class="sxs-lookup"><span data-stu-id="024a1-105">Instead, [submit files here](https://www.microsoft.com/wdsi/filesubmission/).</span></span>

<span data-ttu-id="024a1-106">Siga estas etapas para obter seu aplicativo de desktop certificado para Windows 7, Windows 8, Windows 8.1 e Windows 10.</span><span class="sxs-lookup"><span data-stu-id="024a1-106">Follow these steps to get your desktop app certified for Windows 7, Windows 8, Windows 8.1, and Windows 10.</span></span>

<span data-ttu-id="024a1-107">Se você quiser converter seu aplicativo de área de trabalho para ser compatível com o Plataforma Universal do Windows e a Windows Store, você usará a [ponte de área de trabalho do Windows](https://developer.microsoft.com/windows/bridges/desktop), caso em que você deve seguir as diretrizes de ponte de [Desktop](/windows/uwp/porting/desktop-to-uwp-root) para as etapas de certificação.</span><span class="sxs-lookup"><span data-stu-id="024a1-107">If you wish to convert your desktop app to be compatible with the Universal Windows Platform and Windows Store, you will use the [Windows Desktop Bridge](https://developer.microsoft.com/windows/bridges/desktop), in which case you should follow the [Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root) guidance for certification steps.</span></span>

<span data-ttu-id="024a1-108">Se você estiver desenvolvendo e certificando um aplicativo UWP desde o início, consulte [diretrizes para certificação de aplicativo do Windows em UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) para obter informações sobre certificação.</span><span class="sxs-lookup"><span data-stu-id="024a1-108">If you are developing and certifying a UWP app from the start, see [Guidance for Windows App Certification in UWP](/windows/uwp/debug-test-perf/windows-app-certification-kit) for info on certification.</span></span>

## <a name="step-1-prepare-for-certification"></a><span data-ttu-id="024a1-109">Etapa 1: preparar-se para a certificação</span><span class="sxs-lookup"><span data-stu-id="024a1-109">Step 1: Prepare for certification</span></span>



| <span data-ttu-id="024a1-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="024a1-110">Topic</span></span>                                                                                       | <span data-ttu-id="024a1-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="024a1-111">Description</span></span>                                                                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="024a1-112">Quais são os benefícios?</span><span class="sxs-lookup"><span data-stu-id="024a1-112">What are the benefits?</span></span>](what-are-the-benefits-.md)<br/>                             | <span data-ttu-id="024a1-113">A certificação de seu aplicativo de desktop fornece vários benefícios para você e seus clientes.</span><span class="sxs-lookup"><span data-stu-id="024a1-113">Certifying your desktop app provides several benefits for you and your customers.</span></span>              |
| [<span data-ttu-id="024a1-114">Leia os requisitos</span><span class="sxs-lookup"><span data-stu-id="024a1-114">Read the requirements</span></span>](certification-requirements-for-windows-desktop-apps.md)<br/> | <span data-ttu-id="024a1-115">Examine os requisitos técnicos e as qualificações de qualificação que um aplicativo de desktop deve atender.</span><span class="sxs-lookup"><span data-stu-id="024a1-115">Review the technical requirements and eligibility qualifications that a desktop app must meet.</span></span> |



 

## <a name="step-2-test-your-app-with-the-windows-app-certification-kit"></a><span data-ttu-id="024a1-116">Etapa 2: testar seu aplicativo com o kit de certificação de aplicativos do Windows</span><span class="sxs-lookup"><span data-stu-id="024a1-116">Step 2: Test your app with the Windows App Certification Kit</span></span>



| <span data-ttu-id="024a1-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="024a1-117">Topic</span></span>                                                          | <span data-ttu-id="024a1-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="024a1-118">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="024a1-119">Obtenha o kit</span><span class="sxs-lookup"><span data-stu-id="024a1-119">Get the Kit</span></span>](https://developer.microsoft.com/windows/downloads/app-certification-kit/) | <span data-ttu-id="024a1-120">Para certificar seu aplicativo, você precisa instalar e executar o kit de certificação de aplicativos para Windows (incluído no SDK do Windows).</span><span class="sxs-lookup"><span data-stu-id="024a1-120">To certify your app, you have to install and run the Windows App Certification Kit (included in the Windows SDK).</span></span>                                                                     |
| [<span data-ttu-id="024a1-121">Usando o kit</span><span class="sxs-lookup"><span data-stu-id="024a1-121">Using the Kit</span></span>](using-the-windows-app-certification-kit.md)   | <span data-ttu-id="024a1-122">Antes de poder enviar seu aplicativo, você deve testá-lo para preparação.</span><span class="sxs-lookup"><span data-stu-id="024a1-122">Before you can submit your app, you must test it for readiness.</span></span> <span data-ttu-id="024a1-123">Você também pode baixar uma cópia do [White Paper de certificação do aplicativo](https://www.microsoft.com/download/details.aspx?id=27414).</span><span class="sxs-lookup"><span data-stu-id="024a1-123">You can also download a copy of the [app certification white paper](https://www.microsoft.com/download/details.aspx?id=27414).</span></span> |
| [<span data-ttu-id="024a1-124">Examinar detalhes do teste</span><span class="sxs-lookup"><span data-stu-id="024a1-124">Review test details</span></span>](windows-app-certification-kit-tests.md) | <span data-ttu-id="024a1-125">Obtenha a lista dos testes que seu aplicativo precisa passar para se qualificar para compatibilidade com o sistema operacional Windows mais recente.</span><span class="sxs-lookup"><span data-stu-id="024a1-125">Get the list of the tests your app needs to pass to qualify for compatibility with the latest Windows operating system.</span></span>                                                               |



 

<span data-ttu-id="024a1-126">Observação: os drivers de filtro também devem passar pelo [Kit de certificação de hardware](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span><span class="sxs-lookup"><span data-stu-id="024a1-126">Note: Filter drivers must also pass the [Hardware Certification Kit](https://download.microsoft.com/download/1/8/B/18BC088A-537D-4386-9334-687747A602E6/hlk/hlksetup.exe).</span></span> <span data-ttu-id="024a1-127">(Consulte [requisitos de certificação para aplicativos da área de trabalho do Windows, seção 6,2](certification-requirements-for-windows-desktop-apps.md).)</span><span class="sxs-lookup"><span data-stu-id="024a1-127">(See [Certification requirements for Windows desktop apps, section 6.2](certification-requirements-for-windows-desktop-apps.md).)</span></span>

## <a name="step-3-use-the-windows-certification-dashboard"></a><span data-ttu-id="024a1-128">Etapa 3: usar o painel de certificação do Windows</span><span class="sxs-lookup"><span data-stu-id="024a1-128">Step 3: Use the Windows Certification Dashboard</span></span>

<span data-ttu-id="024a1-129">Para enviar seu aplicativo para certificação, você precisará fazer logon ou registrar uma conta da empresa no [painel de certificação do Windows](/previous-versions/hh833792(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="024a1-129">To submit your app for certification, you'll need to log in or register a company account on the [Windows Certification Dashboard](/previous-versions/hh833792(v=msdn.10)).</span></span> <span data-ttu-id="024a1-130">Depois de fazer isso, não só será possível adquirir seu aplicativo, mas você também obterá acesso a ferramentas para revisar e gerenciar seu aplicativo em todos os estágios do processo.</span><span class="sxs-lookup"><span data-stu-id="024a1-130">Once you do, not only will you be able to get your app certified, but you'll also gain access to tools to review and manage your app at all stages of the process.</span></span>



| <span data-ttu-id="024a1-131">Tópico</span><span class="sxs-lookup"><span data-stu-id="024a1-131">Topic</span></span>                                                                                                                   | <span data-ttu-id="024a1-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="024a1-132">Description</span></span>                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="024a1-133">Configurar sua conta</span><span class="sxs-lookup"><span data-stu-id="024a1-133">Set up your account</span></span>](/windows-hardware/drivers/dashboard/)                 | <span data-ttu-id="024a1-134">Se sua empresa ainda não estiver registrada, você deverá registrá-la por meio do painel de certificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="024a1-134">If your company isn't already registered, you must register it through the Windows Certification Dashboard.</span></span>                                        |
| [<span data-ttu-id="024a1-135">Obter um certificado de assinatura de código</span><span class="sxs-lookup"><span data-stu-id="024a1-135">Get a code signing certificate</span></span>](/windows-hardware/drivers/dashboard/)      | <span data-ttu-id="024a1-136">Antes de poder estabelecer uma conta do painel de certificação do Windows, você precisa obter um certificado de assinatura de código para proteger suas informações digitais.</span><span class="sxs-lookup"><span data-stu-id="024a1-136">Before you can establish a Windows Certification Dashboard account, you need to get a code signing certificate to secure your digital information.</span></span> |
| [<span data-ttu-id="024a1-137">Testar localmente e carregar os resultados</span><span class="sxs-lookup"><span data-stu-id="024a1-137">Test locally and upload the results</span></span>](/windows-hardware/drivers/dashboard/) | <span data-ttu-id="024a1-138">Depois de executar os testes do kit de certificação de aplicativos do Windows, carregue os resultados no painel de certificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="024a1-138">After your run the Windows App Certification Kit tests, upload the results to the Windows Certification Dashboard.</span></span>                                 |
| [<span data-ttu-id="024a1-139">Gerenciar seu envio</span><span class="sxs-lookup"><span data-stu-id="024a1-139">Manage your submission</span></span>](/windows-hardware/drivers/dashboard/)              | <span data-ttu-id="024a1-140">Depois de enviar seu aplicativo para certificação, você pode revisar seu envio por meio do painel de certificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="024a1-140">After you submit your app for certification, you can review your submission through the Windows Certification Dashboard.</span></span>                           |



 

## <a name="step-4-promote-your-desktop-app"></a><span data-ttu-id="024a1-141">Etapa 4: promover seu aplicativo de área de trabalho</span><span class="sxs-lookup"><span data-stu-id="024a1-141">Step 4: Promote your desktop app</span></span>



| <span data-ttu-id="024a1-142">Tópico</span><span class="sxs-lookup"><span data-stu-id="024a1-142">Topic</span></span>                                                                      | <span data-ttu-id="024a1-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="024a1-143">Description</span></span>                                                                                                               |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="024a1-144">Verificar a compatibilidade do aplicativo</span><span class="sxs-lookup"><span data-stu-id="024a1-144">Check app compatibility</span></span>](/windows/compatibility/windows-8-1-introduction) | <span data-ttu-id="024a1-145">Se você estiver criando um aplicativo para Windows 8.1, investigue as preocupações de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="024a1-145">If you are building an app for Windows 8.1, investigate compatibility concerns.</span></span>                                           |
| [<span data-ttu-id="024a1-146">Use o logotipo com seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="024a1-146">Use the logo with your app</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)                  | <span data-ttu-id="024a1-147">Exiba o logotipo no empacotamento e em anúncios e outros materiais promocionais de acordo com as diretrizes.</span><span class="sxs-lookup"><span data-stu-id="024a1-147">Display the logo on packaging and in ads and other promotional materials according to the guidelines.</span></span> <span data-ttu-id="024a1-148">Somente para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="024a1-148">For Windows 7 only.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="024a1-149">Consulte também:</span><span class="sxs-lookup"><span data-stu-id="024a1-149">See also:</span></span>

<span data-ttu-id="024a1-150">[Fórum de compatibilidade de aplicativos](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): encontre suporte da Comunidade sobre a compatibilidade e a certificação de logotipo.</span><span class="sxs-lookup"><span data-stu-id="024a1-150">[App compatibility forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowscompatibility): Find support from the community about compatibility and logo certification.</span></span>

<span data-ttu-id="024a1-151">[Blog de SDK do Windows](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): encontre dicas e notícias relacionadas à certificação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="024a1-151">[Windows SDK blog](https://blogs.msdn.com/b/winsdk/archive/tags/certification/): Find tips and news related to app certification.</span></span>

<span data-ttu-id="024a1-152">[Fórum do Windows Server]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): visite o fórum de certificação para obter respostas.</span><span class="sxs-lookup"><span data-stu-id="024a1-152">[Windows Server forum]( https://social.technet.microsoft.com/Forums/windowsserver/home?forum=WSAppCompat): Visit the Certification forum to get answers.</span></span>

<span data-ttu-id="024a1-153">[Manual de compatibilidade](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Obtenha informações sobre as novidades ou alterações na versão mais recente do Windows.</span><span class="sxs-lookup"><span data-stu-id="024a1-153">[Compatibility cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal): Get info about what's new or changed in the latest version of Windows.</span></span>

 

