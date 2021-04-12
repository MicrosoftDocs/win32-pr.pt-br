---
title: Orientação de texto e fonte internacional
description: Orientação de texto e fonte internacional
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366032"
---
# <a name="international-text-and-font-guidance"></a>Orientação de texto e fonte internacional

## <a name="affected-platforms"></a>Plataformas afetadas

<dl> Clientes-Windows 8 \| Windows 8.1  
Servidores-Windows Server 2012 \| Windows server 2012 R2  
</dl>

## <a name="description"></a>Descrição

Desde antes do Windows 2000, o suporte à exibição de texto para novos scripts foi adicionado em cada versão principal do Windows. Você pode encontrar descrições das alterações feitas em cada versão principal no artigo [suporte de script e fonte para o Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) no centro de [desenvolvimento global go](https://msdn.microsoft.com/goglobal/default).

Observe que o suporte para um script pode exigir certas alterações em componentes de pilha de texto, bem como alterações em fontes. O sistema operacional Windows tem muitos componentes de pilha de texto: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 e outros. As informações fornecidas pertencem principalmente a GDI e DirectWrite. Ele também é geralmente aplicável a estruturas de interface do usuário, como RichEdit ou o agente de renderização MSHTML usado para aplicativos da Windows 8 Store e para renderização de conteúdo da Web, embora esses componentes possam apresentar determinadas diferenças.

## <a name="best-practices"></a>Práticas Recomendadas

**Diretrizes de tipografia para desenvolvedores**

A tipografia é o coração da linguagem de design da Microsoft. Cada um dos princípios de design da Microsoft reforça a importância da tipografia. Pela primeira vez, os desenvolvedores de aplicativos têm um conjunto de estruturas que dão suporte a recursos tipográficos avançados. Vá para [exibindo e editando texto](/previous-versions/windows/apps/hh465442(v=win.10)) para obter informações sobre como usar JavaScript e HTML para exibir e editar texto em aplicativos da Windows Store.

**Métricas de fonte**

As métricas de fonte são uma área de importância específica para os desenvolvedores de aplicativos. Os arquivos de fonte contêm vários valores relacionados a métricas verticais e horizontais. Esses valores são documentados na [especificação OpenType](https://www.microsoft.com/typography/otspec/) e são expostos por meio de uma variedade de APIs encontradas [na \_ \_ estrutura de métricas de fonte DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) e na [estrutura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Recursos

-   [Suporte a scripts e fontes para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Ir para o centro de desenvolvimento global](https://msdn.microsoft.com/goglobal/default)
-   [Exibindo e editando texto](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Especificação de OpenType](https://www.microsoft.com/typography/otspec/)
-   [\_Estrutura de \_ métricas de fonte DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Estrutura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 