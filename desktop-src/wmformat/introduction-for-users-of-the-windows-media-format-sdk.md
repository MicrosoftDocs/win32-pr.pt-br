---
title: introdução para usuários do SDK do formato de mídia do Windows
description: introdução para usuários do SDK do formato de mídia do Windows
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- Windows SDK do formato de mídia, APIs estendidas do cliente DRM
- Windows SDK do formato de mídia, APIs estendidas do cliente
- Windows SDK do formato de mídia, APIs estendidas
- Windows SDK do formato de mídia, APIs
- Windows SDK do formato de mídia, DRM (gerenciamento de direitos digitais)
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- APIs estendidas do cliente DRM, sobre
- APIs estendidas do cliente, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb1994e5e4960613e992f198833f2fb2e3ff2a21181e98bae5d6823fbb31a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119392556"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>introdução para usuários do SDK do formato de mídia do Windows

grande parte da funcionalidade fornecida pelas APIs estendidas do cliente DRM Windows mídia é igual à funcionalidade fornecida pelos objetos do SDK do formato de mídia do Windows. o SDK do formato de mídia Windows fornece aos desenvolvedores os objetos necessários para criar, acessar e manipular arquivos de mídia que usam a estrutura de arquivo ASF (Advanced Systems Format). como o Windows media drm se destina a proteger arquivos ASF, a funcionalidade drm do lado do cliente foi incluída no SDK do formato de mídia do Windows.

as APIs estendidas do cliente de DRM de mídia Windows estão sendo lançadas em conjunto com a plataforma de mídia digital de última geração da Microsoft, o SDK do Microsoft Media Foundation. Media Foundation incluirá a funcionalidade do ASF que sobrepõe alguns dos recursos do SDK do formato de mídia do Windows. como agora há dois SDKs da Microsoft que manipulam arquivos ASF, a funcionalidade DRM do lado do cliente está sendo separada do SDK Windows media Format para as APIs estendidas do cliente drm Windows media. essas APIs podem ser acessadas por usuários do sdk do formato de mídia Windows e do sdk do Media Foundation. no momento, essas APIs são incluídas como parte do pacote de instalação Windows media format sdk e são documentadas como parte do SDK do formato de mídia do Windows. no entanto, as APIs estendidas do cliente DRM de mídia Windows são implementadas em sua própria biblioteca e têm seu próprio arquivo de cabeçalho. depois de instalar o SDK do formato de mídia do Windows, essas APIs podem ser usadas por conta própria, sem incluir nenhum cabeçalho ou biblioteca do SDK do formato de mídia Windows em seu aplicativo.

se você desenvolver aplicativos que usam o sdk do formato de mídia Windows, deverá decidir se usará a funcionalidade DRM que o SDK fornece ou usará as APIs estendidas do cliente do drm de mídia Windows. embora muitos dos recursos desses dois SDKs sejam muito semelhantes, as APIs estendidas do cliente DRM Windows mídia oferecem os seguintes recursos não disponíveis para os usuários das rotinas de DRM mais antigas:

-   Capacidade de importar conteúdo protegido por um sistema de gerenciamento de direitos de terceiros.
-   capacidade de exportar conteúdo protegido pelo Windows DRM de mídia para um sistema de gerenciamento de direitos de terceiros.
-   Enumeração direta de licenças no repositório de licenças.
-   Direitos simples e agregados consultam com base na ID da chave (sem necessidade de carregar o arquivo de mídia).
-   Capacidade de renovar componentes revogados usando a interface de Media Foundation padrão, **IMFContentEnabler**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**sobre as APIs estendidas do cliente de DRM de mídia Windows**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




