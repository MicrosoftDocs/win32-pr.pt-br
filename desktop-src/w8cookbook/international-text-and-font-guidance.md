---
title: Orientação de texto e fonte internacional
description: Orientação de texto e fonte internacional
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eeeeaf59f777610603787c3b8e6ed248f36810d34fc2026466b72ca57a1883
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935396"
---
# <a name="international-text-and-font-guidance"></a>Orientação de texto e fonte internacional

## <a name="affected-platforms"></a>Plataformas afetadas

<dl> clientes-Windows 8 \| Windows 8.1  
servidores-Windows Server 2012 \| Windows Server 2012 R2  
</dl>

## <a name="description"></a>Descrição

desde que antes da Windows 2000, o suporte à exibição de texto para novos scripts foi adicionado em cada versão principal do Windows. você pode encontrar descrições das alterações feitas em cada versão principal no suporte de [scripts e fontes para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) artigo no centro de [desenvolvimento Global](https://msdn.microsoft.com/goglobal/default).

Observe que o suporte para um script pode exigir certas alterações em componentes de pilha de texto, bem como alterações em fontes. o sistema operacional Windows tem muitos componentes de pilha de texto: DirectWrite, GDI, uniscribe, GDI+, WPF, RichEdit, ComCtl32 e outros. As informações fornecidas pertencem principalmente a GDI e DirectWrite. ele também é geralmente aplicável a estruturas de interface do usuário, como RichEdit ou o agente de renderização MSHTML usado para Windows 8 aplicativos da loja e para renderizar conteúdo da web, embora esses componentes possam apresentar determinadas diferenças.

## <a name="best-practices"></a>Práticas Recomendadas

**Diretrizes de tipografia para desenvolvedores**

A tipografia é o coração da linguagem de design da Microsoft. Cada um dos princípios de design da Microsoft reforça a importância da tipografia. Pela primeira vez, os desenvolvedores de aplicativos têm um conjunto de estruturas que dão suporte a recursos tipográficos avançados. vá para [exibindo e editando texto](/previous-versions/windows/apps/hh465442(v=win.10)) para obter informações sobre como usar JavaScript e HTML para exibir e editar texto em aplicativos da Windows store.

**Métricas de fonte**

As métricas de fonte são uma área de importância específica para os desenvolvedores de aplicativos. Os arquivos de fonte contêm vários valores relacionados a métricas verticais e horizontais. Esses valores são documentados na [especificação OpenType](https://www.microsoft.com/typography/otspec/) e são expostos por meio de uma variedade de APIs encontradas [na \_ \_ estrutura de métricas de fonte DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) e na [estrutura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

## <a name="resources"></a>Recursos

-   [Suporte a scripts e fontes para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [Ir para o centro de desenvolvimento global](https://msdn.microsoft.com/goglobal/default)
-   [Exibindo e editando texto](/previous-versions/windows/apps/hh465442(v=win.10))
-   [Especificação de OpenType](https://www.microsoft.com/typography/otspec/)
-   [\_Estrutura de \_ métricas de fonte DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [Estrutura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 