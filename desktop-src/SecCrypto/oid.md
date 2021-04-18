---
description: Representa um OID (identificador de objeto) que é usado por várias propriedades de CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: Objeto OID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778676"
---
# <a name="oid-object"></a>Objeto OID

\[O objeto **OID** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **OID** representa um OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) que é usado por várias propriedades CAPICOM.

## <a name="when-to-use"></a>Quando usar

O objeto **OID** é usado para executar as seguintes tarefas:

-   Defina ou recupere um nome de capicor e o nome de exibição para o OID.
-   Defina ou recupere o número pontilhado para o OID.

## <a name="members"></a>Membros

O objeto **OID** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **OID** tem essas propriedades.



| Propriedade                                            | Tipo de acesso           | Descrição                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Leitura/gravação<br/> | Define ou recupera o nome de exibição para o OID.<br/>                                       |
| [**Nome**](oid-name.md)<br/>                 | Leitura/gravação<br/> | Define ou recupera o nome definido pelo CAPICOM para o OID. Essa é a propriedade padrão.<br/> |
| [**Valor**](oid-value.md)<br/>               | Leitura/gravação<br/> | Define ou recupera o valor do número pontilhado OID do OID.<br/>                      |



 

## <a name="remarks"></a>Comentários

O objeto **OID** pode ser criado e é seguro para scripts. O ProgID para o objeto **OID** é CAPICOM. OID. 1.

As seguintes propriedades de objeto capicor retornam um objeto **OID** :

-   [**PolicyInformation. OID**](policyinformation-oid.md)
-   [**Qualifier. OID**](qualifier-oid.md)
-   [**Extensão. OID**](extension-oid.md)
-   [**Modelo. OID**](template-oid.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
