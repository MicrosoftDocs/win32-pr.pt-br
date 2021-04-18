---
description: 'Saiba mais sobre: definindo o reconhecimento de DPI padrão para um processo'
title: Definindo o reconhecimento de DPI padrão para um processo (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105780739"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="73494-103">Definindo o reconhecimento de DPI padrão para um processo</span><span class="sxs-lookup"><span data-stu-id="73494-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="73494-104">Os aplicativos de área de trabalho no Windows podem ser executados em modos de reconhecimento de DPI diferentes.</span><span class="sxs-lookup"><span data-stu-id="73494-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="73494-105">Esses modos permitem um comportamento de escala de DPI diferente e podem usar espaços de coordenadas diferentes.</span><span class="sxs-lookup"><span data-stu-id="73494-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="73494-106">Para obter mais informações sobre reconhecimento de DPI, consulte [desenvolvimento de aplicativos para desktop de alto dpi no Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="73494-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="73494-107">É importante definir explicitamente o modo de reconhecimento de DPI padrão do seu processo para evitar um comportamento inesperado.</span><span class="sxs-lookup"><span data-stu-id="73494-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="73494-108">Há dois métodos principais para especificar o reconhecimento de DPI padrão de um processo:</span><span class="sxs-lookup"><span data-stu-id="73494-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="73494-109">1 \) por meio de uma configuração de manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="73494-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="73494-110">2 \) programaticamente por meio de uma chamada à API</span><span class="sxs-lookup"><span data-stu-id="73494-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="73494-111">Recomendamos que você especifique o reconhecimento de DPI de processo padrão por meio de uma configuração de manifesto.</span><span class="sxs-lookup"><span data-stu-id="73494-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="73494-112">Embora a especificação do padrão via API tenha suporte, isso não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="73494-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="73494-113">Configurando o reconhecimento padrão com o manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="73494-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="73494-114">Há duas configurações de manifesto que permitem especificar o modo de reconhecimento de DPI padrão do processo: \<dpiAwareness\> e \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="73494-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="73494-115">\<dpiAware\> foi introduzido no Windows Vista e só permite que o seu processo seja definido como reconhecimento do sistema.</span><span class="sxs-lookup"><span data-stu-id="73494-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="73494-116">\<dpiAwareness\> foi introduzido no Windows 10, versão 1607 e permite que você especifique uma lista ordenada de modos de reconhecimento de DPI de processo padrão.</span><span class="sxs-lookup"><span data-stu-id="73494-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="73494-117">Isso permite que você defina modos de reconhecimento de DPI de backup, que serão usados se seu aplicativo for executado em uma versão do Windows que não pode oferecer suporte ao modo de reconhecimento especificado.</span><span class="sxs-lookup"><span data-stu-id="73494-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="73494-118">Em versões mais antigas do Windows, a \<dpiAwareness\> marca mais recente será ignorada.</span><span class="sxs-lookup"><span data-stu-id="73494-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="73494-119">Isso significa que você pode usar ambas as configurações de manifesto para habilitar um cenário em que o padrão do processo pode ser o reconhecimento do sistema em uma versão mais antiga do Windows enquanto está sendo Per-Monitor em versões superiores ao Windows 10, versão 1607.</span><span class="sxs-lookup"><span data-stu-id="73494-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="73494-120">No Windows 10, versão 1607 e em, a \<dpiAware\> configuração será ignorada se o \<dpiAwareness\> elemento estiver presente.</span><span class="sxs-lookup"><span data-stu-id="73494-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="73494-121">A tabela a seguir mostra como especificar modos de reconhecimento de DPI de processo padrão diferentes usando as duas configurações de manifesto:</span><span class="sxs-lookup"><span data-stu-id="73494-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73494-122">Processar o modo de reconhecimento de DPI padrão</span><span class="sxs-lookup"><span data-stu-id="73494-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="73494-123">&lt;configuração de dpiAware &gt;</span><span class="sxs-lookup"><span data-stu-id="73494-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="73494-124">&lt;&gt;configuração de dpiAwareness (Windows 10, versão 1607 e posterior)</span><span class="sxs-lookup"><span data-stu-id="73494-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73494-125">conhecida</span><span class="sxs-lookup"><span data-stu-id="73494-125">unaware</span></span></td>
<td><p><span data-ttu-id="73494-126">N/d (nenhuma configuração de dpiAware no manifesto)</span><span class="sxs-lookup"><span data-stu-id="73494-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="73494-127">ou</span><span class="sxs-lookup"><span data-stu-id="73494-127">or</span></span></p>
<p><span data-ttu-id="73494-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="73494-129">&lt;dpiAwareness sem &gt; reconhecimento de &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73494-130">Reconhecimento do sistema</span><span class="sxs-lookup"><span data-stu-id="73494-130">System aware</span></span></td>
<td><span data-ttu-id="73494-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="73494-132">&lt;dpiAwareness &gt; sistema &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73494-133">Por monitor</span><span class="sxs-lookup"><span data-stu-id="73494-133">Per Monitor</span></span></td>
<td><span data-ttu-id="73494-134">&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="73494-135">&lt;dpiAwareness &gt; Permonitoring &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73494-136">Por monitor v2</span><span class="sxs-lookup"><span data-stu-id="73494-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="73494-137">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="73494-137">Not supported</span></span></td>
<td><span data-ttu-id="73494-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="73494-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="73494-139">O exemplo a seguir mostra o \<dpiAwareness\> e as \<dpiAware\> configurações que estão sendo usadas no mesmo arquivo de manifesto para configurar o comportamento de reconhecimento de dpi de processo padrão para versões diferentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="73494-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

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

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="73494-140">Configurando reconhecimento padrão programaticamente</span><span class="sxs-lookup"><span data-stu-id="73494-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="73494-141">Embora não seja recomendado, é possível definir o reconhecimento de DPI padrão programaticamente.</span><span class="sxs-lookup"><span data-stu-id="73494-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="73494-142">Depois que uma janela (um HWND) tiver sido criada em seu processo, não haverá mais suporte para a alteração do modo de reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="73494-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="73494-143">Se você estiver configurando o modo de reconhecimento de DPI de processo padrão programaticamente, deverá chamar a API correspondente antes que quaisquer HWNDs tenham sido criados.</span><span class="sxs-lookup"><span data-stu-id="73494-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="73494-144">Há várias APIs que permitem especificar o reconhecimento de DPI padrão para seu processo.</span><span class="sxs-lookup"><span data-stu-id="73494-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="73494-145">A API recomendada atual é [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), pois as APIs mais antigas oferecem menos funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="73494-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

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
<th><span data-ttu-id="73494-146">API</span><span class="sxs-lookup"><span data-stu-id="73494-146">API</span></span></th>
<th><span data-ttu-id="73494-147">Versão mínima do Windows</span><span class="sxs-lookup"><span data-stu-id="73494-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="73494-148">Sem reconhecimento de DPI</span><span class="sxs-lookup"><span data-stu-id="73494-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="73494-149">Reconhecimento de DPI do sistema</span><span class="sxs-lookup"><span data-stu-id="73494-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="73494-150">Reconhecimento de DPI por monitor</span><span class="sxs-lookup"><span data-stu-id="73494-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73494-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span><span class="sxs-lookup"><span data-stu-id="73494-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span></span></td>
<td><span data-ttu-id="73494-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73494-152">Windows Vista</span></span></td>
<td><span data-ttu-id="73494-153">N/D</span><span class="sxs-lookup"><span data-stu-id="73494-153">N/A</span></span></td>
<td><span data-ttu-id="73494-154">SetProcessDpiAware()</span><span class="sxs-lookup"><span data-stu-id="73494-154">SetProcessDpiAware()</span></span></td>
<td><span data-ttu-id="73494-155">N/D</span><span class="sxs-lookup"><span data-stu-id="73494-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73494-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="73494-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="73494-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="73494-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="73494-158">SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="73494-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="73494-159">SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="73494-159">SetProcessDpiAwareness(PROCESS_DPI_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="73494-160">SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="73494-160">SetProcessDpiAwareness(PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73494-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="73494-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="73494-162">Windows 10, versão 1607</span><span class="sxs-lookup"><span data-stu-id="73494-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="73494-163">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="73494-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="73494-164">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="73494-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="73494-165">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="73494-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="73494-166">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="73494-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="73494-167">Processo-padrão versus thread padrão</span><span class="sxs-lookup"><span data-stu-id="73494-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="73494-168">Este documento refere-se à definição do reconhecimento de DPI padrão para seu processo.</span><span class="sxs-lookup"><span data-stu-id="73494-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="73494-169">Isso ocorre porque o Windows 10 introduziu o suporte para executar mais de um modo de reconhecimento de DPI em um único processo (antes do Windows 10, o processo inteiro tinha de estar em conformidade com um modo de reconhecimento de DPI único).</span><span class="sxs-lookup"><span data-stu-id="73494-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="73494-170">O suporte para executar mais de um modo de reconhecimento de DPI em um processo é conhecido como "escala de DPI de modo misto".</span><span class="sxs-lookup"><span data-stu-id="73494-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="73494-171">Ao usar o dimensionamento de DPI de modo misto em seu processo, cada janela de nível superior pode ser executada em um modo de reconhecimento de DPI que pode ser diferente daquele do padrão de processo.</span><span class="sxs-lookup"><span data-stu-id="73494-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="73494-172">A menos que seja especificado explicitamente, cada thread usará como padrão o processo padrão quando for criado.</span><span class="sxs-lookup"><span data-stu-id="73494-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="73494-173">Para obter mais informações sobre o dimensionamento de DPI de modo misto, consulte o artigo [escala de dpi de modo misto](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .</span><span class="sxs-lookup"><span data-stu-id="73494-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>
