---
title: Search-Flags atributo
description: Contém um conjunto de sinalizadores que especificam informações de pesquisa e indexação para um atributo.
ms.assetid: 55fc4398-25d2-466a-9aa9-fa375d827023
ms.tgt_platform: multiple
keywords:
- Search-Flags atributo AD Schema
- Esquema do AD do atributo searchFlags
topic_type:
- apiref
api_name:
- Search-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83de0ed819cecb08e5c176aaaec4c200b69413649e85d1c1ab2d743944210e06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119646306"
---
# <a name="search-flags-attribute"></a>Search-Flags atributo

Contém um conjunto de sinalizadores que especificam informações de pesquisa e indexação para um atributo. Consulte Observações.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Search-Flags                         |
| Ldap-Display-Name | searchFlags                          |
| Tamanho              | \-                                   |
| Privilégio de atualização  | Administrador de esquema                 |
| Frequência de atualização  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.2.334               |
| System-Id-Guid    | bf967a2d-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeração**](s-enumeration.md) |



## <a name="implementations"></a>Implementações

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Esquema de atributo**](c-attributeschema.md)<br/> |



## <a name="adam"></a>Adam



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| Tem valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No Catálogo Global      | Falso                                                    |
| Descritor de segurança NT | O:BAG:BAD:S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------|
| ID do link                | \-                                                       |
| MAPI-Id                | 0x812D                                                   |
| System-Only            | Falso                                                    |
| É de valor único       | Verdadeiro                                                     |
| É indexado             | Falso                                                    |
| No catálogo global      | Falso                                                    |
| NT-Security-Descriptor | O:BAG: INADEQUADO: S:                                             |
| Range-Lower            | \-                                                       |
| Range-Upper            | \-                                                       |
| Search-Flags           | 0x00000000                                               |
| System-Flags           | 0x00000010                                               |
| Classes usadas em        | [**Atributo-esquema**](c-attributeschema.md)<br/> |



## <a name="remarks"></a>Comentários

Esse atributo pode ser zero ou uma combinação de um ou mais dos valores a seguir.



| Valor            | Descrição                                                                                                                                                                                                                                                                                                                                                               |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1 (0x00000001)   | Crie um índice para o atributo .                                                                                                                                                                                                                                                                                                                                        |
| 2 (0x00000002)   | Crie um índice para o atributo em cada contêiner.                                                                                                                                                                                                                                                                                                                      |
| 4 (0x00000004)   | Adicione esse atributo ao conjunto ANR (Resolução de Nomes Ambíguos). Isso é usado para ajudar a localizar um objeto quando apenas informações parciais são fornecidas. Por exemplo, se o filtro LDAP for (ANR=JEFF), a pesquisa encontrará cada objeto em que o nome, sobrenome, endereço de email ou outro atributo ANR é igual a JEFF. O bit 0 deve ser definido para que esse índice afete. |
| 8 (0x00000008)   | Preserve esse atributo no objeto de exclusão para objetos excluídos.                                                                                                                                                                                                                                                                                                      |
| 16 (0x00000010)  | Copie o valor desse atributo quando o objeto for copiado.                                                                                                                                                                                                                                                                                                              |
| 32 (0x00000020)  | Crie um índice de tupla para o atributo. Isso melhorará as pesquisas em que o curinga aparece na frente da cadeia de caracteres de pesquisa. Por exemplo, (sn= \* mith).                                                                                                                                                                                                                |
| 64(0x00000040)   | Suporte a partir do ADAM. Cria um índice para ajudar muito o desempenho da VLV em atributos arbitrários.                                                                                                                                                                                                                                                                  |
| 128 (0x00000080) | Marcar atributo como confidencial. Ignorado para atributos de esquema base (systemFlags=0x10).                                                                                                                                                                                                                                                                                    |
| 64 (0x00000040)  | Suporte a partir do Windows Server 2008. Crie um índice para melhorar o desempenho da pesquisa VLV nesse atributo.                                                                                                                                                                                                                                                        |



 

 

 





