---
description: Você não precisa de um Tablet PC para desenvolver aplicativos de Tablet PC, mas precisa de um computador pessoal capaz de executar o software listado posteriormente neste tópico.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: O ambiente de desenvolvimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922834"
---
# <a name="the-development-environment"></a><span data-ttu-id="b4a05-103">O ambiente de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="b4a05-103">The Development Environment</span></span>

<span data-ttu-id="b4a05-104">Você não precisa de um Tablet PC para desenvolver aplicativos de Tablet PC, mas precisa de um computador pessoal capaz de executar o software listado posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="b4a05-104">You do not need a Tablet PC to develop Tablet PC applications, but you do need a personal computer capable of running the software listed later in this topic.</span></span>

<span data-ttu-id="b4a05-105">É altamente recomendável que você teste seu aplicativo em um Tablet PC real para garantir que todas as diferenças no hardware, como o digitalizador de resolução mais alta, sejam contadas para o.</span><span class="sxs-lookup"><span data-stu-id="b4a05-105">We strongly recommend that you test your application on an actual Tablet PC to ensure that all differences in hardware, such as the higher resolution digitizer, are accounted for.</span></span>

<span data-ttu-id="b4a05-106">Um sistema comum de desenvolvimento mínimo consiste no hardware e software a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4a05-106">A typical, minimal development system consists of the following hardware and software.</span></span>

## <a name="hardware"></a><span data-ttu-id="b4a05-107">Hardware</span><span class="sxs-lookup"><span data-stu-id="b4a05-107">Hardware</span></span>

-   <span data-ttu-id="b4a05-108">8 MB de espaço em disco rígido para uma instalação completa.</span><span class="sxs-lookup"><span data-stu-id="b4a05-108">8 MB of hard disk space for a complete installation.</span></span>
-   <span data-ttu-id="b4a05-109">Um dispositivo apontador para entrada.</span><span class="sxs-lookup"><span data-stu-id="b4a05-109">A pointing device for input.</span></span> <span data-ttu-id="b4a05-110">Isso inclui dispositivos como um mouse, um Tablet externo ou um Tablet PC com um digitalizador HID.</span><span class="sxs-lookup"><span data-stu-id="b4a05-110">This includes devices such as a mouse, an external tablet, or a Tablet PC with an HID digitizer.</span></span>

<span data-ttu-id="b4a05-111">O HID significa dispositivos de interface humana, um padrão para dispositivos de entrada.</span><span class="sxs-lookup"><span data-stu-id="b4a05-111">HID stands for Human Interface Device, a standard for input devices.</span></span> <span data-ttu-id="b4a05-112">Os digitalizadores não compatíveis com HID são tratados como um mouse regular, enquanto os digitalizadores compatíveis com HID têm resolução maior e mais metadados em traços, como pressão, semelhantes aos que estão instalados no hardware do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b4a05-112">Non-HID compliant digitizers are treated like a regular mouse, while HID compliant digitizers have higher resolution and more metadata on strokes, such as pressure, similar to those that are installed on Tablet PC hardware.</span></span>

## <a name="software"></a><span data-ttu-id="b4a05-113">Software</span><span class="sxs-lookup"><span data-stu-id="b4a05-113">Software</span></span>

<span data-ttu-id="b4a05-114">Os seguintes sistemas operacionais podem ser usados para desenvolver aplicativos para Tablet PC:</span><span class="sxs-lookup"><span data-stu-id="b4a05-114">The following operating systems can be used to develop Tablet PC applications:</span></span>

-   <span data-ttu-id="b4a05-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4a05-115">Windows 7</span></span>
-   <span data-ttu-id="b4a05-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4a05-116">Windows Vista</span></span>
-   <span data-ttu-id="b4a05-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4a05-117">Windows Server 2008</span></span>
-   <span data-ttu-id="b4a05-118">Windows XP Tablet PC Edition 2005</span><span class="sxs-lookup"><span data-stu-id="b4a05-118">Windows XP Tablet PC Edition 2005</span></span>
-   <span data-ttu-id="b4a05-119">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b4a05-119">Windows Server 2003</span></span>
-   <span data-ttu-id="b4a05-120">Windows XP Professional</span><span class="sxs-lookup"><span data-stu-id="b4a05-120">Windows XP Professional</span></span>

<span data-ttu-id="b4a05-121">Você também precisará de:</span><span class="sxs-lookup"><span data-stu-id="b4a05-121">You also need:</span></span>

-   <span data-ttu-id="b4a05-122">Visual Studio versão 6 com Service Pack 5, ou Visual Studio .NET ou Visual Studio .NET 2005</span><span class="sxs-lookup"><span data-stu-id="b4a05-122">Visual Studio version 6 with Service Pack 5, or Visual Studio .NET, or Visual Studio .NET 2005</span></span>
-   <span data-ttu-id="b4a05-123">Microsoft Internet Explorer 6 ou superior (recomendado)</span><span class="sxs-lookup"><span data-stu-id="b4a05-123">Microsoft Internet Explorer 6, or higher (recommended)</span></span>

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a><span data-ttu-id="b4a05-124">Detalhes sobre o desenvolvimento em SKUs sem Tablet PC do Windows</span><span class="sxs-lookup"><span data-stu-id="b4a05-124">Details on Developing on Non-Tablet PC SKUs of Windows</span></span>

