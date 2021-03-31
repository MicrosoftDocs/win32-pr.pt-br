---
title: Instance-Type atributo
description: Um campo de bits que determina como o objeto é instanciado em um servidor específico.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Esquema de Instance-Type do atributo AD
- atributo do AD de atributos InstanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103645483"
---
# <a name="instance-type-attribute"></a>Instance-Type atributo

Um campo de bits que determina como o objeto é instanciado em um servidor específico. O valor desse atributo pode diferir em réplicas diferentes, mesmo que as réplicas estejam em sincronia.

Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.

| Valor      | Descrição                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | O cabeçalho do contexto de nomenclatura.                                                                        |
| 0x00000002 | Esta réplica não está instanciada.                                                                  |
| 0x00000004 | O objeto é gravável neste diretório.                                                          |
| 0x00000008 | O contexto de nomenclatura acima deste diretório é mantido.                                       |
| 0x00000010 | O contexto de nomenclatura está no processo de ser construído pela primeira vez usando a replicação. |
| 0x00000020 | O contexto de nomenclatura está no processo de ser removido do DSA local.                          |



 



| Entrada | Valor |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| LDAP-Display-Name | instanceType                                   |
| Tamanho              | 4 bytes.                                       |
| Privilégio de atualização  | Esse valor é definido pelo administrador do esquema. |
| Frequência de atualização  | Quando o objeto é criado.                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-ID-GUID    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Sintaxe            | [**Enumeração**](s-enumeration.md)           |



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
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|---------------------------------|
| ID do link                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| É de valor único       | True                            |
| É indexado             | Falso                           |
| No catálogo global      | True                            |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





