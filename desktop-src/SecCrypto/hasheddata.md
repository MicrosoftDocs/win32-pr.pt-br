---
description: Fornece funcionalidade para hash de uma cadeia de caracteres.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Objeto HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c61d52e7621acffb76df5bcb05693efb48c695c15e79d1f0a45523a0f0087c6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006444"
---
# <a name="hasheddata-object"></a>Objeto HashedData

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use [**a Classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System.Security.Cryptography.**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)\]

O **objeto HashedData** fornece funcionalidade para hash de uma cadeia de caracteres.

## <a name="when-to-use"></a>Quando usar

O **objeto HashedData** é usado para executar as seguintes tarefas:

-   Especifique a cadeia de caracteres de conteúdo que contém os dados a serem com hashed.
-   Aplique um algoritmo de hash especificado à cadeia de caracteres de conteúdo.

## <a name="members"></a>Membros

O **objeto HashedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto HashedData** tem esses métodos.



| Método                          | Descrição                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Hash**](hasheddata-hash.md) | Cria um hash da cadeia de caracteres especificada.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto HashedData** tem essas propriedades.



| Propriedade                                             | Tipo de acesso           | Descrição                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](hasheddata-algorithm.md)<br/> | Leitura/gravação<br/> | Define ou recupera o tipo de algoritmo de hash usado.<br/>                                                                                                                     |
| [**Valor**](hasheddata-value.md)<br/>         | Somente leitura<br/>  | Recupera os dados com hash após chamadas bem-sucedidas para o [**método Hash.**](hasheddata-hash.md) O hash é retornado em formato hexadecimal. Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

Para criar o hash de uma grande quantidade de dados, chame o método [**Hash**](hasheddata-hash.md) para cada parte dos dados. O hash de cada parte dos dados é concatenado à [**propriedade Value**](hasheddata-value.md) até que a propriedade seja lida. O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.

O **objeto HashedData** pode ser criado e é seguro para scripts. O ProgID para o **objeto HashedData** é "CAPICOM. HashedData.1".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
