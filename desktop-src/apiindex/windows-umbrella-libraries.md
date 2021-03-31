---
description: Uma biblioteca abrangente é uma biblioteca de vínculo estático única que exporta um subconjunto de APIs do Win32. Por exemplo, uma lib abrangente chamada OneCore. lib fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10.
ms.assetid: A323B5D1-3235-4BBA-96BF-A7DFEBB85C89
title: Bibliotecas de abrangência do Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 86a8f9b8f3bef5081bd7e0e64300b9295fd85401
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/24/2020
ms.locfileid: "103642970"
---
# <a name="windows-umbrella-libraries"></a>Bibliotecas de abrangência do Windows

Uma *biblioteca abrangente* é uma biblioteca de vínculo estático única que exporta um subconjunto de APIs do Win32. Por exemplo, uma biblioteca abrangente chamada **OneCore. lib** fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10.

As APIs em uma biblioteca abrangente podem ser implementadas em uma variedade de módulos (seja um [conjunto de API](windows-apisets.md) ou uma dll), mas a biblioteca abrangente abstrai esses detalhes, tornando seu aplicativo mais portátil entre as versões do sistema operacional. Basta vincular seu aplicativo de área de trabalho ou driver à biblioteca de abrangência que contém o conjunto de APIs em que você está interessado, e isso é tudo o que você precisa fazer. 

| Biblioteca | Descrição |
|------------------------|-------------------------|
| OneCore. lib | Essa biblioteca fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10. Vincule seu aplicativo de área de trabalho ou driver a OneCore. lib (e nenhuma outra biblioteca) para acessar essas APIs. Se você vincular seu aplicativo ou driver a OneCore. lib e chamar apenas as APIs do Win32 nessa biblioteca, o aplicativo ou o driver será carregado com êxito em todos os dispositivos com Windows 10.         |
| OneCore_apiset. lib | Essa biblioteca fornece a mesma cobertura que OneCore. lib, mas usa o [encaminhamento direto do conjunto de API](api-set-loader-operation.md#direct-forwarding). Observe que o uso dessa biblioteca será compatível apenas com a versão do Windows 10, conforme especificado pelo SDK versão de destino, ou maior.  |
| OneCoreUap. lib | Essa biblioteca fornece as exportações para o subconjunto de APIs do Win32 que são comuns a todos os dispositivos Windows 10 que dão suporte ao Windows Runtime (WinRT). Vincule seu aplicativo de área de trabalho ou driver a OneCoreUap. lib (e nenhuma outra biblioteca) para acessar essas APIs. Se você vincular seu aplicativo ou driver a OneCoreUap. lib e chamar apenas as APIs do Win32 nessa biblioteca, o aplicativo ou o driver será carregado com êxito em todos os dispositivos com Windows 10 que dão suporte a UWP. |
| OneCoreUAP_apiset. lib | Essa biblioteca fornece a mesma cobertura que OneCoreUAP. lib, mas usa a técnica de [encaminhamento direto do conjunto de API](api-set-loader-operation.md#direct-forwarding) . Observe que o uso dessa biblioteca será compatível apenas com a versão do Windows 10, conforme especificado pelo SDK no qual você está direcionando ou mais.  |
