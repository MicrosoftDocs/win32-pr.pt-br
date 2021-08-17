---
description: Uma biblioteca umbrella é uma única biblioteca de vínculo estático que exporta um subconjunto de APIs do Win32. Por exemplo, uma biblioteca umbrella chamada OneCore.lib fornece as exportações para o subconjunto de APIs Win32 que são comuns a todos os Windows 10 dispositivos.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Bibliotecas de abrangência do Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 8714f7054e11e488c61a01fd3f010faaae8c1403efdce6727e88dc26a9d5f133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737613"
---
# <a name="windows-umbrella-libraries"></a>Bibliotecas de abrangência do Windows

Uma *biblioteca umbrella* é uma única biblioteca de vínculo estático que exporta um subconjunto de APIs do Win32. Por exemplo, uma biblioteca umbrella chamada **OneCore.lib** fornece as exportações para o subconjunto de APIs Win32 que são comuns a todos os Windows 10 dispositivos.

As APIs em uma biblioteca umbrella podem ser implementadas em uma variedade de módulos (seja um conjunto de [API](windows-apisets.md) ou uma DLL), mas a biblioteca umbrella abstrai esse detalhe de você, tornando seu aplicativo mais portátil entre as versões do sistema operacional. Basta vincular seu aplicativo ou driver da área de trabalho à biblioteca umbrella que contém o conjunto de APIs em que você está interessado e isso é tudo o que você precisa fazer. 

| Biblioteca | Descrição |
|------------------------|-------------------------|
| OneCore.lib | Essa biblioteca fornece as exportações para o subconjunto de APIs Win32 que são comuns a todos os Windows 10 dispositivos. Vincule seu aplicativo ou driver da área de trabalho com OneCore.lib (e nenhuma outra biblioteca) para acessar essas APIs. Se você vincular seu aplicativo ou driver a OneCore.lib e chamar apenas APIs win32 nessa biblioteca, seu aplicativo ou driver será carregado com êxito em todos os Windows 10 dispositivos.         |
| OneCore_apiset.lib | Essa biblioteca fornece a mesma cobertura que OneCore.lib, mas usa o encaminhamento direto [do conjunto de API.](api-set-loader-operation.md#direct-forwarding) Observe que o uso dessa biblioteca será compatível apenas com a versão Windows 10 conforme especificado pela vértice do SDK que você está direcionando ou superior.  |
| OneCoreUap.lib | Essa biblioteca fornece as exportações para o subconjunto de APIs win32 que são comuns a todos os Windows 10 que suportam o WinRT (runtime Windows). Vincule seu aplicativo ou driver da área de trabalho com OneCoreUap.lib (e nenhuma outra biblioteca) para acessar essas APIs. Se você vincular seu aplicativo ou driver a OneCoreUap.lib e chamar apenas APIs win32 nessa biblioteca, seu aplicativo ou driver será carregado com êxito em todos os dispositivos Windows 10 que suportam a UWP. |
| OneCoreUAP_apiset.lib | Essa biblioteca fornece a mesma cobertura que OneCoreUAP.lib, mas usa a técnica de encaminhamento direto do conjunto [de API.](api-set-loader-operation.md#direct-forwarding) Observe que o uso dessa biblioteca será compatível apenas com Windows 10 versão do Windows 10 conforme especificado pelo SDK que você está direcionando ou superior.  |
