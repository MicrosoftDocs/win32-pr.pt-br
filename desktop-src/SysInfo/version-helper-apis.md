---
description: As funções a seguir podem ser usadas para determinar a versão atual do sistema operacional ou identificar se é uma versão do Windows ou do Windows Server.
ms.assetid: 2FAF67CD-CEEA-4096-B482-F5E2DF8D6C34
title: Funções auxiliares de versão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746e6488d949fe6512355d7ef9910c26aaf3b54b
ms.sourcegitcommit: 49df0f62429d21bca96d8704205048267ee0eb59
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/23/2021
ms.locfileid: "105751053"
---
# <a name="version-helper-functions"></a><span data-ttu-id="c5709-103">Funções auxiliares de versão</span><span class="sxs-lookup"><span data-stu-id="c5709-103">Version Helper functions</span></span>

<span data-ttu-id="c5709-104">As funções a seguir podem ser usadas para determinar a versão atual do sistema operacional ou identificar se é uma versão do Windows ou do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c5709-104">The following functions can be used to determine the current operating system version or identify whether it is a Windows or Windows Server release.</span></span> <span data-ttu-id="c5709-105">Essas funções fornecem testes simples que usam a função [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) e as comparações recomendadas maiores ou iguais às comparações comprovadas como um meio robusto para determinar a versão do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c5709-105">These functions provide simple tests that use the [VerifyVersionInfo](/windows/win32/api/Winbase/nf-winbase-verifyversioninfoa) function and the recommended greater than or equal to comparisons that are proven as a robust means to determine the operating system version.</span></span>

