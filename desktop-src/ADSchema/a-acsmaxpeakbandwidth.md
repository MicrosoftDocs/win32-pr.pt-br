---
title: Atributo ACS-Max-Peak-Bandwidth
description: A largura de banda de pico que pode ser reservada.
ms.assetid: ee101dc9-ec67-4e1f-af8f-4ab2d2deb09a
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo ACS-Max-Peak-Bandwidth
- Esquema do AD do atributo aCSMaxPeakBandwidth
topic_type:
- apiref
api_name:
- ACS-Max-Peak-Bandwidth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3507052f5c8f20bba6647e626dbae71ec13c69a9d1d15b3304f0a7db85881df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082100"
---
# <a name="acs-max-peak-bandwidth-attribute"></a>Atributo ACS-Max-Peak-Bandwidth

A largura de banda de pico que pode ser reservada.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ACS-Max-Peak-Bandwidth               |
| Ldap-Display-Name | aCSMaxPeakBandwidth                  |
| Tamanho              | 8 bytes                              |
| Privilégio de atualização  | \-                                   |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.767               |
| System-Id-Guid    | 7f561284-5301-11d1-a9c5-0000f80367c1 |
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
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No Catálogo Global      | Falso                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Limites de recursos do ACS**](c-acsresourcelimits.md)<br/> [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No Catálogo Global      | Falso                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Limites de recursos do ACS**](c-acsresourcelimits.md)<br/> [**Sub-rede do ACS**](c-acssubnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| Tem valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No Catálogo Global      | Falso                                                                                                      |
| Descritor de segurança NT | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**Limites de recursos do ACS**](c-acsresourcelimits.md)<br/> [**ACS-sub-rede**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**ACS-limites de recursos**](c-acsresourcelimits.md)<br/> [**ACS-sub-rede**](c-acssubnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**ACS-limites de recursos**](c-acsresourcelimits.md)<br/> [**ACS-sub-rede**](c-acssubnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------|
| ID do link                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falso                                                                                                      |
| É de valor único       | Verdadeiro                                                                                                       |
| É indexado             | Falso                                                                                                      |
| No catálogo global      | Falso                                                                                                      |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| Classes usadas em        | [**ACS-limites de recursos**](c-acsresourcelimits.md)<br/> [**ACS-sub-rede**](c-acssubnet.md)<br/> |



 

 





