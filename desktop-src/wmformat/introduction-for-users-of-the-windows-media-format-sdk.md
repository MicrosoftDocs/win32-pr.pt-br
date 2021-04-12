---
title: Introdução para usuários do Windows Media Format SDK
description: Introdução para usuários do Windows Media Format SDK
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
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
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364045"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a>Introdução para usuários do Windows Media Format SDK

Grande parte da funcionalidade fornecida pelas APIs estendidas do cliente DRM do Windows Media é a mesma que a funcionalidade fornecida pelos objetos do SDK do Windows Media Format. O Windows Media Format SDK fornece aos desenvolvedores os objetos necessários para criar, acessar e manipular arquivos de mídia que usam a estrutura de arquivos ASF (Advanced Systems Format). Como o DRM do Windows Media destina-se a proteger arquivos ASF, a funcionalidade DRM do lado do cliente foi incluída no Windows Media Format SDK.

As APIs estendidas do cliente DRM do Windows Media estão sendo lançadas em conjunto com a plataforma de mídia digital de última geração da Microsoft, o SDK do Microsoft Media Foundation. Media Foundation incluirá a funcionalidade do ASF que sobrepõe alguns dos recursos do SDK do Windows Media Format. Como agora há dois SDKs da Microsoft que manipulam arquivos ASF, a funcionalidade DRM do lado do cliente está sendo separada do SDK do Windows Media Format para as APIs estendidas do cliente DRM do Windows Media. Essas APIs podem ser acessadas por usuários do Windows Media Format SDK e do SDK do Media Foundation. No momento, essas APIs são incluídas como parte do pacote de instalação do Windows Media Format SDK e são documentadas como parte do Windows Media Format SDK. No entanto, as APIs estendidas do cliente Windows Media DRM são implementadas em sua própria biblioteca e têm seu próprio arquivo de cabeçalho. Depois de instalar o SDK do Windows Media Format, essas APIs podem ser usadas por conta própria, sem incluir cabeçalhos ou bibliotecas do Windows Media Format SDK em seu aplicativo.

Se você desenvolver aplicativos que usam o SDK do Windows Media Format, deverá decidir se usará a funcionalidade DRM fornecida pelo SDK ou usará as APIs estendidas do cliente DRM do Windows Media. Embora muitos dos recursos desses dois SDKs sejam muito semelhantes, as APIs estendidas do cliente Windows Media DRM oferecem os seguintes recursos não disponíveis para os usuários das rotinas de DRM mais antigas:

-   Capacidade de importar conteúdo protegido por um sistema de gerenciamento de direitos de terceiros.
-   Capacidade de exportar conteúdo protegido pelo Windows Media DRM para um sistema de gerenciamento de direitos de terceiros.
-   Enumeração direta de licenças no repositório de licenças.
-   Direitos simples e agregados consultam com base na ID da chave (sem necessidade de carregar o arquivo de mídia).
-   Capacidade de renovar componentes revogados usando a interface de Media Foundation padrão, **IMFContentEnabler**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as APIs estendidas do cliente DRM do Windows Media**](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




