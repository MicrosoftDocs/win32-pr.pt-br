---
description: Uma biblioteca abrangente é uma biblioteca de vínculo estático única que exporta um subconjunto de APIs do Win32. por exemplo, uma lib abrangente denominada OneCore. lib fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10.
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

Uma *biblioteca abrangente* é uma biblioteca de vínculo estático única que exporta um subconjunto de APIs do Win32. por exemplo, uma biblioteca abrangente chamada **OneCore. lib** fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10.

As APIs em uma biblioteca abrangente podem ser implementadas em uma variedade de módulos (seja um [conjunto de API](windows-apisets.md) ou uma dll), mas a biblioteca abrangente abstrai esses detalhes, tornando seu aplicativo mais portátil entre as versões do sistema operacional. Basta vincular seu aplicativo de área de trabalho ou driver à biblioteca de abrangência que contém o conjunto de APIs em que você está interessado, e isso é tudo o que você precisa fazer. 

| Biblioteca | Descrição |
|------------------------|-------------------------|
| OneCore. lib | essa biblioteca fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10. vincule seu aplicativo de área de trabalho ou driver a OneCore. lib (e nenhuma outra biblioteca) para acessar essas APIs. se você vincular seu aplicativo ou driver a OneCore. lib e chamar apenas as APIs do Win32 nessa biblioteca, o aplicativo ou o driver será carregado com êxito em todos os dispositivos Windows 10.         |
| OneCore_apiset. lib | essa biblioteca fornece a mesma cobertura que OneCore. lib, mas usa o [encaminhamento direto do conjunto de API](api-set-loader-operation.md#direct-forwarding). observe que o uso dessa biblioteca será compatível apenas com a versão de Windows 10 conforme especificado pelo SDK versão de destino, ou maior.  |
| OneCoreUap. lib | essa biblioteca fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10 que dão suporte ao Windows Runtime (WinRT). Vincule seu aplicativo de área de trabalho ou driver a OneCoreUap. lib (e nenhuma outra biblioteca) para acessar essas APIs. se você vincular seu aplicativo ou driver a OneCoreUap. lib e chamar apenas as APIs do Win32 nessa biblioteca, o aplicativo ou o driver será carregado com êxito em todos os dispositivos Windows 10 que dão suporte a UWP. |
| OneCoreUAP_apiset. lib | Essa biblioteca fornece a mesma cobertura que OneCoreUAP. lib, mas usa a técnica de [encaminhamento direto do conjunto de API](api-set-loader-operation.md#direct-forwarding) . observe que o uso dessa biblioteca será compatível apenas com a versão Windows 10 conforme especificado pelo SDK no qual você está direcionando ou mais.  |
