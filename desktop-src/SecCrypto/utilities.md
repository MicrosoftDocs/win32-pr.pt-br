---
description: Fornece funcionalidade para geração de número aleatório, conversões e codificação e decodificação de Base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Objeto Utilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754586"
---
# <a name="utilities-object"></a>Objeto Utilities

\[O objeto **Utilities** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O objeto **Utilities** fornece funcionalidade para geração de número aleatório, conversões e codificação e decodificação de Base64.

## <a name="when-to-use"></a>Quando usar

O objeto **Utilities** é usado para executar as seguintes tarefas:

-   Codifique uma cadeia de caracteres como Base64 ou decodifique uma cadeia de caracteres de Base64.
-   Converter uma cadeia de caracteres de pacote binário em uma matriz de bytes e vice-versa.
-   Converter uma cadeia de caracteres de um binário compactado em uma cadeia de caracteres hexadecimal e vice-versa.
-   Gerar um número aleatório seguro.
-   Converter a hora local em tempo universal coordenado (hora de Greenwich) e vice-versa.

## <a name="members"></a>Membros

O objeto **Utilities** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **Utilities** tem esses métodos.



| Método                                                               | Descrição                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**Base64Decode**](utilities-base64decode.md)                       | Decodifica uma cadeia de caracteres de Base64.<br/>                                     |
| [**Base64Encode**](utilities-base64encode.md)                       | Codifica uma cadeia de caracteres como Base64.<br/>                                       |
| [**BinaryStringToByteArray**](utilities-binarystringtobytearray.md) | Converte uma cadeia de caracteres de pacote binário em uma matriz de bytes.<br/>             |
| [**BinaryToHex**](utilities-binarytohex.md)                         | Converte uma cadeia de caracteres de pacote binário em uma cadeia de caracteres hexadecimal.<br/>          |
| [**ByteArrayToBinaryString**](utilities-bytearraytobinarystring.md) | Converte uma matriz de bytes em uma cadeia de caracteres de pacote binário.<br/>             |
| [**Getrandom**](utilities-getrandom.md)                             | Gera um número aleatório seguro.<br/>                                 |
| [**HexToBinary**](utilities-hextobinary.md)                         | Converte uma cadeia de caracteres hexadecimal em uma cadeia de caracteres de pacote binário.<br/>          |
| [**LocalTimeToUTCTime**](utilities-localtimetoutctime.md)           | Converte a hora local do computador em tempo universal coordenado.<br/> |
| [**UTCTimeToLocalTime**](utilities-utctimetolocaltime.md)           | Converte o tempo universal coordenado na hora local do computador.<br/> |



 

## <a name="remarks"></a>Comentários

O objeto **Utilities** pode ser criado e é seguro para scripts. O ProgID para o objeto **Utilities** é CAPICOM. Utilities. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




