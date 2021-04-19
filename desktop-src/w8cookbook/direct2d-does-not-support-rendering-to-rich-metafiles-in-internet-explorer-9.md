---
title: Direct2D não dá suporte à renderização para metaarquivos avançados no Internet Explorer 9
description: Direct2D não dá suporte à renderização para metaarquivos avançados no Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f51ae6d098c08c0a18656aae2adf3d79d68652
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314819"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D não dá suporte à renderização para metaarquivos avançados no Internet Explorer 9

## <a name="platforms"></a>Plataformas

**Clientes** – Windows Vista, Windows 7, Windows 8  
**Servidores** – windows Server 2008, windows Server 2008 R2, windows Server 2012  




## <a name="description"></a>Descrição

Devido a alterações de renderização internas no Internet Explorer 9, as APIs [IHTMLElementRender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) agora criarão um metarquivo contendo um único bitmap que representa o conteúdo da Web em vez de um metarquivo avançado contendo informações de texto e vetor. Essa alteração ocorreu devido à mudança do processamento de GDI para a renderização de Direct2D (D2D) acelerada por hardware.

Essa alteração afeta os aplicativos que usam essas APIs e dependem do texto ou das informações de vetor no metarquivo.

## <a name="manifestation"></a>Manifestação

Dependendo do aplicativo que é afetado por essa alteração, os usuários poderão ver o comportamento corrompido ou incorreto em seus aplicativos.

## <a name="mitigation"></a>Atenuação

Os aplicativos que só precisam extrair informações de texto de um documento da Web (sem informações de posicionamento) podem usar a propriedade [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) para extrair o texto.

Os aplicativos que usam IViewObject::D RAW podem usar o [recurso \_ IVIEWOBJECTDRAW \_ DMLT9 \_ com \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) a chave de controle de recurso GDI para reverter para a renderização GDI se o modo de documento:

-   É menor ou igual a 8
-   O FCK autoriza esse host a usar o GDI
-   E um DC de metarquivo é passado para a API

## <a name="resources"></a>Recursos

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D bruto](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [Propriedade IHTMLElement:: innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Controles de recursos da Internet (I... Debug](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 