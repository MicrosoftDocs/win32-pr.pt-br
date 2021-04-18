---
description: Fornece a funcionalidade para o hash de uma cadeia de caracteres.
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
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778685"
---
# <a name="hasheddata-object"></a>Objeto HashedData

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe HashAlgorithm**](/previous-versions/windows/) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **HashedData** fornece a funcionalidade para o hash de uma cadeia de caracteres.

## <a name="when-to-use"></a>Quando usar

O objeto **HashedData** é usado para executar as seguintes tarefas:

-   Especifique a cadeia de caracteres de conteúdo que contém os dados a serem codificados em hash.
-   Aplique um algoritmo de hash especificado à cadeia de caracteres de conteúdo.

## <a name="members"></a>Membros

O objeto **HashedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **HashedData** tem esses métodos.



| Método                          | Descrição                                        |
|:--------------------------------|:---------------------------------------------------|
| [**Tralha**](hasheddata-hash.md) | Cria um hash da cadeia de caracteres especificada.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **HashedData** tem essas propriedades.



| Propriedade                                             | Tipo de acesso           | Descrição                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](hasheddata-algorithm.md)<br/> | Leitura/gravação<br/> | Define ou recupera o tipo de algoritmo de hash usado.<br/>                                                                                                                     |
| [**Valor**](hasheddata-value.md)<br/>         | Somente leitura<br/>  | Recupera os dados com hash após chamadas bem-sucedidas para o método de [**hash**](hasheddata-hash.md) . O hash é retornado no formato hexadecimal. Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

Para criar o hash de uma grande quantidade de dados, chame o método de [**hash**](hasheddata-hash.md) para cada dado. O hash de cada parte dos dados é concatenado à propriedade [**Value**](hasheddata-value.md) até que a propriedade seja lida. O conteúdo da propriedade **Value** é redefinido quando a propriedade é lida.

O objeto **HashedData** pode ser criado e é seguro para scripts. O ProgID do objeto **HashedData** é "CAPICOM. HashedData. 1 ".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
