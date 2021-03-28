---
description: Esta seção descreve como determinar a versão das DLLs de Shell em que seu aplicativo está em execução e como direcionar seu aplicativo para uma versão específica.
title: 'Versões de DLL do Shell e Shlwapi '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 49fb1767b7074da6480a47c52eb1384fb935317b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169418"
---
# <a name="shell-and-shlwapi-dll-versions"></a><span data-ttu-id="42363-103">Versões de DLL do Shell e Shlwapi </span><span class="sxs-lookup"><span data-stu-id="42363-103">Shell and Shlwapi DLL Versions</span></span>

<span data-ttu-id="42363-104">Esta seção descreve como determinar a versão das DLLs de Shell em que seu aplicativo está em execução e como direcionar seu aplicativo para uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="42363-104">This section describes how to determine which version of the Shell DLLs your application is running on and how to target your application for a specific version.</span></span>

-   [<span data-ttu-id="42363-105">Números de versão da DLL</span><span class="sxs-lookup"><span data-stu-id="42363-105">DLL Version Numbers</span></span>](#dll-version-numbers)
-   [<span data-ttu-id="42363-106">Usando DllGetVersion para determinar o número de versão</span><span class="sxs-lookup"><span data-stu-id="42363-106">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
    -   [<span data-ttu-id="42363-107">Usando DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="42363-107">Using DllGetVersion</span></span>](#using-dllgetversion)
-   [<span data-ttu-id="42363-108">Versões do projeto</span><span class="sxs-lookup"><span data-stu-id="42363-108">Project Versions</span></span>](#project-versions)

## <a name="dll-version-numbers"></a><span data-ttu-id="42363-109">Números de versão da DLL</span><span class="sxs-lookup"><span data-stu-id="42363-109">DLL Version Numbers</span></span>

<span data-ttu-id="42363-110">Todos, exceto alguns dos elementos de programação discutidos na documentação do Shell, estão contidos em duas DLLs: Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="42363-110">All but a handful of the programming elements discussed in the Shell documentation are contained in two DLLs: Shell32.dll and Shlwapi.dll.</span></span> <span data-ttu-id="42363-111">Devido a aprimoramentos contínuos, versões diferentes dessas DLLs implementam recursos diferentes.</span><span class="sxs-lookup"><span data-stu-id="42363-111">Because of ongoing enhancements, different versions of these DLLs implement different features.</span></span> <span data-ttu-id="42363-112">Em toda a documentação de referência do Shell, cada elemento de programação especifica um número de versão da DLL com suporte mínimo.</span><span class="sxs-lookup"><span data-stu-id="42363-112">Throughout the Shell reference documentation, each programming element specifies a minimum supported DLL version number.</span></span> <span data-ttu-id="42363-113">Esse número de versão indica que o elemento de programação é implementado nessa versão e nas versões subsequentes da DLL, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="42363-113">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="42363-114">Se nenhum número de versão for especificado, o elemento de programação será implementado em todas as versões existentes da DLL.</span><span class="sxs-lookup"><span data-stu-id="42363-114">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="42363-115">Antes do Windows XP, novas versões Shell32.dll e Shlwapi.dll às vezes eram fornecidas com novas versões do Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="42363-115">Before Windows XP, new Shell32.dll and Shlwapi.dll versions were sometimes provided with new versions of Windows Internet Explorer.</span></span> <span data-ttu-id="42363-116">A partir do Windows XP, essas DLLs não eram mais fornecidas como arquivos redistribuíveis fora das novas versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="42363-116">As of Windows XP, those DLLs were no longer provided as redistributable files outside of new versions of Windows itself.</span></span> <span data-ttu-id="42363-117">A tabela a seguir descreve as diferentes versões de DLL e como elas foram distribuídas de volta para o Microsoft Internet Explorer 3,0, o Windows 95 e o Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="42363-117">The following table outlines the different DLL versions and how they were distributed dating back to Microsoft Internet Explorer 3.0, Windows 95, and Microsoft Windows NT 4.0.</span></span>

<span data-ttu-id="42363-118">Shell32.dll versão 4,0 é encontrada nas versões originais do Windows 95 e do Microsoft Windows NT 4,0.</span><span class="sxs-lookup"><span data-stu-id="42363-118">Shell32.dll version 4.0 is found in the original versions of Windows 95 and Microsoft Windows NT 4.0.</span></span> <span data-ttu-id="42363-119">O shell não foi atualizado com a versão 3,0 do Internet Explorer, portanto Shell32.dll não tem uma versão 4,70.</span><span class="sxs-lookup"><span data-stu-id="42363-119">The Shell was not updated with the Internet Explorer 3.0 release, so Shell32.dll does not have a version 4.70.</span></span> <span data-ttu-id="42363-120">Shell32.dll versões 4,71 e 4,72 foram enviadas com as versões correspondentes do Internet Explorer, mas elas não foram necessariamente instaladas (consulte a observação 1).</span><span class="sxs-lookup"><span data-stu-id="42363-120">Shell32.dll versions 4.71 and 4.72 were shipped with the corresponding Internet Explorer releases, but they were not necessarily installed (see note 1).</span></span> <span data-ttu-id="42363-121">Para versões posteriores ao Microsoft Internet Explorer 4, 1 e ao Windows 98, os números de versão para Shell32.dll e Shlwapi.dll divergência.</span><span class="sxs-lookup"><span data-stu-id="42363-121">For releases subsequent to Microsoft Internet Explorer 4.01 and Windows 98, the version numbers for Shell32.dll and Shlwapi.dll diverge.</span></span> <span data-ttu-id="42363-122">Em geral, você deve assumir que as DLLs têm números de versão diferentes e testar cada uma separadamente.</span><span class="sxs-lookup"><span data-stu-id="42363-122">In general, you should assume that the DLLs have different version numbers and test each one separately.</span></span>

#### <a name="shell32dll"></a><span data-ttu-id="42363-123">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="42363-123">Shell32.dll</span></span>

| <span data-ttu-id="42363-124">Versão</span><span class="sxs-lookup"><span data-stu-id="42363-124">Version</span></span> | <span data-ttu-id="42363-125">Plataforma de distribuição</span><span class="sxs-lookup"><span data-stu-id="42363-125">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="42363-126">4,0</span><span class="sxs-lookup"><span data-stu-id="42363-126">4.0</span></span>     | <span data-ttu-id="42363-127">Windows 95 e Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="42363-127">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="42363-128">4,71</span><span class="sxs-lookup"><span data-stu-id="42363-128">4.71</span></span>    | <span data-ttu-id="42363-129">Microsoft Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="42363-129">Microsoft Internet Explorer 4.0.</span></span> <span data-ttu-id="42363-130">Consulte a observação 1.</span><span class="sxs-lookup"><span data-stu-id="42363-130">See note 1.</span></span>                                |
| <span data-ttu-id="42363-131">4,72</span><span class="sxs-lookup"><span data-stu-id="42363-131">4.72</span></span>    | <span data-ttu-id="42363-132">Internet Explorer 4, 1 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="42363-132">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="42363-133">Consulte a observação 1.</span><span class="sxs-lookup"><span data-stu-id="42363-133">See note 1.</span></span>                          |
| <span data-ttu-id="42363-134">5.0</span><span class="sxs-lookup"><span data-stu-id="42363-134">5.0</span></span>     | <span data-ttu-id="42363-135">Windows 2000 e Windows Millennium Edition (Windows me).</span><span class="sxs-lookup"><span data-stu-id="42363-135">Windows 2000 and Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="42363-136">Consulte a observação 2.</span><span class="sxs-lookup"><span data-stu-id="42363-136">See note 2.</span></span>       |
| <span data-ttu-id="42363-137">6.0</span><span class="sxs-lookup"><span data-stu-id="42363-137">6.0</span></span>     | <span data-ttu-id="42363-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="42363-138">Windows XP</span></span>                                                                  |
| <span data-ttu-id="42363-139">6.0.1</span><span class="sxs-lookup"><span data-stu-id="42363-139">6.0.1</span></span>   | <span data-ttu-id="42363-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42363-140">Windows Vista</span></span>                                                               |
| <span data-ttu-id="42363-141">6.1</span><span class="sxs-lookup"><span data-stu-id="42363-141">6.1</span></span>     | <span data-ttu-id="42363-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42363-142">Windows 7</span></span>                                                                   |

#### <a name="shlwapidll"></a><span data-ttu-id="42363-143">Shlwapi.dll</span><span class="sxs-lookup"><span data-stu-id="42363-143">Shlwapi.dll</span></span>

| <span data-ttu-id="42363-144">Versão</span><span class="sxs-lookup"><span data-stu-id="42363-144">Version</span></span> | <span data-ttu-id="42363-145">Plataforma de distribuição</span><span class="sxs-lookup"><span data-stu-id="42363-145">Distribution Platform</span></span>                                                       |
|---------|-----------------------------------------------------------------------------|
| <span data-ttu-id="42363-146">4,0</span><span class="sxs-lookup"><span data-stu-id="42363-146">4.0</span></span>     | <span data-ttu-id="42363-147">Windows 95 e Microsoft Windows NT 4,0</span><span class="sxs-lookup"><span data-stu-id="42363-147">Windows 95 and Microsoft Windows NT 4.0</span></span>                                     |
| <span data-ttu-id="42363-148">4,71</span><span class="sxs-lookup"><span data-stu-id="42363-148">4.71</span></span>    | <span data-ttu-id="42363-149">Internet Explorer 4,0.</span><span class="sxs-lookup"><span data-stu-id="42363-149">Internet Explorer 4.0.</span></span> <span data-ttu-id="42363-150">Consulte a observação 1.</span><span class="sxs-lookup"><span data-stu-id="42363-150">See note 1.</span></span>                                          |
| <span data-ttu-id="42363-151">4,72</span><span class="sxs-lookup"><span data-stu-id="42363-151">4.72</span></span>    | <span data-ttu-id="42363-152">Internet Explorer 4, 1 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="42363-152">Internet Explorer 4.01 and Windows 98.</span></span> <span data-ttu-id="42363-153">Consulte a observação 1.</span><span class="sxs-lookup"><span data-stu-id="42363-153">See note 1.</span></span>                          |
| <span data-ttu-id="42363-154">4.7</span><span class="sxs-lookup"><span data-stu-id="42363-154">4.7</span></span>     | <span data-ttu-id="42363-155">Internet Explorer 3. x</span><span class="sxs-lookup"><span data-stu-id="42363-155">Internet Explorer 3.x</span></span>                                                       |
| <span data-ttu-id="42363-156">5.0</span><span class="sxs-lookup"><span data-stu-id="42363-156">5.0</span></span>     | <span data-ttu-id="42363-157">Microsoft Internet Explorer 5 e Windows 98 SE.</span><span class="sxs-lookup"><span data-stu-id="42363-157">Microsoft Internet Explorer 5 and Windows 98 SE.</span></span> <span data-ttu-id="42363-158">Consulte a observação 2.</span><span class="sxs-lookup"><span data-stu-id="42363-158">See note 2.</span></span>                |
| <span data-ttu-id="42363-159">5.5</span><span class="sxs-lookup"><span data-stu-id="42363-159">5.5</span></span>     | <span data-ttu-id="42363-160">Microsoft Internet Explorer 5,5 e Windows Millennium Edition (Windows me)</span><span class="sxs-lookup"><span data-stu-id="42363-160">Microsoft Internet Explorer 5.5 and Windows Millennium Edition (Windows Me)</span></span> |
| <span data-ttu-id="42363-161">6.0</span><span class="sxs-lookup"><span data-stu-id="42363-161">6.0</span></span>     | <span data-ttu-id="42363-162">Windows XP e Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42363-162">Windows XP and Windows Vista</span></span>                                                |



<span data-ttu-id="42363-163">**Observação 1:** Todos os sistemas com o Internet Explorer 4,0 ou 4, 1 tinham a versão associada do Shlwapi.dll (4,71 ou 4,72, respectivamente).</span><span class="sxs-lookup"><span data-stu-id="42363-163">**Note 1:** All systems with Internet Explorer 4.0 or 4.01 had the associated version of Shlwapi.dll (4.71 or 4.72, respectively).</span></span> <span data-ttu-id="42363-164">No entanto, para sistemas anteriores ao Windows 98, o Internet Explorer 4,0 e 4, 1 podem ser instalados com ou sem o que era conhecido como *shell integrado*.</span><span class="sxs-lookup"><span data-stu-id="42363-164">However, for systems prior to Windows 98, Internet Explorer 4.0 and 4.01 can be installed with or without what was known as the *integrated Shell*.</span></span> <span data-ttu-id="42363-165">Se o Internet Explorer foi instalado com o Shell integrado, a versão associada do Shell32.dll (4,71 ou 4,72) também foi instalada.</span><span class="sxs-lookup"><span data-stu-id="42363-165">If Internet Explorer was installed with the integrated Shell, the associated version of Shell32.dll (4.71 or 4.72) was also installed.</span></span> <span data-ttu-id="42363-166">Se o Internet Explorer foi instalado sem o Shell integrado, Shell32.dll permaneceu como a versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="42363-166">If Internet Explorer was installed without the integrated Shell, Shell32.dll remained as version 4.0.</span></span> <span data-ttu-id="42363-167">Em outras palavras, a presença da versão 4,71 ou 4,72 de Shlwapi.dll em um sistema não garante que Shell32.dll tenha o mesmo número de versão.</span><span class="sxs-lookup"><span data-stu-id="42363-167">In other words, the presence of version 4.71 or 4.72 of Shlwapi.dll on a system does not guarantee that Shell32.dll has the same version number.</span></span> <span data-ttu-id="42363-168">Todos os sistemas Windows 98 têm a versão 4,72 do Shell32.dll.</span><span class="sxs-lookup"><span data-stu-id="42363-168">All Windows 98 systems have version 4.72 of Shell32.dll.</span></span>

<span data-ttu-id="42363-169">**Observação 2:** A versão 5,0 do Shlwapi.dll foi distribuída com o Internet Explorer 5 e foi encontrada em todos os sistemas nos quais o Internet Explorer 5 foi instalado, com exceção do Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="42363-169">**Note 2:** Version 5.0 of Shlwapi.dll was distributed with Internet Explorer 5 and was found on all systems on which Internet Explorer 5 was installed, with the exception of Windows 2000.</span></span> <span data-ttu-id="42363-170">A versão 5,0 do Shell32.dll foi distribuída nativamente com o Windows 2000 e o Windows Millennium Edition (Windows me), junto com a versão 5,0 do Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="42363-170">Version 5.0 of Shell32.dll was distributed natively with Windows 2000 and Windows Millennium Edition (Windows Me), together with version 5.0 of Shlwapi.dll.</span></span>

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="42363-171">Usando DllGetVersion para determinar o número de versão</span><span class="sxs-lookup"><span data-stu-id="42363-171">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="42363-172">A partir da versão 4,71, as DLLs do Shell, entre outras, começaram a exportar [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="42363-172">Starting with version 4.71, the Shell DLLs, among others, began exporting [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="42363-173">Essa função pode ser chamada por um aplicativo para determinar qual versão de DLL está presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="42363-173">This function can be called by an application to determine which DLL version is present on the system.</span></span>

> [!Note]  
> <span data-ttu-id="42363-174">As DLLs não necessariamente exportam [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span><span class="sxs-lookup"><span data-stu-id="42363-174">DLLs do not necessarily export [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="42363-175">Sempre teste-o antes de tentar usá-lo.</span><span class="sxs-lookup"><span data-stu-id="42363-175">Always test for it before attempting to use it.</span></span>

<span data-ttu-id="42363-176">Para versões do Windows anteriores ao Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) retorna uma estrutura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) que contém os números de versão principal e secundária, o número da compilação e uma ID de plataforma.</span><span class="sxs-lookup"><span data-stu-id="42363-176">For Windows versions earlier than Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure that contains the major and minor version numbers, the build number, and a platform ID.</span></span> <span data-ttu-id="42363-177">Para sistemas Windows 2000 e posteriores, **DllGetVersion** pode retornar uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="42363-177">For Windows 2000 and later systems, **DllGetVersion** might instead return a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="42363-178">Além das informações fornecidas por meio do **DLLVERSIONINFO**, o **DLLVERSIONINFO2** também fornece o número do hotfix que identifica o Service Pack mais recente instalado, que fornece uma maneira mais robusta de comparar os números de versão.</span><span class="sxs-lookup"><span data-stu-id="42363-178">In addition to the information provided through **DLLVERSIONINFO**, **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="42363-179">Como o primeiro membro de **DLLVERSIONINFO2** é uma estrutura **DLLVERSIONINFO** , a estrutura posterior é compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="42363-179">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>

### <a name="using-dllgetversion"></a><span data-ttu-id="42363-180">Usando DllGetVersion</span><span class="sxs-lookup"><span data-stu-id="42363-180">Using DllGetVersion</span></span>

<span data-ttu-id="42363-181">A função de exemplo a seguir `GetVersion` carrega uma DLL especificada e tenta chamar sua função [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="42363-181">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="42363-182">Se for bem-sucedido, ele usará uma macro para empacotar os números de versão principal e secundária da estrutura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) em um **DWORD** que é retornado para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="42363-182">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="42363-183">Se a DLL não exportar **DllGetVersion**, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="42363-183">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="42363-184">Com o Windows 2000 e sistemas posteriores, você pode modificar a função para lidar com a possibilidade de que **DllGetVersion** retorne uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="42363-184">With Windows 2000 and later systems, you can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="42363-185">Nesse caso, use as informações contidas no membro **ullVersion** da estrutura **DLLVERSIONINFO2** para comparar versões, números de compilação e Service Pack versões.</span><span class="sxs-lookup"><span data-stu-id="42363-185">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="42363-186">A macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) simplifica a tarefa de comparar esses valores com aqueles em **ullVersion**.</span><span class="sxs-lookup"><span data-stu-id="42363-186">The [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="42363-187">Usar [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorretamente pode representar riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="42363-187">Using [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="42363-188">Consulte a documentação de **LoadLibrary** para obter informações sobre como carregar DLLs corretamente com diferentes versões do Windows.</span><span class="sxs-lookup"><span data-stu-id="42363-188">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


<span data-ttu-id="42363-189">O exemplo de código a seguir ilustra como você pode usar o `GetVersion` para testar se Shell32.dll é a versão 6,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-189">The following code example illustrates how you can use `GetVersion` to test whether Shell32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a><span data-ttu-id="42363-190">Versões do projeto</span><span class="sxs-lookup"><span data-stu-id="42363-190">Project Versions</span></span>

<span data-ttu-id="42363-191">Para garantir que seu aplicativo seja compatível com versões de destino diferentes de um arquivo. dll, as macros de versão estão presentes nos arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="42363-191">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="42363-192">Essas macros são usadas para definir, excluir ou redefinir determinadas definições para diferentes versões da DLL.</span><span class="sxs-lookup"><span data-stu-id="42363-192">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="42363-193">Consulte [usando os cabeçalhos do Windows](../winprog/using-the-windows-headers.md) para obter uma descrição detalhada dessas macros.</span><span class="sxs-lookup"><span data-stu-id="42363-193">See [Using the Windows Headers](../winprog/using-the-windows-headers.md) for an in-depth description of these macros.</span></span>

<span data-ttu-id="42363-194">Por exemplo, o nome da macro **\_ Win32 \_ IE** normalmente é encontrado em cabeçalhos mais antigos.</span><span class="sxs-lookup"><span data-stu-id="42363-194">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="42363-195">Você é responsável por definir a macro como um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="42363-195">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="42363-196">Esse número de versão define a versão de destino do aplicativo que está usando a DLL.</span><span class="sxs-lookup"><span data-stu-id="42363-196">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="42363-197">A tabela a seguir mostra os números de versão disponíveis e o efeito que cada um tem em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="42363-197">The following table shows the available version numbers and the effect each has on your application.</span></span>


| <span data-ttu-id="42363-198">Versão</span><span class="sxs-lookup"><span data-stu-id="42363-198">Version</span></span> | <span data-ttu-id="42363-199">Descrição</span><span class="sxs-lookup"><span data-stu-id="42363-199">Description</span></span>                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42363-200">0x0200</span><span class="sxs-lookup"><span data-stu-id="42363-200">0x0200</span></span>  | <span data-ttu-id="42363-201">O aplicativo é compatível com Shell32.dll versão 4, 0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-201">The application is compatible with Shell32.dll version 4.00 and later.</span></span> <span data-ttu-id="42363-202">O aplicativo não pode implementar recursos que foram adicionados após a versão 4, 0.</span><span class="sxs-lookup"><span data-stu-id="42363-202">The application cannot implement features that were added after version 4.00.</span></span>                                              |
| <span data-ttu-id="42363-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="42363-203">0x0300</span></span>  | <span data-ttu-id="42363-204">O aplicativo é compatível com Shell32.dll versão 4,70 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-204">The application is compatible with Shell32.dll version 4.70 and later.</span></span> <span data-ttu-id="42363-205">O aplicativo não pode implementar recursos que foram adicionados após a versão 4,70.</span><span class="sxs-lookup"><span data-stu-id="42363-205">The application cannot implement features that were added after version 4.70.</span></span>                                              |
| <span data-ttu-id="42363-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="42363-206">0x0400</span></span>  | <span data-ttu-id="42363-207">O aplicativo é compatível com Shell32.dll versão 4,71 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-207">The application is compatible with Shell32.dll version 4.71 and later.</span></span> <span data-ttu-id="42363-208">O aplicativo não pode implementar recursos que foram adicionados após a versão 4,71.</span><span class="sxs-lookup"><span data-stu-id="42363-208">The application cannot implement features that were added after version 4.71.</span></span>                                              |
| <span data-ttu-id="42363-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="42363-209">0x0401</span></span>  | <span data-ttu-id="42363-210">O aplicativo é compatível com Shell32.dll versão 4,72 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-210">The application is compatible with Shell32.dll version 4.72 and later.</span></span> <span data-ttu-id="42363-211">O aplicativo não pode implementar recursos que foram adicionados após a versão 4,72.</span><span class="sxs-lookup"><span data-stu-id="42363-211">The application cannot implement features that were added after version 4.72.</span></span>                                              |
| <span data-ttu-id="42363-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="42363-212">0x0500</span></span>  | <span data-ttu-id="42363-213">O aplicativo é compatível com Shell32.dll e Shlwapi.dll versão 5,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-213">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="42363-214">O aplicativo não pode implementar recursos que foram adicionados após a versão 5,0 de Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="42363-214">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="42363-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="42363-215">0x0501</span></span>  | <span data-ttu-id="42363-216">O aplicativo é compatível com Shell32.dll e Shlwapi.dll versão 5,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-216">The application is compatible with Shell32.dll and Shlwapi.dll version 5.0 and later.</span></span> <span data-ttu-id="42363-217">O aplicativo não pode implementar recursos que foram adicionados após a versão 5,0 de Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="42363-217">The application cannot implement features that were added after version 5.0 of Shell32.dll and Shlwapi.dll.</span></span> |
| <span data-ttu-id="42363-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="42363-218">0x0600</span></span>  | <span data-ttu-id="42363-219">O aplicativo é compatível com Shell32.dll e Shlwapi.dll versão 6,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="42363-219">The application is compatible with Shell32.dll and Shlwapi.dll version 6.0 and later.</span></span> <span data-ttu-id="42363-220">O aplicativo não pode implementar recursos que foram adicionados após a versão 6,0 de Shell32.dll e Shlwapi.dll.</span><span class="sxs-lookup"><span data-stu-id="42363-220">The application cannot implement features that were added after version 6.0 of Shell32.dll and Shlwapi.dll.</span></span> |


<span data-ttu-id="42363-221">Se você não definir a macro **\_ \_ IE do Win32** em seu projeto, ela será definida automaticamente como 0x0500.</span><span class="sxs-lookup"><span data-stu-id="42363-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="42363-222">Para definir um valor diferente, você pode adicionar o seguinte às diretivas do compilador em seu arquivo Make; Substitua o número de versão desejado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="42363-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>

```
/D _WIN32_IE=0x0400
```

<span data-ttu-id="42363-223">Outro método é adicionar uma linha semelhante à seguinte em seu código-fonte antes de incluir os arquivos de cabeçalho do Shell.</span><span class="sxs-lookup"><span data-stu-id="42363-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="42363-224">Substitua o número de versão desejado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="42363-224">Substitute the desired version number for 0x0400.</span></span>

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
