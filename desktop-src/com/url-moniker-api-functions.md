---
title: Funções de Moniker de URL
description: Funções de Moniker de URL
ms.assetid: 773743d3-9434-4ec9-b85c-9b971e37682f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd4dc19d47a933e9f93516630b25fdab2f64b21cb3755ac9fd5bbdfa7edaba51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992036"
---
# <a name="url-moniker-functions"></a>Funções de Moniker de URL

As funções de moniker de URL isolam os desenvolvedores das complexidades de criação, gerenciamento e uso de monikers de URL. Essas funções são as seguinte:

-   [**CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85))
-   [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85))
-   [**RegisterMediaTypes**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85))
-   [**CreateFormatEnumerator**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator)
-   [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))
-   [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85))
-   [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85))
-   [**FindMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85))
-   [**GetClassFileOrMime**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85))
-   [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85))

Sua familiaridade com essas funções pode ser a seguinte:

-   Familiarizar-se [**com CreateURLMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775102(v=vs.85)) e [**IsValidURL**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775112(v=vs.85)) se você estiver usando monikers de URL em aplicativos autônomos. Se você estiver criando um controle ActiveX, deverá usar [**IBindHost::CreateMoniker em**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775075(v=vs.85)) vez de **CreateURLMoniker**.
-   Familiarizar-se com [**RegisterMediaTypes,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775118(v=vs.85)) [**CreateFormatEnumerator,**](/windows/desktop/api/Urlmon/nf-urlmon-createformatenumerator) [**RegisterFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775116(v=vs.85))e [**RevokeFormatEnumerator**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775121(v=vs.85)) se você estiver executando qualquer negociação MIME com monikers de URL.
-   Familiarizar-se com [**RegisterMediaTypeClass**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775117(v=vs.85)), [**FindMediaTypeClass,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775106(v=vs.85)) [**GetClassFileOrMime e**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775108(v=vs.85)) [**UrlMkSetSessionOption**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775125(v=vs.85)) somente se você tiver uma experiência significativa com monikers de URL e com COM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[URL Monikers](url-monikers.md)
</dt> </dl>

 

 