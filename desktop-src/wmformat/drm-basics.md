---
title: Noções básicas de DRM
description: Noções básicas de DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- SDK do Windows Media Format, noções básicas de DRM
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), sobre
- DRM (gerenciamento de direitos digitais), proteção de conteúdo
- DRM (gerenciamento de direitos digitais), protegendo o conteúdo
- DRM (gerenciamento de direitos digitais), conteúdo de empacotamento
- DRM (gerenciamento de direitos digitais), conteúdo de empacotamento
- DRM (gerenciamento de direitos digitais), lendo conteúdo protegido
- DRM (gerenciamento de direitos digitais), lendo conteúdo protegido
- protegendo o conteúdo
- empacotando conteúdo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364435"
---
# <a name="drm-basics"></a>Noções básicas de DRM

As tecnologias DRM do Windows Media são bem simples da perspectiva do Windows Media Format SDK. Os componentes do SDK podem ser usados para proteger o conteúdo e para reproduzir conteúdo protegido.

## <a name="protecting-content"></a>Protegendo conteúdo

Proteger o conteúdo (também chamado de conteúdo de empacotamento) envolve criptografar a seção de dados do arquivo e incluir algumas informações no cabeçalho do arquivo que permite que os jogadores descriptografem o conteúdo.

Para criptografar o conteúdo, você precisa de uma chave, que é um valor usado para propagar os algoritmos de criptografia. Uma chave é composta de duas partes: uma semente de chave (ou chave privada) e um identificador de chave (ou chave pública). A semente de chave é o valor secreto com o qual você codifica o conteúdo. O identificador de chave é um valor público que é incluído no cabeçalho de um arquivo protegido.

Quando um arquivo é protegido, ele não pode ser descriptografado sem uma licença. Uma licença inclui informações que especificam os termos de uso do conteúdo protegido. Os termos de uma licença são decididos pelo proprietário do conteúdo e podem ser personalizados para atender a uma variedade de necessidades. Parte do processo de empacotamento de um arquivo é incluir a URL de uma página da Web em que os usuários podem adquirir uma licença para acessar o conteúdo.

## <a name="reading-protected-content"></a>Lendo conteúdo protegido

Para ler o conteúdo protegido, uma licença para o conteúdo deve residir no computador cliente. Algumas restrições de licença são verificadas internamente pelos componentes DRM do SDK do Windows Media Format, enquanto outras devem ser impostas pelo seu aplicativo.

Você pode usar os objetos do Windows Media Format SDK para ajudar o usuário a adquirir licenças para conteúdo e executar outras tarefas administrativas, como atualizar componentes DRM e fazer backup de licenças.

> [!Note]  
> O DRM não é compatível com a versão baseada em x64 deste SDK.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Habilitando o suporte a DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




