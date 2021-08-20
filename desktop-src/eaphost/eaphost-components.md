---
title: Componentes do EAPHost
description: Saiba mais sobre os três componentes da autenticação do EAPHost. Exiba recursos adicionais disponíveis para usar a autenticação EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa86f09473b14df6dbcc8bbc667dc4a1cc1badf9e0b6dd67ac95f8d11f2bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086410"
---
# <a name="components-of-eaphost"></a>Componentes do EAPHost

Este tópico descreve os três componentes da autenticação do EAPHost.

## <a name="eaphost-components"></a>Componentes do EAPHost

A autenticação EAPHost tem os três componentes a seguir.

-   O suplicante, que faz as solicitações de autenticação.
-   Os métodos EAP de par (ou cliente), que implementam os métodos de EAP específicos e gerenciam a sessão de autenticação no lado do cliente.
-   Os métodos EAP do autenticador (ou servidor), que implementam o lado do servidor do protocolo EAP.

As APIs suplicantes são chamadas diretamente de um aplicativo que deseja autenticar via EAPHost. O método par e as APIs do método autenticador, no entanto, são protótipos de função que devem ser implementados para um tipo de método de autenticação EAP específico, como o protocolo de autenticação handshake de desafio da Microsoft versão 2,0 (MS-CHAPv2).

Se você estiver criando um aplicativo que usará o EAPHost para autenticação, consulte a referência da [API suplicante do EAPHost](eap-host-supplicant-api-reference.md).

se você estiver criando um novo método de autenticação EAP a ser gerenciado pelo EAPHost, consulte a referência da [API do método par do eaphost](eap-host-peer-method-api-reference.md) e as [APIs do método de Authenticator do eaphost](eaphost-authenticator-method-apis.md). Observe que você estará criando implementações dessas APIs expostas em uma nova DLL que o EAPHost carrega, em vez de chamá-las diretamente.

 

 




