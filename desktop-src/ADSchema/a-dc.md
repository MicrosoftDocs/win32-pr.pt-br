---
title: Domain-Component atributo
description: O atributo de nomenclatura para objetos de domínio e DNS. Geralmente exibido como DC DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Esquema de Domain-Component do atributo AD
- Esquema de AD do atributo de DC
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086712"
---
# <a name="domain-component-attribute"></a>Domain-Component atributo

O atributo de nomenclatura para objetos de domínio e DNS. Geralmente exibido como DC = DomainName.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| LDAP-Display-Name | dc                                          |
| Tamanho              | \-                                          |
| Privilégio de atualização  | Administrador de domínio                        |
| Frequência de atualização  | Quando o domínio é criado.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-ID-GUID    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Syntax            | [**Cadeia de caracteres (Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| É de valor único       | True                                                                                                                    |
| É indexado             | Falso                                                                                                                   |
| No catálogo global      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Controlador**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| É de valor único       | True                                                                                                                    |
| É indexado             | Falso                                                                                                                   |
| No catálogo global      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Controlador**](c-domain.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------------|
| ID do link                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| É de valor único       | True                                  |
| É indexado             | Falso                                 |
| No catálogo global      | True                                  |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Classes usadas em        | [**Controlador**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| É de valor único       | True                                                                                                                    |
| É indexado             | Falso                                                                                                                   |
| No catálogo global      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Controlador**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| É de valor único       | True                                                                                                                    |
| É indexado             | Falso                                                                                                                   |
| No catálogo global      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Controlador**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| É de valor único       | True                                                                                                                    |
| É indexado             | Falso                                                                                                                   |
| No catálogo global      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Controlador**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| É de valor único       | True                                                                                                                    |
| É indexado             | Falso                                                                                                                   |
| No catálogo global      | True                                                                                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Classes usadas em        | [**Nó DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Controlador**](c-domain.md)<br/> |



 

 





