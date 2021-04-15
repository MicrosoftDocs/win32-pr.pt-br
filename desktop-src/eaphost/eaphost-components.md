---
title: Componentes do EAPHost
description: Saiba mais sobre os três componentes da autenticação do EAPHost. Exiba recursos adicionais disponíveis para usar a autenticação EAPHost.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104454351"
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

Se você estiver criando um novo método de autenticação EAP a ser gerenciado pelo EAPHost, consulte a referência da [API do método par do EAPHost](eap-host-peer-method-api-reference.md) e as [APIs do método de autenticador EAPHost](eaphost-authenticator-method-apis.md). Observe que você estará criando implementações dessas APIs expostas em uma nova DLL que o EAPHost carrega, em vez de chamá-las diretamente.

 

 




