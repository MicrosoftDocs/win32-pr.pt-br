---
title: Executando individualização de DRM
description: Executando individualização de DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- SDK do Windows Media Format, individualização de DRM
- SDK do Windows Media Format, individualização
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), individualização
- DRM (gerenciamento de direitos digitais), individualização
- DRM (gerenciamento de direitos digitais), individualização de DRM
- DRM (gerenciamento de direitos digitais), individualização de DRM
- APIs estendidas do cliente DRM, individualização
- APIs estendidas do cliente, individualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292617"
---
# <a name="performing-drm-individualization"></a>Executando individualização de DRM

A individualização é o processo de atualizar o componente DRM no computador cliente, criptografá-lo e torná-lo exclusivo. Quando um computador é individualizado, o componente DRM é vinculado ao computador e não será capaz de decodificar o conteúdo em nenhum outro computador. As APIs estendidas do cliente Windows Media DRM oferecem suporte para individualizar o componente DRM em computadores cliente.

A individualização é executada chamando o método [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) . Você pode chamar **PerformSecurityUpdate** para que ela seja individualizada somente se a versão no servidor for mais recente do que a instalada no computador cliente ou se você puder forçar a individualização sem considerar as versões de segurança relativas. O sinalizador para a individualização conforme necessário é a \_ segurança do WMDRM \_ Execute \_ indiv. O sinalizador para individualização forçada é a segurança do WMDRM \_ \_ Execute \_ Force \_ indiv.

**PerformSecurityUpdate** é uma chamada assíncrona. Ele retornará rapidamente e, em seguida, gerará eventos para fornecer informações de status sobre o processo de individualização. A maioria dos eventos gerados será **MEWMDRMIndividualizationProgress** eventos e cada um terá uma interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associada. Para obter a interface de status, você deve chamar **IMFMediaEvent:: GetValue** para recuperar um ponteiro **IUnknown** que esteja no mesmo objeto e, em seguida, consultá-lo para **IWMDRMIndividualizationStatus**.

Você pode obter dados para uma estrutura de [**\_ \_ status de individualização do WM**](drmwm-individualize-status.md) chamando [**IWMDRMIndividualizeStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md). Cada evento gerado tem seu próprio objeto com status, portanto, você deve passar pelo processo de obter o valor do evento e consultar a interface de status a cada vez.

Dependendo do tamanho do download, pode haver dezenas ou centenas de eventos **MEWMDRMIndividualizationProgress** . Quando o processo de individualização é concluído, um evento **MEWMDRMIndividualizationCompleted** é gerado.

Quando a individualização for concluída, os únicos objetos existentes que refletirão o novo estado individual serão aqueles que herdam de [**IWMDRMSecurity**](iwmdrmsecurity.md). Todos os outros objetos existentes não serão atualizados. Você deve liberar e recriar outros objetos para que eles reflitam o novo estado individual.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplo de individualização de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> <dt>

[**Usando o modelo de evento Media Foundation**](using-the-media-foundation-model.md)
</dt> <dt>

[Práticas recomendadas de individualização do Windows Media DRM](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




