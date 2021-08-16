---
title: Atributo ms-DS-Egress-Claims-Transformation-Policy
description: Este é um link para um Objeto de Política de Transformação de Declarações para as declarações de saída (declarações que deixam essa floresta) para o domínio confiável.
ms.assetid: 693ebb45-e90c-4629-8afc-f048c83b4b95
ms.tgt_platform: multiple
keywords:
- ms-DS-Egress-Claims-Transformation-Policy atributo AD Schema
- Esquema AD do atributo msDS-EgressClaimsTransformationPolicy
topic_type:
- apiref
api_name:
- ms-DS-Egress-Claims-Transformation-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99ec71308c0ebc17942b3400d8ddd9e87ff88ea29d4f21e93047c3aa80f77128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118014649"
---
# <a name="ms-ds-egress-claims-transformation-policy-attribute"></a>Atributo ms-DS-Egress-Claims-Transformation-Policy

Este é um link para um Objeto de Política de Transformação de Declarações para as declarações de saída (declarações que deixam essa floresta) para o domínio confiável. Isso é aplicável somente a uma confiança entre florestas de entrada ou bidirecional. Quando esse link não está presente, todas as declarações têm permissão para sair como estão.



| Entrada | Valor |
|-------------------|-------------------------------------------|
| CN                | ms-DS-Egress-Claims-Transformation-Policy |
| Ldap-Display-Name | msDS-EgressClaimsTransformationPolicy     |
| Tamanho              | \-                                        |
| Privilégio de atualização  | \-                                        |
| Frequência de atualização  | \-                                        |
| Attribute-Id      | 1.2.840.113556.1.4.2192                   |
| System-Id-Guid    | c137427e-9a73-b040-9190-1b095bb43288      |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)   |



## <a name="implementations"></a>Implementações

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------|
| ID do link                | 2192                                                 |
| MAPI-Id                | \-                                                   |
| System-Only            | Falso                                                |
| Tem valor único       | Verdadeiro                                                 |
| É indexado             | Falso                                                |
| No Catálogo Global      | Falso                                                |
| Descritor de segurança NT | O:BAG:BAD:S:                                         |
| Range-Lower            | \-                                                   |
| Range-Upper            | \-                                                   |
| Search-Flags           | 0x00000000                                           |
| System-Flags           | 0x00000010                                           |
| Classes usadas em        | [**Domínio confiável**](c-trusteddomain.md)<br/> |



 

 





