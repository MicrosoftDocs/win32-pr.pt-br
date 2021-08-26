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
ms.openlocfilehash: 216952ac05811226c403739d389f8de9f636c3b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880530"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Definindo o reconhecimento de DPI padrão para um processo

Aplicativos da área de Windows podem ser executados em diferentes modos de reconhecimento de DPI. Esses modos permitem um comportamento de dimensionamento de DPI diferente e podem usar espaços de coordenadas diferentes. Para obter mais informações sobre reconhecimento de DPI, consulte Desenvolvimento de aplicativos de área de [trabalho de DPI alto Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) É importante definir explicitamente o modo de reconhecimento de DPI padrão do processo para evitar um comportamento inesperado.

Há dois métodos principais para especificar o reconhecimento de DPI padrão de um processo:

1 \) por meio de uma configuração de manifesto do aplicativo

2 \) programaticamente por meio de uma chamada à API

Recomendamos que você especifique o reconhecimento de DPI do processo padrão por meio de uma configuração de manifesto. Embora seja possível especificar o padrão por meio da API, não é recomendável.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Definindo o reconhecimento padrão com o manifesto do aplicativo

Há duas configurações de manifesto que permitem que você especifique o modo de reconhecimento de DPI padrão do processo: \<dpiAwareness\> e \<dpiAware\> . \<dpiAware\>foi introduzido no Windows Vista e permite que o padrão do processo seja definido como reconhecimento do sistema. \<dpiAwareness\>foi introduzido no Windows 10, versão 1607 e permite que você especifique uma lista ordenada de modos de reconhecimento de DPI padrão do processo. Isso permite definir modos de reconhecimento de DPI de backup, que serão usados se o aplicativo for usado em uma versão do Windows não puder dar suporte ao primeiro modo de reconhecimento especificado. Em versões mais antigas Windows, a marca \<dpiAwareness\> mais nova será ignorada. Isso significa que você pode usar essas duas configurações de manifesto para habilitar um cenário em que o padrão do processo pode ser o reconhecimento do sistema sobre a versão mais antiga do Windows enquanto está sendo Per-Monitor em versões maiores que Windows 10, versão 1607. No Windows 10, versão 1607 e on, a configuração será \<dpiAware\> ignorada se o \<dpiAwareness\> elemento estiver presente.

A tabela a seguir mostra como especificar diferentes modos de reconhecimento de DPI padrão do processo usando as duas configurações de manifesto:


| Processar o modo de reconhecimento de DPI padrão | &lt;Configuração de &gt; dpiAware | &lt;Configuração de dpiAwareness &gt; (Windows 10, versão 1607 e posterior) | 
|------------------------------------|--------------------|--------------------------------------------------------------|
| Inconscientes | <p>N/A (nenhuma configuração de dpiAware no manifesto)</p><p>ou</p><p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p> | &lt;dpiAwareness &gt; não &lt; ciente /dpiAwareness&gt; | 
| Ciente do sistema | &lt;dpiAware &gt; true &lt; /dpiAware&gt; | &lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt; | 
| Por Monitor | &lt;dpiAware &gt; true/pm &lt; dpiAware&gt; | &lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt; | 
| Por Monitor V2 | Sem suporte | &lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt; | 


 

O exemplo a seguir mostra as configurações que estão sendo usadas dentro do mesmo arquivo de manifesto para configurar o comportamento de reconhecimento de DPI padrão do processo para diferentes versões \<dpiAwareness\> \<dpiAware\> do Windows.

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

## <a name="setting-default-awareness-programmatically"></a>Definindo o reconhecimento padrão programaticamente

Embora não seja recomendável, é possível definir o reconhecimento de DPI padrão programaticamente. Depois que uma janela (um HWND) tiver sido criada em seu processo, não haverá mais suporte para alterar o modo de reconhecimento de DPI. Se você estiver definindo o modo de reconhecimento de DPI padrão do processo programaticamente, deverá chamar a API correspondente antes de qualquer HWNDs ter sido criado.

Há várias APIs que permitem especificar o reconhecimento de DPI padrão para seu processo. A API recomendada atual é [**SetProcessDpiAwarenessContext, pois**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))as APIs mais antigas oferecem menos funcionalidade.

 


| API | Versão mínima do Windows | DPI sem conhecimento | Ciente de DPI do sistema | Por monitor com conhecimento de DPI | 
|-----|----------------------------|-------------|------------------|-----------------------|
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a> | Windows Vista | N/D | SetProcessDPIAware() | N/D | 
| <a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a> | Windows 8.1 | SetProcessDpiAwareness(PROCESS_DPI_UNAWARE) | SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE) | SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE) | 
| <a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a> | Windows 10, versão 1607 | SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE) | SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE) | <p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p><p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p> | 


 

## <a name="process-default-vs-thread-default"></a>Padrão de processo vs. Padrão de thread

Este documento refere-se à configuração do reconhecimento de DPI padrão para seu processo. Isso porque Windows 10 suporte para executar mais de um modo de reconhecimento de DPI em um único processo (antes do Windows 10, todo o processo precisava estar em conformidade com um único modo de reconhecimento de DPI). O suporte para executar mais de um modo de reconhecimento de DPI dentro de um processo é conhecido como "dimensionamento de DPI de modo misto". Ao usar o dimensionamento de DPI de modo misto em seu processo, cada Janela de nível superior pode ser executado em um modo de reconhecimento de DPI que pode ser diferente do padrão do processo. A menos que especificado explicitamente, cada thread será padrão para o processo padrão quando criado. Para obter mais informações sobre o dimensionamento de DPI de modo misto, consulte o artigo [Dimensionamento de DPI](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) de modo misto.
