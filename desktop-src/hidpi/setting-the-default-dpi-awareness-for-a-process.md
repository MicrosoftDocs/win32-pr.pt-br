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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Definindo o reconhecimento de DPI padrão para um processo

Os aplicativos de área de trabalho no Windows podem ser executados em modos de reconhecimento de DPI diferentes. Esses modos permitem um comportamento de escala de DPI diferente e podem usar espaços de coordenadas diferentes. Para obter mais informações sobre reconhecimento de DPI, consulte [desenvolvimento de aplicativos para desktop de alto dpi no Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) É importante definir explicitamente o modo de reconhecimento de DPI padrão do seu processo para evitar um comportamento inesperado.

Há dois métodos principais para especificar o reconhecimento de DPI padrão de um processo:

1 \) por meio de uma configuração de manifesto do aplicativo

2 \) programaticamente por meio de uma chamada à API

Recomendamos que você especifique o reconhecimento de DPI de processo padrão por meio de uma configuração de manifesto. Embora a especificação do padrão via API tenha suporte, isso não é recomendado.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Configurando o reconhecimento padrão com o manifesto do aplicativo

Há duas configurações de manifesto que permitem especificar o modo de reconhecimento de DPI padrão do processo: \<dpiAwareness\> e \<dpiAware\> . \<dpiAware\> foi introduzido no Windows Vista e só permite que o seu processo seja definido como reconhecimento do sistema. \<dpiAwareness\> foi introduzido no Windows 10, versão 1607 e permite que você especifique uma lista ordenada de modos de reconhecimento de DPI de processo padrão. Isso permite que você defina modos de reconhecimento de DPI de backup, que serão usados se seu aplicativo for executado em uma versão do Windows que não pode oferecer suporte ao modo de reconhecimento especificado. Em versões mais antigas do Windows, a \<dpiAwareness\> marca mais recente será ignorada. Isso significa que você pode usar ambas as configurações de manifesto para habilitar um cenário em que o padrão do processo pode ser o reconhecimento do sistema em uma versão mais antiga do Windows enquanto está sendo Per-Monitor em versões superiores ao Windows 10, versão 1607. No Windows 10, versão 1607 e em, a \<dpiAware\> configuração será ignorada se o \<dpiAwareness\> elemento estiver presente.

A tabela a seguir mostra como especificar modos de reconhecimento de DPI de processo padrão diferentes usando as duas configurações de manifesto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Processar o modo de reconhecimento de DPI padrão</th>
<th>&lt;configuração de dpiAware &gt;</th>
<th>&lt;&gt;configuração de dpiAwareness (Windows 10, versão 1607 e posterior)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>conhecida</td>
<td><p>N/d (nenhuma configuração de dpiAware no manifesto)</p>
<p>ou</p>
<p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;dpiAwareness sem &gt; reconhecimento de &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Reconhecimento do sistema</td>
<td>&lt;dpiAware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; sistema &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="odd">
<td>Por monitor</td>
<td>&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; Permonitoring &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Por monitor v2</td>
<td>Sem suporte</td>
<td>&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</td>
</tr>
</tbody>
</table>

 

O exemplo a seguir mostra o \<dpiAwareness\> e as \<dpiAware\> configurações que estão sendo usadas no mesmo arquivo de manifesto para configurar o comportamento de reconhecimento de dpi de processo padrão para versões diferentes do Windows.

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

## <a name="setting-default-awareness-programmatically"></a>Configurando reconhecimento padrão programaticamente

Embora não seja recomendado, é possível definir o reconhecimento de DPI padrão programaticamente. Depois que uma janela (um HWND) tiver sido criada em seu processo, não haverá mais suporte para a alteração do modo de reconhecimento de DPI. Se você estiver configurando o modo de reconhecimento de DPI de processo padrão programaticamente, deverá chamar a API correspondente antes que quaisquer HWNDs tenham sido criados.

Há várias APIs que permitem especificar o reconhecimento de DPI padrão para seu processo. A API recomendada atual é [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), pois as APIs mais antigas oferecem menos funcionalidade.

 

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
<th>API</th>
<th>Versão mínima do Windows</th>
<th>Sem reconhecimento de DPI</th>
<th>Reconhecimento de DPI do sistema</th>
<th>Reconhecimento de DPI por monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></td>
<td>Windows Vista</td>
<td>N/D</td>
<td>SetProcessDpiAware()</td>
<td>N/D</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></td>
<td>Windows 10, versão 1607</td>
<td>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Processo-padrão versus thread padrão

Este documento refere-se à definição do reconhecimento de DPI padrão para seu processo. Isso ocorre porque o Windows 10 introduziu o suporte para executar mais de um modo de reconhecimento de DPI em um único processo (antes do Windows 10, o processo inteiro tinha de estar em conformidade com um modo de reconhecimento de DPI único). O suporte para executar mais de um modo de reconhecimento de DPI em um processo é conhecido como "escala de DPI de modo misto". Ao usar o dimensionamento de DPI de modo misto em seu processo, cada janela de nível superior pode ser executada em um modo de reconhecimento de DPI que pode ser diferente daquele do padrão de processo. A menos que seja especificado explicitamente, cada thread usará como padrão o processo padrão quando for criado. Para obter mais informações sobre o dimensionamento de DPI de modo misto, consulte o artigo [escala de dpi de modo misto](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .
