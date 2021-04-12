---
title: Adquirindo licenças
description: Adquirindo licenças
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- SDK do Windows Media Format, APIs estendidas do cliente DRM
- SDK do Windows Media Format, APIs estendidas do cliente
- SDK do Windows Media Format, APIs estendidas
- SDK do Windows Media Format, APIs
- SDK do Windows Media Format, DRM (gerenciamento de direitos digitais)
- Windows Media Format SDK, adquirindo licenças
- SDK do Windows Media Format, licenças
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas do cliente
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs estendidas
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), APIs
- DRM (gerenciamento de direitos digitais), aquisição de licenças
- DRM (gerenciamento de direitos digitais), aquisição de licenças
- DRM (gerenciamento de direitos digitais), licenças
- DRM (gerenciamento de direitos digitais), licenças
- APIs estendidas do cliente DRM, adquirindo licenças
- APIs estendidas do cliente, adquirindo licenças
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363689"
---
# <a name="acquiring-licenses"></a>Adquirindo licenças

Um cenário comum para adquirir licenças é quando um usuário tem um arquivo de mídia do Windows protegido e tenta acessar o conteúdo pela primeira vez. Como as APIs estendidas do cliente DRM do Windows Media são separadas das rotinas de manipulação de arquivos ASF, o cenário de aquisição de licença básica, embora com suporte, requer mais chamadas à API do que usar o SDK do Windows Media Format e o SDK do Media Foundation.

Esta seção descreve como usar as APIs estendidas do cliente DRM do Windows Media para adquirir licenças armazenadas no repositório de licenças local em um computador cliente. Ele contém os tópicos a seguir.



| Tópico                                                                | Descrição                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Aquisição de licença silenciosa](silent-license-acquisition.md)         | Descreve como adquirir licenças sem intervenção do usuário.                                                                               |
| [Aquisição de licença não silenciosa](non-silent-license-acquisition.md) | Descreve como adquirir licenças quando a intervenção do usuário (como pagar pelo conteúdo) é necessária.                                     |
| [Pré-entrega de licença](license-pre-delivery.md)                     | Descreve como efetuar pull de licenças de um servidor de licença para um computador cliente.                                                                 |
| [Criando licenças localmente](creating-licenses-locally.md)           | Descreve como criar suas próprias licenças sem baixá-las de um servidor de licenças e como armazená-las no repositório de licenças local. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação**](drm-programming-guide.md)
</dt> </dl>

 

 




