---
description: Usando o .NET Framework 4 com aplicativos criados em versões anteriores
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Usando o .NET Framework 4 com aplicativos criados em versões anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef252d128ae5d3c8f5b85ef486828fb82e152d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813596"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="48b96-103">Usando o .NET Framework 4 com aplicativos criados em versões anteriores</span><span class="sxs-lookup"><span data-stu-id="48b96-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="48b96-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="48b96-104">Platform</span></span>

 <span data-ttu-id="48b96-105">**Clientes** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="48b96-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="48b96-106">**Servidores** -windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="48b96-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="48b96-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="48b96-107">Feature Impact</span></span>

 <span data-ttu-id="48b96-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="48b96-108">**Severity** - Low</span></span>  
<span data-ttu-id="48b96-109">**Frequência** -alta</span><span class="sxs-lookup"><span data-stu-id="48b96-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="48b96-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="48b96-110">Description</span></span>

<span data-ttu-id="48b96-111">O .NET Framework 4 é altamente compatível com aplicativos que são criados usando versões anteriores do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="48b96-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="48b96-112">As principais alterações no .NET Framework 4 são melhorar a segurança, a conformidade dos padrões, a exatidão, a confiabilidade e o desempenho.</span><span class="sxs-lookup"><span data-stu-id="48b96-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="48b96-113">No entanto, .NET Framework 4 não usa automaticamente sua versão do Common Language Runtime (CLR) para executar aplicativos que são criados com o uso de versões anteriores do .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="48b96-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="48b96-114">Manifestação</span><span class="sxs-lookup"><span data-stu-id="48b96-114">Manifestation</span></span>

<span data-ttu-id="48b96-115">Se você tiver criado um aplicativo usando uma .NET Framework anterior e um usuário abrir esse aplicativo em um computador que tenha o .NET Framework 4 e a versão anterior do .NET Framework instalado, o aplicativo usará a versão mais antiga do CLR.</span><span class="sxs-lookup"><span data-stu-id="48b96-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="48b96-116">No entanto, se o .NET Framework 4 for a única versão de tempo de execução instalada no computador, o aplicativo lançará uma exceção e solicitará que o usuário instale a versão de tempo de execução na qual você criou o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48b96-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="48b96-117">Solução</span><span class="sxs-lookup"><span data-stu-id="48b96-117">Solution</span></span>

<span data-ttu-id="48b96-118">Para executar aplicativos criados com versões anteriores do .NET Framework com o .NET Framework 4, você deve compilar seu aplicativo para direcionar a versão do .NET Framework 4 especificando-o nas propriedades do seu projeto no Microsoft Visual Studio, ou pode especificar .NET Framework 4 no [**<supportedRuntime> elemento**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) em um arquivo de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48b96-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="48b96-119">Para obter mais informações sobre como migrar para o .NET Framework 4, consulte [Guia de migração para o .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) e [compatibilidade de versão no .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="48b96-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="48b96-120">Testes de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="48b96-120">Compatibility Tests</span></span>

<span data-ttu-id="48b96-121">Depois de fazer as alterações, teste seu aplicativo para certificar-se de que ele seja executado corretamente.</span><span class="sxs-lookup"><span data-stu-id="48b96-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="48b96-122">Você pode testar a compatibilidade conforme descrito no tópico [.NET Framework 4 compatibilidade de aplicativos](/previous-versions/dd889541(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="48b96-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="48b96-123">Se seu aplicativo ou componente não funcionar após a instalação do .NET Framework 4, envie um bug por meio do site do [Microsoft Connect](https://connect.microsoft.com/visualstudio) .</span><span class="sxs-lookup"><span data-stu-id="48b96-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="48b96-124">Links para outros recursos</span><span class="sxs-lookup"><span data-stu-id="48b96-124">Links to Other Resources</span></span>

-   <span data-ttu-id="48b96-125">[**<supportedRuntime> elementos**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="48b96-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="48b96-126">[Guia de migração do .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="48b96-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="48b96-127">[Compatibilidade de versão no .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="48b96-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="48b96-128">**Explicação da compatibilidade de aplicativos RTM do .NET Framework 4:**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="48b96-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="48b96-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="48b96-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
