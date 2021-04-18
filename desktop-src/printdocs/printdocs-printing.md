---
description: O Windows fornece aos aplicativos um conjunto completo de funções que permitem a impressão em vários dispositivos, como impressoras a laser, plotadoras vetoriais, impressoras de varredura e máquinas de fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impressão (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788647"
---
# <a name="printing-documents-and-printing"></a><span data-ttu-id="b82db-103">Impressão (documentos e impressão)</span><span class="sxs-lookup"><span data-stu-id="b82db-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="b82db-104">O Windows fornece aos aplicativos um conjunto completo de funções que permitem a impressão em vários dispositivos, como impressoras a laser, plotadoras vetoriais, impressoras de varredura e máquinas de fax.</span><span class="sxs-lookup"><span data-stu-id="b82db-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="b82db-105">Impressão de aplicativo de desktop</span><span class="sxs-lookup"><span data-stu-id="b82db-105">Desktop App Printing</span></span>

<span data-ttu-id="b82db-106">Os programadores do Windows podem selecionar entre várias tecnologias diferentes para imprimir de seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b82db-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b82db-107">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="b82db-107">Technology</span></span></th>
<th><span data-ttu-id="b82db-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b82db-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b82db-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Imprimir API de pacote de documento</a></span><span class="sxs-lookup"><span data-stu-id="b82db-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="b82db-110">Fornece uma interface que permite que um aplicativo acesse e gerencie o pacote de documentos de impressão.</span><span class="sxs-lookup"><span data-stu-id="b82db-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="b82db-111">Essa API está disponível com o Windows 8 e versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="b82db-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b82db-112"><a href="print-spooler-api.md">API do spooler de impressão</a></span><span class="sxs-lookup"><span data-stu-id="b82db-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="b82db-113">Fornece uma interface para o spooler de impressão para que os aplicativos possam gerenciar impressoras e trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="b82db-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="b82db-114">Os aplicativos usam a <a href="print-spooler-api.md">API spooler de impressão</a> para iniciar, parar, controlar e configurar trabalhos de impressão gerenciados pelo spooler de impressão, independentemente de usarem a <a href="/windows/desktop/printdocs/tailored-app-printing-api">API de pacote de documentos de impressão</a> ou a <a href="gdi-printing.md">API de impressão GDI</a> para imprimir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b82db-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b82db-115"><a href="print-ticket-api.md">API de tíquete de impressão</a></span><span class="sxs-lookup"><span data-stu-id="b82db-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="b82db-116">Fornece aplicativos com funções para gerenciar e converter tíquetes de impressão.</span><span class="sxs-lookup"><span data-stu-id="b82db-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b82db-117"><a href="gdi-printing.md">API de impressão GDI</a></span><span class="sxs-lookup"><span data-stu-id="b82db-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="b82db-118">Fornece aplicativos com uma interface de impressão independente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b82db-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="b82db-119">Os desenvolvedores que estão escrevendo aplicativos para o Windows Vista e versões posteriores do Windows devem considerar o uso da <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de documento XPS</a> em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b82db-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="b82db-120">A <a href="gdi-printing.md">API de impressão GDI</a> é adequada para aplicativos que devem ser executados no Windows XP e em versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="b82db-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b82db-121">A ilustração a seguir fornece uma exibição de alto nível de como as diferentes APIs de impressão estão relacionadas.</span><span class="sxs-lookup"><span data-stu-id="b82db-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![um diagrama que mostra como um aplicativo nativo do Windows pode usar as APIs de impressão](images/print-apis.png)

 

<span data-ttu-id="b82db-123">Os s da [API de pacote de documentos de impressão](./tailored-app-printing-api.md)nesta seção descrevem o pacote de documentos impressos e as interfaces de visualização de impressão que você pode usar com o Windows 8 e versões posteriores do Windows desktop.</span><span class="sxs-lookup"><span data-stu-id="b82db-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="b82db-124">Para obter mais informações sobre a impressão de aplicativos da Windows Store que são escritos em JavaScript e HTML, consulte [impressão (aplicativos da Windows Store usando JavaScript e HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="b82db-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="b82db-125">Para obter mais informações sobre a impressão de aplicativos da Windows Store que são escritos em C#, Microsoft Visual Basic ou C++ e XAML, consulte [impressão (aplicativos da Windows Store usando C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="b82db-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="b82db-126">Consulte [Win32 e com para aplicativos da Windows Store (impressão e documentos)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) para obter a lista de APIs de impressão do aplicativo de desktop que também podem ser usadas em aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="b82db-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b82db-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b82db-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b82db-128">[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b82db-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b82db-129">Comunicações bidirecionais de impressora (centro de desenvolvimento de hardware)</span><span class="sxs-lookup"><span data-stu-id="b82db-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

