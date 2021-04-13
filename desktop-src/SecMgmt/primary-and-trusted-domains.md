---
description: Os termos a seguir descrevem os domínios que existem em sistemas remotos.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Domínios primários e confiáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501544"
---
# <a name="primary-and-trusted-domains"></a>Domínios primários e confiáveis

Os termos a seguir descrevem os domínios que existem em sistemas remotos.

-   [Domínio Primário](#primary-domain)
-   [Domínio confiável](#primary-and-trusted-domains)

## <a name="primary-domain"></a>Domínio Primário

Um domínio primário é o domínio que é responsável por estabelecer relações de confiança adicionais e executar a autenticação (ou para passar uma solicitação de autenticação para um domínio confiável apropriado). Os controladores de domínio no domínio primário tratam ou passam por solicitações de autenticação originadas na estação de trabalho.

Quando ocorre o logon, a LSA verifica os domínios internos e de conta para obter informações de autenticação. Se a conta que está sendo conectada não estiver em nenhum desses domínios, a solicitação de logon será enviada para o domínio primário do sistema.

## <a name="trusted-domain"></a>Domínio confiável

Um domínio confiável é um domínio no qual o sistema local confia para autenticar usuários. Em outras palavras, se um usuário ou aplicativo for autenticado por um domínio confiável, essa autenticação será aceita por todos os domínios que confiam no domínio de autenticação.

Cada domínio subordinado tem automaticamente uma relação de confiança bidirecional com o domínio principal. Por padrão, essa confiança é transitiva, o que significa que, se um sistema confiar no domínio A, ele também confiará em todos os domínios em que o domínio confia. Também há suporte para relações de confiança unidirecionais em sistemas operacionais anteriores ao Windows 2000, que não dão suporte a relações de confiança bidirecionais transitivas.

A [*autoridade de segurança local*](/windows/desktop/SecGloss/l-gly) (LSA) tem um tipo de objeto, [**TrustedDomain**](the-trusteddomain-object-type.md), que é usado para armazenar informações sobre relações de confiança, incluindo o nome e o [*identificador de segurança*](/windows/desktop/SecGloss/s-gly) (SID) do domínio confiável, a conta no domínio a ser usada para solicitações de autenticação, solicitações de conversão de nome e Sid e os nomes de controladores de domínio no domínio confiável.

Em controladores de domínio, a LSA cria uma instância de um objeto [**TrustedDomain**](the-trusteddomain-object-type.md) para cada domínio confiável pelo sistema local.

Por exemplo, se uma estação de trabalho do Windows XP confiar em um controlador de domínio do Windows 2000 que, por sua vez, confiar em quatro outros sistemas, a estação de trabalho, conectada usando confiança transitiva, terá cinco objetos [**TrustedDomain**](the-trusteddomain-object-type.md) em seu sistema local.

 

 
