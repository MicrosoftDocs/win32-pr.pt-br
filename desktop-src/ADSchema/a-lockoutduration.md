---
title: Lockout-Duration atributo
description: A quantidade de tempo em que uma conta é bloqueada devido à Lockout-Threshold sendo excedida.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Esquema de Lockout-Duration do atributo AD
- Esquema de AD do atributo lockoutDuration
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105753825"
---
# <a name="lockout-duration-attribute"></a>Lockout-Duration atributo

A quantidade de tempo que uma conta está bloqueada devido ao [**limite de bloqueio**](a-lockoutthreshold.md) ser excedido. Esse valor é armazenado como um inteiro grande que representa o negativo do número de intervalos de 100 a nanossegundos a partir do momento em que o [**limite de bloqueio**](a-lockoutthreshold.md) é excedido e deve decorrer antes que a conta seja desbloqueada.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Lockout-Duration                     |
| LDAP-Display-Name | lockoutDuration                      |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Administrador de domínio                 |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.60                |
| System-ID-GUID    | bf9679a5-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervalo**](s-interval.md)       |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| É de valor único       | True                                                                                                                                                  |
| É indexado             | Falso                                                                                                                                                 |
| No catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classes usadas em        | [**Política de domínio**](c-domainpolicy.md)<br/> [**Sam-domínio**](c-samdomain.md)<br/> [**Sam-domínio-base**](c-samdomainbase.md)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Limite de bloqueio**](a-lockoutthreshold.md)
</dt> </dl>

 

 





