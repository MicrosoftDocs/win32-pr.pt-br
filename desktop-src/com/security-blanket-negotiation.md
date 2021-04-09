---
title: Negociação em cobertura de segurança
description: Negociação em cobertura de segurança
ms.assetid: 5a01912d-611c-4a6e-ab9d-0243cba331f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e51407de908eaaf0f79eea452046f8e424ccf900
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008439"
---
# <a name="security-blanket-negotiation"></a>Negociação em cobertura de segurança

Uma ampla segurança é um grupo de valores que descrevem as configurações de segurança que se aplicam a todos os proxies em um processo ou apenas a um determinado proxy de interface. Uma ampla segurança inclui os seguintes valores:

-   Serviço de autenticação
-   Serviço de autorização
-   Nome da entidade de segurança
-   Nível de autenticação
-   Nível de representação
-   Identidade de autenticação
-   Funcionalidades
-   Uma ACL (lista de controle de acesso) (somente servidores)

A negociação de cobertura ampla é o processo que o COM usa para escolher as configurações de segurança para um proxy quando ele é criado. Esse processo envolve a comparação da cobertura de segurança do servidor com a cobertura de segurança do cliente e o uso desses valores para criar uma ampla cobertura de segurança padrão para o proxy. Os parágrafos a seguir explicam de onde vêm as coberturas de segurança do cliente e do servidor e descrevem como o COM negocia a cobertura de segurança para o proxy usando as amplas de segurança do cliente e do servidor.

O cliente e o servidor podem chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para especificar suas respectivas amplas de segurança. Se um aplicativo não chamar **CoInitializeSecurity** explicitamente, o com o chamará implicitamente para o aplicativo, usando valores padrão apropriados. Para obter mais informações sobre esses valores padrão, consulte [padrões de segurança com](com-security-defaults.md).

Alguns parâmetros para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) se aplicam quando o aplicativo é um servidor e alguns se aplicam quando o aplicativo é um cliente. Quando o aplicativo está agindo como um servidor, esses parâmetros são relevantes: uma ACL, uma lista de tuplas do serviço de autenticação/autorização do nome da entidade de segurança e um nível de autenticação. A chamada de um servidor para **CoInitializeSecurity**, implícita ou explícita, determina a cobertura de segurança do servidor, que permanece corrigida.

Quando o aplicativo está agindo como um cliente, os valores a seguir passados para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) são relevantes: um nível de autenticação, um nível de representação, a identidade de autenticação e os recursos. A chamada implícita ou explícita de um cliente para **CoInitializeSecurity** indica a ampla cobertura de segurança que o cliente deseja.

Quando um proxy é criado, o COM usa os valores especificados pela cobertura de segurança do servidor e a cobertura de segurança do cliente para negociar uma cobertura de segurança padrão apropriada para o proxy. COM escolhe um serviço de autenticação que funciona no cliente e no servidor. O serviço de autorização e o nome da entidade de segurança são escolhidos para trabalhar com o serviço de autenticação. Para o nível de autenticação, COM escolhe o maior dos níveis de autenticação especificados pelo cliente e o servidor. O nível de representação e os recursos escolhidos por COM são aqueles especificados pelo cliente. A identidade de autenticação é aquela especificada pelo cliente para o serviço de autenticação escolhido.

Depois que a cobertura de segurança padrão for computada, seus valores serão atribuídos ao proxy recém-criado. O cliente pode substituir as configurações de segurança para o proxy chamando [**IClientSecurity:: setampla**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Os valores especificados para **setampla** não são negociados; Eles são simplesmente atribuídos ao proxy especificado. No entanto, se os parâmetros padrão (como padrão de nível de imp do RPC \_ C \_ \_ \_ ) forem passados para setapartment, o com usará o algoritmo de negociação ampla de segurança descrito anteriormente para calcular os parâmetros padrão. 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 