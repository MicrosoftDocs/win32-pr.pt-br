---
title: Descrição de segurança
description: Uma descrição de segurança é representada por uma \_ \_ estrutura de descrição de segurança do WS, e uma instância de descrições de segurança é fornecida quando você chama a função WsCreateChannel para criar um canal seguro ou a função WsCreateListener para criar um ouvinte.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Serviços Web de descrição de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104091863"
---
# <a name="security-description"></a>Descrição de segurança

Uma descrição de segurança é representada por uma estrutura de [**\_ \_ Descrição de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) , e uma instância de descrições de segurança é fornecida quando você chama a função [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para criar um canal seguro ou a função [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) para criar um ouvinte.


## <a name="structure-of-a-security-description"></a>Estrutura de uma descrição de segurança

O modelo básico de segurança de canal é que um canal é protegido com um ou mais tokens de segurança. Refletindo esse modelo, a estrutura de [**\_ \_ Descrição do WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contém uma lista de associações de segurança, representadas por estruturas de [**\_ \_ Associação de segurança do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , e cada associação de segurança descreve como um token de segurança é obtido e usado no canal. O tipo de segurança usado em um canal é decidido pela seleção de subtipos de associação de segurança que são incluídos na descrição de segurança.

Configurações de segurança opcionais específicas para uma associação de segurança são especificadas como [configurações de associação de segurança](security-binding-settings.md) na estrutura de associação de segurança; no entanto, as configurações de todo o canal independentemente das associações de segurança são especificadas diretamente como [configurações de canal de segurança](security-channel-settings.md) no campo **Propriedades** da própria descrição de segurança.

![Diagrama mostrando a estrutura de uma descrição de segurança.](images/securitydescription.png)

Os seguintes elementos de API são usados com descrições de segurança.

| Estrutura                                                    | Descrição                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Descrição da segurança do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | A estrutura de nível superior usada para especificar os requisitos de segurança para um canal (no lado do cliente) ou um ouvinte (no lado do servidor). |



 

 

 




