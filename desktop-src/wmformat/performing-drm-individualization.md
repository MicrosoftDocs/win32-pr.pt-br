---
title: Executando a individualização de DRM
description: Executando a individualização de DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows SDK de Formato de Mídia, APIs Estendidas do Cliente DRM
- Windows SDK de formato de mídia, APIs estendidas do cliente
- Windows SDK de formato de mídia, APIs estendidas
- Windows SDK de formato de mídia, APIs
- Windows SDK de Formato de Mídia, DRM (gerenciamento de direitos digitais)
- Windows SDK de formato de mídia, individualização de DRM
- Windows SDK de formato de mídia, individualização
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
ms.openlocfilehash: 72c46d2cd6fccd2c6c1a8898a2d0215b6bc62a3655b12412192d1809021747ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027384"
---
# <a name="performing-drm-individualization"></a>Executando a individualização de DRM

A individualização é o processo de atualizar o componente DRM no computador cliente, criptografá-lo e tornando-o exclusivo. Quando um computador é individualizado, o componente DRM é vinculado ao computador e não poderá decodificar o conteúdo em nenhum outro computador. As APIs estendidas do cliente drm de Windows mídia oferecem suporte para individualizar o componente DRM em computadores cliente.

A individualização é executada chamando o [**método IWMDRMSecurity::P erformSecurityUpdate.**](iwmdrmsecurity-performsecurityupdate.md) Você pode chamar **PerformSecurityUpdate** para que ele seja individualizado somente se a versão no servidor for mais recente do que a instalada no computador cliente ou se você puder forçar a individualização sem considerar as versões de segurança relativas. O sinalizador para a individualização conforme necessário é WMDRM \_ SECURITY \_ PERFORM \_ INDIV. O sinalizador para individualização forçada é WMDRM \_ SECURITY \_ PERFORM FORCE \_ \_ INDIV.

**PerformSecurityUpdate** é uma chamada assíncrona. Ele retornará rapidamente e, em seguida, gerará eventos para fornecer informações de status sobre o processo de individualização. A maioria dos eventos gerados serão **eventos MEWMDRMIndividualizationProgress** e cada um deles tem uma interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associada. Para obter a interface de status, você deve chamar **IMFMediaEvent::GetValue** para recuperar um ponteiro **IUnknown** que está no mesmo objeto e, em seguida, consulta-lo para **IWMDRMIndividualizationStatus**.

Você pode obter dados para uma estrutura [**WM \_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md) chamando [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md). Cada evento gerado tem seu próprio objeto com status, portanto, você deve passar pelo processo de obter o valor do evento e consultar a interface de status sempre.

Dependendo do tamanho do download, pode haver dezenas ou centenas de eventos **MEWMDRMIndividualizationProgress.** Quando o processo de individualização é concluído, **um evento MEWMDRMIndividualizationCompleted** é gerado.

Quando a individualização é concluída, os únicos objetos existentes que refletirão o novo estado individualizado são aqueles que herdam [**de IWMDRMSecurity.**](iwmdrmsecurity.md) Todos os outros objetos existentes não serão atualizados. Você deve liberar e re-criar quaisquer outros objetos para que eles reflitam o novo estado individualizado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Exemplo de individualização de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> <dt>

[**Usando o modelo Media Foundation evento**](using-the-media-foundation-model.md)
</dt> <dt>

[Windows Práticas recomendadas de individualização de DRM de mídia](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




