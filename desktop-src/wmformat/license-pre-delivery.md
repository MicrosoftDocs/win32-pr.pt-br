---
title: Pré-entrega de licença
description: Pré-entrega de licença
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- SDK do Windows Media Format, pré-entrega de licenças
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), pré-entrega de licenças
- DRM (gerenciamento de direitos digitais), pré-entrega de licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, pré-entrega de licenças
- APIs estendidas do cliente, pré-entrega de licenças
- pré-entrega de licenças
- licenças, pré-entrega de licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105755907"
---
# <a name="license-pre-delivery"></a>Pré-entrega de licença

A pré-entrega de licença é o processo usado para efetuar pull de licenças para um computador cliente preemptivo. Um cenário comum para usar a pré-entrega é quando um usuário assina um serviço de música. Sem o fornecimento de licenças antes que elas sejam necessárias, o usuário precisa aguardar a aquisição de licença para cada nova música.

Como a pré-entrega não é feita como uma resposta à tentativa de acesso, ela normalmente é executada apenas pelo proprietário do conteúdo. Ou seja, você só pode entregar licenças previamente para o conteúdo que você controla. O processo de pré-entrega é uma coordenação entre um componente de cliente e um servidor de licença criado usando os objetos do SDK do Windows Media Digital Rights Management.

A pré-entrega de licença é semelhante à [aquisição de licença não silenciosa](non-silent-license-acquisition.md). Siga as mesmas etapas, exceto que você não tem um cabeçalho DRM para passar para [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md). O método gerará um desafio que não é específico de conteúdo que você pode enviar para o servidor de licença.

Como alternativa, você pode usar o [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) para entregar licenças previamente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Adquirindo licenças**](acquiring-licenses.md)
</dt> <dt>

[**Usando o modelo de evento Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 