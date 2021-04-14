---
title: ms-DS-repl-atributo de modo de autenticação
description: O atributo ms-DS-repl-authentication-mode é usado para especificar qual método de autenticação é usado para autenticar parceiros de replicação.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-repl-authentication-mode
- Esquema de AD do atributo msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456283"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a>ms-DS-repl-atributo de modo de autenticação

O atributo **MS-DS-repl-authentication-mode** é usado para especificar qual método de autenticação é usado para autenticar parceiros de replicação. Esse atributo se aplica à partição de configuração de uma instância do ADAM.

Os valores a seguir são os possíveis valores para esse atributo.

| Valor        | Método de autenticação                          | Descrição                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0<br/> | Passagem negociada<br/>             | Todas as instâncias do ADAM no conjunto de configuração usam um nome de conta e senha idênticos como a conta de serviço do ADAM.<br/>                                                 |
| 1<br/> | Negociado<br/>                          | A tentativa com a autenticação Kerberos (usando SPNs) é feita primeiro. Se essa tentativa falhar, a tentativa com a autenticação NTLM será realizada. Se o NTLM falhar, as instâncias do ADAM não serão replicadas.<br/> |
| 2<br/> | Autenticação mútua com o Kerberos<br/> | Autenticação Kerberos usando SPNs (nomes principais de serviços) necessária. Se a autenticação Kerberos falhar, as instâncias do ADAM não serão replicadas.<br/>                |



 

A tabela a seguir contém os identificadores programáticos para os valores desse atributo.

| Valor        | Identificador (de NTDSAPI. h)                                               |
|--------------|---------------------------------------------------------------------------|
| 0<br/> | **modo de autenticação de repl do ADAM \_ \_ \_ \_ negociar \_ passagem \_**<br/> |
| 1<br/> | **modo de autenticação do ADAM \_ repl \_ \_ \_ Negotiate**<br/>                |
| 2<br/> | **autorização mútua do modo de autenticação do ADAM \_ repl \_ \_ \_ \_ \_ necessário**<br/>   |



 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-repl-authentication-mode       |
| LDAP-Display-Name | msDS-ReplAuthenticationMode          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1861              |
| System-ID-GUID    | 6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|-----------------------------------------------------|
| ID do link                | \-                                                  |
| MAPI-Id                | \-                                                  |
| System-Only            | Falso                                               |
| É de valor único       | True                                                |
| É indexado             | Falso                                               |
| No catálogo global      | Falso                                               |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                        |
| Range-Lower            | \-                                                  |
| Range-Upper            | \-                                                  |
| Search-Flags           | 0x00000000                                          |
| System-Flags           | 0x00000010                                          |
| Classes usadas em        | [**Configuração**](c-configuration.md)<br/> |



 

 





