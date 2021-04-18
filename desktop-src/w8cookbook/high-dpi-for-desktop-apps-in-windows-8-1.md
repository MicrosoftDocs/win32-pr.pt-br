---
title: Alto DPI para aplicativos da área de trabalho no Windows 8.1
description: Alto DPI para aplicativos da área de trabalho no Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105786159"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="437ca-103">Alto DPI para aplicativos da área de trabalho no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="437ca-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="437ca-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="437ca-104">Platforms</span></span>

<dl> <span data-ttu-id="437ca-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="437ca-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="437ca-106">Servidores-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="437ca-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="437ca-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="437ca-107">Description</span></span>

<span data-ttu-id="437ca-108">Em Windows 8.1 aplicativos de área de trabalho devem ser executados em monitores com dimensionamento de 200% além do dimensionamento de 100%, 125% e 150% com suporte no Windows 8.</span><span class="sxs-lookup"><span data-stu-id="437ca-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="437ca-109">Além disso, os aplicativos de área de trabalho são dimensionados de acordo com cada monitor, em vez de um único fator de escala aplicado a todos os monitores.</span><span class="sxs-lookup"><span data-stu-id="437ca-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="437ca-110">Os desenvolvedores também podem chamar novas APIs no Windows 8.1 para obter fatores de escala por monitor.</span><span class="sxs-lookup"><span data-stu-id="437ca-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="437ca-111">Manifestações</span><span class="sxs-lookup"><span data-stu-id="437ca-111">Manifestations</span></span>

<span data-ttu-id="437ca-112">Os usuários podem usar novos monitores de alta densidade com Windows 8.1 para uma experiência visual excelente que aproveita os dados de pixels mais altos.</span><span class="sxs-lookup"><span data-stu-id="437ca-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="437ca-113">Se os aplicativos não tratarem do DPI alto, o Windows os dimensionará para o usuário.</span><span class="sxs-lookup"><span data-stu-id="437ca-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="437ca-114">Além disso, os usuários podem usar uma mistura de exibições de alta densidade altas no mesmo computador, e o Windows dimensionará o conteúdo adequadamente para cada exibição.</span><span class="sxs-lookup"><span data-stu-id="437ca-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="437ca-115">Esse é um aprimoramento do Windows 8, onde o conteúdo pode ser muito grande em alguns monitores.</span><span class="sxs-lookup"><span data-stu-id="437ca-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="437ca-116">Atenuação</span><span class="sxs-lookup"><span data-stu-id="437ca-116">Mitigation</span></span>

<span data-ttu-id="437ca-117">Como o Windows dimensionará os aplicativos que não se expandem, os desenvolvedores geralmente não precisam realizar trabalho adicional, mas os desenvolvedores que investem em escrever aplicativos que dão suporte a DPI alto terão uma vantagem competitiva, pois esses aplicativos terão uma aparência melhor em novos laptops de alto DPI e monitores de desktop.</span><span class="sxs-lookup"><span data-stu-id="437ca-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="437ca-118">Solução</span><span class="sxs-lookup"><span data-stu-id="437ca-118">Solution</span></span>

<span data-ttu-id="437ca-119">Criar um aplicativo que possa aproveitar o alto DPI é uma tarefa complexa de design e implementação.</span><span class="sxs-lookup"><span data-stu-id="437ca-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="437ca-120">Consulte os links abaixo para obter informações sobre o tutorial, criar conteúdo de apresentação e suporte semelhante.</span><span class="sxs-lookup"><span data-stu-id="437ca-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="437ca-121">Testes</span><span class="sxs-lookup"><span data-stu-id="437ca-121">Tests</span></span>

<span data-ttu-id="437ca-122">Mesmo que os desenvolvedores não escolham fazer com que seus aplicativos tirem proveito do DPI alto, eles devem testar seu aplicativo em 100%, 125%, 150% e escala de 200% para garantir que a experiência do usuário final seja satisfatória e competitiva.</span><span class="sxs-lookup"><span data-stu-id="437ca-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="437ca-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="437ca-123">Resources</span></span>

-   [<span data-ttu-id="437ca-124">White Paper e tutorial sobre DPI alto no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="437ca-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="437ca-125">Programas de exemplo da área de trabalho do Windows</span><span class="sxs-lookup"><span data-stu-id="437ca-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="437ca-126">COMPILAR sessão de saída 2013 em DPI alto no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="437ca-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 