---
title: Descrição de segurança
description: Uma descrição de segurança é representada por uma estrutura WS SECURITY DESCRIPTION e uma instância de uma descrição de segurança é fornecida quando você chama a função WsCreateChannel para criar um canal seguro ou a \_ \_ função WsCreateListener para criar um ouvinte.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Serviços Web de descrição de segurança para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a2395e2c1e894968f47fa41e98599ec333f6d2724cf6ffe6cbc5219396bca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083151"
---
# <a name="security-description"></a>Descrição de segurança

Uma descrição de segurança é representada por uma estrutura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e uma instância de uma descrição de segurança é fornecida quando você chama a [**função WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) para criar um canal seguro ou a [**função WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) para criar um ouvinte.


## <a name="structure-of-a-security-description"></a>Estrutura de uma descrição de segurança

O modelo básico de segurança de canal é que um canal é protegido com um ou mais tokens de segurança. Refletindo esse modelo, a estrutura DESCRIÇÃO DE SEGURANÇA do [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contém uma lista de vinculações de segurança, representadas por estruturas DE ASSOCIAÇÃO DE SEGURANÇA do [**\_ \_ WS,**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) e cada associação de segurança descreve como um token de segurança é obtido e usado no canal. O tipo de segurança usado em um canal é decidido pela seleção de subtipos de associação de segurança incluídos na descrição de segurança.

As configurações de segurança opcionais específicas de uma associação de segurança são [especificadas](security-binding-settings.md) como configurações de associação de segurança na estrutura de associação de segurança; No entanto, as configurações de todo o canal, independentemente das  vinculações de segurança, são [especificadas](security-channel-settings.md) diretamente como configurações de canal de segurança no campo propriedades da própria descrição de segurança.

![Diagrama mostrando a estrutura de uma descrição de segurança.](images/securitydescription.png)

Os elementos de API a seguir são usados com descrições de segurança.

| Estrutura                                                    | Descrição                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**DESCRIÇÃO DE SEGURANÇA DO WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | A estrutura de nível superior usada para especificar os requisitos de segurança para um canal (no lado do cliente) ou um ouvinte (no lado do servidor). |



 

 

 




