---
title: Serviços de autorização
description: Um serviço de autorização é o método que o SSP usa para autorizar o acesso a um procedimento remoto. Os SSPs podem fornecer mais de um serviço de autorização. No entanto, normalmente, eles selecionam um como padrão.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005828"
---
# <a name="authorization-services"></a>Serviços de autorização

Um serviço de autorização é o método que o SSP usa para autorizar o acesso a um procedimento remoto. Os SSPs podem fornecer mais de um serviço de autorização. No entanto, normalmente, eles selecionam um como padrão.

Seu aplicativo pode usar o método de autorização padrão para o SSP atual ou pode especificar um. No momento, o Microsoft RPC dá suporte a dois métodos de autorização. Uma é para o servidor fornecer autorização com base no nome do programa cliente. O outro é que o servidor Compare as credenciais de autenticação do cliente com a ACL (lista de controle de acesso) do servidor.

Para obter uma lista de serviços de autorização, consulte [constantes de serviço de autorização](authorization-service-constants.md).

> [!Note]  
> É recomendável que os desenvolvedores usem RPC \_ C \_ AUTHZ \_ None.

 

 

 