<span data-ttu-id="b4a05-125">Os componentes da plataforma Tablet PC podem ser instalados no Windows XP Professional com Service Pack 2 ou no Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b4a05-125">The Tablet PC platform components can be installed on Windows XP Professional with Service Pack 2 or Windows Server 2003.</span></span> <span data-ttu-id="b4a05-126">Nesses sistemas operacionais, seu aplicativo pode coletar tinta com a classe [**InkCollector**](inkcollector-class.md) e pode ser testado e depurado.</span><span class="sxs-lookup"><span data-stu-id="b4a05-126">On these operating systems, your application can collect ink with the [**InkCollector**](inkcollector-class.md) class and can be tested and debugged.</span></span> <span data-ttu-id="b4a05-127">No entanto, nenhum reconhecimento estará disponível a menos que você também instale o pacote de reconhecimento do Microsoft Windows XP Tablet PC Edition 2005.</span><span class="sxs-lookup"><span data-stu-id="b4a05-127">However, no recognition is available unless you also install the Microsoft Windows XP Tablet PC Edition 2005 Recognizer Pack.</span></span> <span data-ttu-id="b4a05-128">Você pode baixar esse pacote do centro de download no MSDN.</span><span class="sxs-lookup"><span data-stu-id="b4a05-128">You can download that pack from the Download Center on MSDN.</span></span>

<span data-ttu-id="b4a05-129">Depois de instalar o SDK do Windows em um sistema Windows XP Professional ou Windows Server 2003, você terá todos os arquivos de desenvolvimento necessários para criar aplicativos de tinta (como msinkaut. h para um desenvolvedor COM).</span><span class="sxs-lookup"><span data-stu-id="b4a05-129">After installing the Windows SDK on to a Windows XP Professional or Windows Server 2003 system, you will have all the development files necessary to build ink applications (such as msinkaut.h for a COM developer).</span></span> <span data-ttu-id="b4a05-130">No entanto, você não poderá executar ou depurar seu aplicativo nesse sistema até instalar os arquivos de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b4a05-130">However, you will be unable to run or debug your application on that system until you install the runtime files.</span></span> <span data-ttu-id="b4a05-131">Por exemplo, no caso de um desenvolvedor COM, inkobj.dll deve ser instalado e registrado.</span><span class="sxs-lookup"><span data-stu-id="b4a05-131">For instance, in the case of a COM developer, inkobj.dll must be installed and registered.</span></span> <span data-ttu-id="b4a05-132">Como você não está em um sistema onde esses arquivos de plataforma existem, você deve instalar os componentes da plataforma Tablet PC do módulo de mesclagem redistribuível, mstpcrt. msm, para obter os arquivos de tempo de execução em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="b4a05-132">Because you are not on a system where these platform files exist, you must install the Tablet PC platform components from the redistributable merge module, mstpcrt.msm, to get the runtime files on your system.</span></span>

<span data-ttu-id="b4a05-133">A maneira mais simples de obter os tempos de execução da plataforma instalados em um sistema Windows XP Professional ou Windows 2000 para fins de desenvolvimento é compilar o projeto de configuração de exemplo fornecido com os exemplos de PC móvel e Tablet PC e implantá-lo no computador de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="b4a05-133">The simplest way to get the platform runtimes installed on a Windows XP Professional or Windows 2000 system for development purposes is to compile the sample setup project provided with the Mobile PC and Tablet PC Samples and deploy it to the development machine.</span></span>

> [!Note]  
> <span data-ttu-id="b4a05-134">O Windows Vista e o Windows XP Tablet PC Edition 2005 já têm os componentes da plataforma instalados, portanto, eles não exigem etapas adicionais para executar e depurar aplicativos do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="b4a05-134">Windows Vista and Windows XP Tablet PC Edition 2005 already have the platform components installed, so they do not require additional steps to run and debug Tablet PC applications.</span></span>

 

<span data-ttu-id="b4a05-135">Os controles [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) podem ser usados para coletar tinta no Windows 2000 com Service Pack 4 ou Windows XP Professional com Service Pack 2 quando os componentes da plataforma do Tablet PC estão presentes, instalando o SDK do Tablet PC versão 1,7, mas não podem coletar tinta em sistemas que não são do Tablet PC que não têm os componentes da plataforma Tablet PC instalados.</span><span class="sxs-lookup"><span data-stu-id="b4a05-135">The [InkEdit](inkedit-control-reference.md) and [InkPicture](inkpicture-control-reference.md) controls can be used to collect ink on Windows 2000 with Service Pack 4 or Windows XP Professional with Service Pack 2 when the Tablet PC platform components are present by installing the Tablet PC SDK version 1.7, but are not able to collect ink on non-Tablet PC systems that do not have the Tablet PC platform components installed.</span></span>

<span data-ttu-id="b4a05-136">O SDK do Windows fornece todos os componentes necessários para desenvolver aplicativos para Tablet PC em SKUs não-Tablet do Windows.</span><span class="sxs-lookup"><span data-stu-id="b4a05-136">The Windows SDK provides all the necessary components to develop Tablet PC applications on non-Tablet SKUs of Windows.</span></span> <span data-ttu-id="b4a05-137">Defina a seguinte chave do registro **DWORD** como 1 para coletar tinta em SKUs não-Tablet do Windows:</span><span class="sxs-lookup"><span data-stu-id="b4a05-137">Set the following **DWORD** registry key to 1 in order to collect ink on non-Tablet SKUs of Windows:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

<span data-ttu-id="b4a05-138">Essa chave destina-se apenas a fins de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="b4a05-138">This key is intended for development purposes only.</span></span>

 

 



