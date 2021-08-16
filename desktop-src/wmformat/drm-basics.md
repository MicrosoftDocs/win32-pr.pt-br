---
title: Noções básicas sobre DRM
description: Noções básicas sobre DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows SDK de formato de mídia, noções básicas de DRM
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais),sobre
- DRM (gerenciamento de direitos digitais), protegendo conteúdo
- DRM (gerenciamento de direitos digitais), protegendo o conteúdo
- DRM (gerenciamento de direitos digitais), empacotamento de conteúdo
- DRM (gerenciamento de direitos digitais), empacotamento de conteúdo
- DRM (gerenciamento de direitos digitais), leitura de conteúdo protegido
- DRM (gerenciamento de direitos digitais), leitura de conteúdo protegido
- protegendo o conteúdo
- empacotando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ef4439308868b0d77db1e9cefac7381fb8fd9ee78be50cccbf2a8dc26e4176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086136"
---
# <a name="drm-basics"></a>Noções básicas sobre DRM

As Windows drm de mídia são bastante simples da perspectiva do SDK Windows Formato de Mídia. Os componentes do SDK podem ser usados para proteger o conteúdo e reproduzir conteúdo protegido.

## <a name="protecting-content"></a>Protegendo conteúdo

Proteger conteúdo (também chamado de conteúdo de empacotamento) envolve criptografar a seção de dados do arquivo e incluir algumas informações no título do arquivo que permite aos jogadores descriptografar o conteúdo.

Para criptografar o conteúdo, você precisa de uma chave, que é um valor usado para a semente dos algoritmos de criptografia. Uma chave é feita de duas partes: uma semente de chave (ou chave privada) e um identificador de chave (ou chave pública). A semente da chave é o valor secreto com o qual você codifica o conteúdo. O identificador de chave é um valor público incluído no header de um arquivo protegido.

Quando um arquivo é protegido, ele não pode ser descriptografado sem uma licença. Uma licença inclui informações que especificam os termos de uso para o conteúdo protegido. Os termos de uma licença são decididos pelo proprietário do conteúdo e podem ser personalizados para atender a uma variedade de necessidades. Parte do processo de empacotamento de um arquivo é incluir a URL de uma página da Web em que os usuários podem adquirir uma licença para acessar o conteúdo.

## <a name="reading-protected-content"></a>Lendo conteúdo protegido

Para ler o conteúdo protegido, uma licença para o conteúdo deve residir no computador cliente. Algumas restrições de licença são verificadas internamente pelos componentes drm do SDK Windows Formato de Mídia, enquanto outras devem ser impostas pelo seu aplicativo.

Você pode usar os objetos do SDK de Formato de Mídia do Windows para ajudar o usuário a adquirir licenças para conteúdo e executar outras tarefas administrativas, como atualizar componentes drm e fazer o back-up de licenças.

> [!Note]  
> O DRM não é suportado pela versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




