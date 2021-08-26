---
title: Direct2D não dá suporte à renderização para metadados avançado no Internet Explorer 9
description: Direct2D não dá suporte à renderização para metadados avançado no Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebe10310202385fa4e9458cb1a442cbf98a3f6f178331d888c096449631ca61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057346"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a>Direct2D não dá suporte à renderização para metadados avançado no Internet Explorer 9

## <a name="platforms"></a>Plataformas

**Clientes** – Windows Vista, Windows 7, Windows 8  
**Servidores** – Windows Server 2008, Windows Server 2008 R2, Windows Server 2012  




## <a name="description"></a>Descrição

Devido a alterações de renderização internas no Internet Explorer 9, as APIs [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D raw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) agora criarão um metarquivo contendo um único bitmap que representa o conteúdo da Web em vez de um metarquivo avançado contendo informações de texto e vetor. Essa alteração ocorreu devido à mudança da renderização GDI para a renderização D2D (Direct2D acelerada por hardware).

Essa alteração afeta aplicativos que usam essas APIs e dependem de informações de texto ou vetor no metadado.

## <a name="manifestation"></a>Manifestação

Dependendo do aplicativo afetado por essa alteração, os usuários podem ver um comportamento desfeito ou incorreto em seus aplicativos.

## <a name="mitigation"></a>Atenuação

Aplicativos que só precisam extrair informações de texto de um documento da Web (sem informações de posicionamento) podem usar a [propriedade innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) para extrair texto.

Os aplicativos que usam IViewObject::D raw podem usar a chave de controle de recurso [ \_ FEATURE IVIEWOBJECTDRAW \_ DMLT9 \_ WITH \_ GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) para reverter para a renderização GDI se o modo de documento:

-   É menor ou igual a 8
-   O FCK autoriza esse host a usar a GDI
-   E um DC de metadados é passado para a API

## <a name="resources"></a>Recursos

-   [IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))
-   [IViewObject::D raw](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   [Propriedade IHTMLElement::innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))
-   [Controles de recursos da Internet (ou seja, L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))

 

 