---
title: Revogação de licença (Microsoft Windows Cliente DRM de Mídia)
description: Revogação de licença (Microsoft Windows Cliente DRM de Mídia)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows SDK de Formato de Mídia, licenças
- Windows SDK de Formato de Mídia, revogação de licença
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), revogação de licença
- DRM (gerenciamento de direitos digitais), revogação de licença
- APIs estendidas do cliente DRM, licenças
- APIs estendidas do cliente, licenças
- APIs estendidas do cliente DRM, revogação de licença
- APIs estendidas do cliente, revogação de licença
- licenças, revogação
- revogação de licença, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3cd295ddc1aec40c04f5284d791d7482854208a17875bdd3ed60d998f4ccf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027833"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Revogação de licença (Microsoft Windows Cliente DRM de Mídia)

A revogação de licença refere-se à remoção de licenças de um armazenamento de licenças local. Um cenário comum para revogação de licença ocorre quando um provedor de serviços, como um serviço de assinatura de música, deve desativar o serviço no computador de um usuário.

O processo de revogação de licença é iniciado por um serviço fornecido pelo emissor da licença. Seu aplicativo pode hospedar esse serviço ou pode ser um aplicativo Web. Em ambos os casos, seu aplicativo deve ser capaz de receber um desafio de licença criado pelo serviço.

Para remover licenças do armazenamento de licenças, faça o seguinte:

1.  Ao receber um desafio de licença do emissor da licença, crie um desafio de revogação usando o método [**IWMDRMLicenseManagement::CreateLicenseRevocationChallenge.**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) Esse método alocará um buffer que contém dados de desafio de revogação, que são passados para seu aplicativo por meio do *parâmetro ppbChallengeOutput.*
2.  Envie o desafio de revogação de licença para um serviço de revogação de licença. O servidor gerará um BLOB de revogação de licença (LRB) em resposta.
3.  Remova a licença do armazenamento local usando o método [**IWMDRMLicenseManagement::P rocessLicenseRevocationResponse,**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) passando o LRB retornado pelo servidor de licença.
4.  Desaloque o buffer alocado por **CreateLicenseRevocationChallenge** usando a **função CoTaskMemFree.**

Para obter mais informações sobre como a revogação de licença funciona ou sobre como escrever um serviço de revogação, consulte Implementando a [revogação de licença.](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> <dt>

[**Armazenamento de licenças local**](local-license-store.md)
</dt> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> </dl>

 

 