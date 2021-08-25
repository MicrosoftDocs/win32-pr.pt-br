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
ms.openlocfilehash: cb087afedfb6570c2d25858ca99a53749607f2260f3a6f7a24ae766e22ea3e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925276"
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
| Syntax            | [**Enumeração**](s-enumeration.md)           |



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
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
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
| System-Only            | Verdadeiro                            |
| É de valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No catálogo global      | Verdadeiro                            |
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
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
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
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
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
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
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
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
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
| System-Only            | Verdadeiro                            |
| Tem valor único       | Verdadeiro                            |
| É indexado             | Falso                           |
| No Catálogo Global      | Verdadeiro                            |
| Descritor de segurança NT | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classes usadas em        | [**Início**](c-top.md)<br/> |



 

 





