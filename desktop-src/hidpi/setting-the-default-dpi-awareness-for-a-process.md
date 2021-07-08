---
description: 'Saiba mais sobre: Definindo o reconhecimento de DPI padrão para um processo'
title: Definindo o reconhecimento de DPI padrão para um processo (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: c9192bf650588b7c21f17afb45149fe460f91bea
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481861"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="e8352-103">Definindo o reconhecimento de DPI padrão para um processo</span><span class="sxs-lookup"><span data-stu-id="e8352-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="e8352-104">Aplicativos da área de Windows podem ser executados em diferentes modos de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e8352-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="e8352-105">Esses modos permitem um comportamento de dimensionamento de DPI diferente e podem usar espaços de coordenadas diferentes.</span><span class="sxs-lookup"><span data-stu-id="e8352-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="e8352-106">Para obter mais informações sobre reconhecimento de DPI, consulte Desenvolvimento de aplicativos de área de [trabalho de DPI alta Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="e8352-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="e8352-107">É importante definir explicitamente o modo de reconhecimento de DPI padrão do processo para evitar um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="e8352-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="e8352-108">Há dois métodos principais para especificar o reconhecimento de DPI padrão de um processo:</span><span class="sxs-lookup"><span data-stu-id="e8352-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="e8352-109">1 \) por meio de uma configuração de manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e8352-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="e8352-110">2 \) programaticamente por meio de uma chamada à API</span><span class="sxs-lookup"><span data-stu-id="e8352-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="e8352-111">Recomendamos que você especifique o reconhecimento de DPI do processo padrão por meio de uma configuração de manifesto.</span><span class="sxs-lookup"><span data-stu-id="e8352-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="e8352-112">Embora seja possível especificar o padrão por meio da API, não é recomendável.</span><span class="sxs-lookup"><span data-stu-id="e8352-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="e8352-113">Definindo o reconhecimento padrão com o manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="e8352-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="e8352-114">Há duas configurações de manifesto que permitem que você especifique o modo de reconhecimento de DPI padrão do processo: \<dpiAwareness\> e \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="e8352-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="e8352-115">\<dpiAware\>foi introduzido no Windows Vista e permite que o padrão do processo seja definido como reconhecimento do sistema.</span><span class="sxs-lookup"><span data-stu-id="e8352-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="e8352-116">\<dpiAwareness\>foi introduzido no Windows 10, versão 1607 e permite que você especifique uma lista ordenada de modos de reconhecimento de DPI padrão do processo.</span><span class="sxs-lookup"><span data-stu-id="e8352-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="e8352-117">Isso permite definir modos de reconhecimento de DPI de backup, que serão usados se o aplicativo for usado em uma versão do Windows não puder dar suporte ao primeiro modo de reconhecimento especificado.</span><span class="sxs-lookup"><span data-stu-id="e8352-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="e8352-118">Em versões mais antigas Windows, a marca \<dpiAwareness\> mais nova será ignorada.</span><span class="sxs-lookup"><span data-stu-id="e8352-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="e8352-119">Isso significa que você pode usar essas duas configurações de manifesto para habilitar um cenário em que o padrão do processo pode ser o reconhecimento do sistema sobre a versão mais antiga do Windows enquanto estiver Per-Monitor em versões maiores que Windows 10, versão 1607.</span><span class="sxs-lookup"><span data-stu-id="e8352-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="e8352-120">No Windows 10, versão 1607 e on, a configuração será \<dpiAware\> ignorada se o \<dpiAwareness\> elemento estiver presente.</span><span class="sxs-lookup"><span data-stu-id="e8352-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="e8352-121">A tabela a seguir mostra como especificar diferentes modos de reconhecimento de DPI padrão do processo usando as duas configurações de manifesto:</span><span class="sxs-lookup"><span data-stu-id="e8352-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8352-122">Processar o modo de reconhecimento de DPI padrão</span><span class="sxs-lookup"><span data-stu-id="e8352-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="e8352-123">&lt;Configuração de &gt; dpiAware</span><span class="sxs-lookup"><span data-stu-id="e8352-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="e8352-124">&lt;Configuração de dpiAwareness &gt; (Windows 10, versão 1607 e posterior)</span><span class="sxs-lookup"><span data-stu-id="e8352-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8352-125">Inconscientes</span><span class="sxs-lookup"><span data-stu-id="e8352-125">unaware</span></span></td>
<td><p><span data-ttu-id="e8352-126">N/A (nenhuma configuração de dpiAware no manifesto)</span><span class="sxs-lookup"><span data-stu-id="e8352-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="e8352-127">ou</span><span class="sxs-lookup"><span data-stu-id="e8352-127">or</span></span></p>
<p><span data-ttu-id="e8352-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="e8352-129">&lt;dpiAwareness &gt; não &lt; ciente /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8352-130">Ciente do sistema</span><span class="sxs-lookup"><span data-stu-id="e8352-130">System aware</span></span></td>
<td><span data-ttu-id="e8352-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="e8352-132">&lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8352-133">Por Monitor</span><span class="sxs-lookup"><span data-stu-id="e8352-133">Per Monitor</span></span></td>
<td><span data-ttu-id="e8352-134">&lt;dpiAware &gt; true/pm &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="e8352-135">&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8352-136">Por Monitor V2</span><span class="sxs-lookup"><span data-stu-id="e8352-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="e8352-137">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="e8352-137">Not supported</span></span></td>
<td><span data-ttu-id="e8352-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="e8352-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="e8352-139">O exemplo a seguir mostra as configurações e sendo usadas dentro do mesmo arquivo de manifesto para configurar o comportamento de reconhecimento de DPI padrão do processo para diferentes versões \<dpiAwareness\> \<dpiAware\> do Windows.</span><span class="sxs-lookup"><span data-stu-id="e8352-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="e8352-140">Definindo o reconhecimento padrão programaticamente</span><span class="sxs-lookup"><span data-stu-id="e8352-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="e8352-141">Embora não seja recomendável, é possível definir o reconhecimento de DPI padrão programaticamente.</span><span class="sxs-lookup"><span data-stu-id="e8352-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="e8352-142">Depois que uma janela (um HWND) tiver sido criada em seu processo, não haverá mais suporte para alterar o modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="e8352-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="e8352-143">Se você estiver definindo o modo de reconhecimento de DPI padrão do processo programaticamente, deverá chamar a API correspondente antes de qualquer HWNDs ter sido criado.</span><span class="sxs-lookup"><span data-stu-id="e8352-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="e8352-144">Há várias APIs que permitem especificar o reconhecimento de DPI padrão para seu processo.</span><span class="sxs-lookup"><span data-stu-id="e8352-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="e8352-145">A API recomendada atual é [**SetProcessDpiAwarenessContext, pois**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))as APIs mais antigas oferecem menos funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="e8352-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8352-146">API</span><span class="sxs-lookup"><span data-stu-id="e8352-146">API</span></span></th>
<th><span data-ttu-id="e8352-147">Versão mínima do Windows</span><span class="sxs-lookup"><span data-stu-id="e8352-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="e8352-148">DPI sem conhecimento</span><span class="sxs-lookup"><span data-stu-id="e8352-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="e8352-149">Ciente de DPI do sistema</span><span class="sxs-lookup"><span data-stu-id="e8352-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="e8352-150">Por monitor com conhecimento de DPI</span><span class="sxs-lookup"><span data-stu-id="e8352-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e8352-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span><span class="sxs-lookup"><span data-stu-id="e8352-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span></span></td>
<td><span data-ttu-id="e8352-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8352-152">Windows Vista</span></span></td>
<td><span data-ttu-id="e8352-153">N/D</span><span class="sxs-lookup"><span data-stu-id="e8352-153">N/A</span></span></td>
<td><span data-ttu-id="e8352-154">SetProcessDPIAware()</span><span class="sxs-lookup"><span data-stu-id="e8352-154">SetProcessDPIAware()</span></span></td>
<td><span data-ttu-id="e8352-155">N/D</span><span class="sxs-lookup"><span data-stu-id="e8352-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e8352-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8352-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="e8352-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e8352-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="e8352-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="e8352-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="e8352-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="e8352-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="e8352-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="e8352-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e8352-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="e8352-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="e8352-162">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="e8352-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="e8352-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="e8352-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="e8352-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="e8352-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="e8352-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="e8352-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="e8352-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="e8352-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="e8352-167">Padrão de processo vs. Padrão de thread</span><span class="sxs-lookup"><span data-stu-id="e8352-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="e8352-168">Este documento refere-se à configuração do reconhecimento de DPI padrão para seu processo.</span><span class="sxs-lookup"><span data-stu-id="e8352-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="e8352-169">Isso porque Windows 10 suporte para executar mais de um modo de reconhecimento de DPI em um único processo (antes do Windows 10, todo o processo precisava estar em conformidade com um único modo de reconhecimento de DPI).</span><span class="sxs-lookup"><span data-stu-id="e8352-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="e8352-170">O suporte para executar mais de um modo de reconhecimento de DPI dentro de um processo é conhecido como "dimensionamento de DPI de modo misto".</span><span class="sxs-lookup"><span data-stu-id="e8352-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="e8352-171">Ao usar o dimensionamento de DPI de modo misto em seu processo, cada Janela de nível superior pode ser executado em um modo de reconhecimento de DPI que pode ser diferente do padrão do processo.</span><span class="sxs-lookup"><span data-stu-id="e8352-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="e8352-172">A menos que especificado explicitamente, cada thread será padrão para o processo padrão quando criado.</span><span class="sxs-lookup"><span data-stu-id="e8352-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="e8352-173">Para obter mais informações sobre o dimensionamento de DPI de modo misto, consulte o artigo [Dimensionamento de DPI](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) de modo misto.</span><span class="sxs-lookup"><span data-stu-id="e8352-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