> [!Note]  
> <span data-ttu-id="c5709-106">Essas APIs são definidas por **versionhelpers. h**, que está incluído no Windows 8.1 Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c5709-106">These APIs are defined by **versionhelpers.h**, which is included in the Windows 8.1 software development kit (SDK).</span></span> <span data-ttu-id="c5709-107">Esse arquivo pode ser usado com outras versões de Microsoft Visual Studio para implementar a mesma funcionalidade para versões do Windows anteriores à Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="c5709-107">This file can be used with other Microsoft Visual Studio releases to implement the same functionality for Windows versions prior to Windows 8.1.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c5709-108">Função</span><span class="sxs-lookup"><span data-stu-id="c5709-108">Function</span></span></th>
<th><span data-ttu-id="c5709-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5709-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c5709-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-110"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxporgreater"><strong>IsWindowsXPOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-111">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5709-111">Indicates if the current OS version matches, or is greater than, the Windows XP version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-112"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp1orgreater"><strong>IsWindowsXPSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-113">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c5709-113">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5709-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-114"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp2orgreater"><strong>IsWindowsXPSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-115">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="c5709-115">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-116"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsxpsp3orgreater"><strong>IsWindowsXPSP3OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-117">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows XP com Service Pack 3 (SP3).</span><span class="sxs-lookup"><span data-stu-id="c5709-117">Indicates if the current OS version matches, or is greater than, the Windows XP with Service Pack 3 (SP3) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5709-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-118"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistaorgreater"><strong>IsWindowsVistaOrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-119">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5709-119">Indicates if the current OS version matches, or is greater than, the Windows Vista version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-120"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp1orgreater"><strong>IsWindowsVistaSP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-121">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows Vista com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c5709-121">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5709-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-122"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsvistasp2orgreater"><strong>IsWindowsVistaSP2OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-123">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows Vista com Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="c5709-123">Indicates if the current OS version matches, or is greater than, the Windows Vista with Service Pack 2 (SP2) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-124"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7orgreater"><strong>IsWindows7OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-125">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5709-125">Indicates if the current OS version matches, or is greater than, the Windows 7 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5709-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-126"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows7sp1orgreater"><strong>IsWindows7SP1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-127">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows 7 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c5709-127">Indicates if the current OS version matches, or is greater than, the Windows 7 with Service Pack 1 (SP1) version.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-128"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8orgreater"><strong>IsWindows8OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-129">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c5709-129">Indicates if the current OS version matches, or is greater than, the Windows 8 version.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5709-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-130"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-131">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="c5709-131">Indicates if the current OS version matches, or is greater than, the Windows 8.1 version.</span></span><br/> <span data-ttu-id="c5709-132">Para o Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> retornará false, a menos que o aplicativo contenha um manifesto que inclua uma seção de compatibilidade que contenha os GUIDs que designam Windows 8.1 e/ou Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c5709-132">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows8point1orgreater"><strong>IsWindows8Point1OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUIDs that designate Windows 8.1 and/or Windows 10.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-133"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a></span></span></td>
<td><span data-ttu-id="c5709-134">Indica se a versão atual do sistema operacional corresponde ou é maior que a versão do Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c5709-134">Indicates if the current OS version matches, or is greater than, the Windows 10 version.</span></span><br/> <span data-ttu-id="c5709-135">Para o Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> retornará false, a menos que o aplicativo contenha um manifesto que inclua uma seção de compatibilidade que contenha o GUID que designa o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c5709-135">For Windows 10, <a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindows10orgreater"><strong>IsWindows10OrGreater</strong></a> returns false unless the application contains a manifest that includes a compatibility section that contains the GUID that designates Windows 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5709-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-136"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsserver"><strong>IsWindowsServer</strong></a></span></span></td>
<td><span data-ttu-id="c5709-137">Indica se o sistema operacional atual é uma versão do Windows Server.</span><span class="sxs-lookup"><span data-stu-id="c5709-137">Indicates if the current OS is a Windows Server release.</span></span> <span data-ttu-id="c5709-138">Os aplicativos que precisam distinguir entre as versões de servidor e cliente do Windows devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="c5709-138">Applications that need to distinguish between server and client versions of Windows should call this function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5709-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span><span class="sxs-lookup"><span data-stu-id="c5709-139"><a href="/windows/desktop/api/VersionHelpers/nf-versionhelpers-iswindowsversionorgreater"><strong>IsWindowsVersionOrGreater</strong></a></span></span></td>
<td>
<blockquote><span data-ttu-id="c5709-140">Você só deve usar essa função se as outras funções auxiliares de versão fornecidas não se ajustarem ao seu cenário.</span><span class="sxs-lookup"><span data-stu-id="c5709-140">You should only use this function if the other provided version helper functions do not fit your scenario.</span></span></blockquote>
<br/><span data-ttu-id="c5709-141">Indica se a versão atual do sistema operacional corresponde ou é maior que as informações de versão fornecidas.</span><span class="sxs-lookup"><span data-stu-id="c5709-141">Indicates if the current OS version matches, or is greater than, the provided version information.</span></span> <span data-ttu-id="c5709-142">Essa função é útil na confirmação de uma versão do Windows Server que não compartilha um número de versão com uma versão do cliente.</span><span class="sxs-lookup"><span data-stu-id="c5709-142">This function is useful in confirming a version of Windows Server that doesn't share a version number with a client release.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="c5709-143">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c5709-143">Example</span></span>

<span data-ttu-id="c5709-144">As funções embutidas definidas no arquivo de cabeçalho **VersionHelpers. h** permitem verificar a versão do sistema operacional retornando um valor **booliano** durante o teste de uma versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="c5709-144">The inline functions defined in the **VersionHelpers.h** header file let you verify the operating system version by returning a **Boolean** value when testing for a version of Windows.</span></span>

<span data-ttu-id="c5709-145">Por exemplo, se seu aplicativo exigir o Windows 8 ou posterior, use o teste a seguir.</span><span class="sxs-lookup"><span data-stu-id="c5709-145">For example, if your application requires Windows 8 or later, use the following test.</span></span>

```C++
#include <VersionHelpers.h>
 
if (!IsWindows8OrGreater())
{
   MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
}
```

## <a name="related-topics"></a><span data-ttu-id="c5709-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5709-146">Related topics</span></span>

- [<span data-ttu-id="c5709-147">OSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="c5709-147">OSVERSIONINFOEX</span></span>](/windows/desktop/api/Winnt/ns-winnt-osversioninfoexa)
