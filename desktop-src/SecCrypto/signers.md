---
description: Representa uma coleção de objetos de signatário.
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: Objeto de assinantes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62c5f59fc90d0d34226b4442b8fa443ad734d474e8077bf210df8bfdf752b1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898329"
---
# <a name="signers-object"></a>Objeto de assinantes

\[O objeto de **assinantes** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use uma coleção de objetos CmsSigner. Para obter mais informações, consulte a [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O **objeto de** signatários representa uma coleção de objetos de [**assinante**](signer.md) .

## <a name="when-to-use"></a>Quando usar

O objeto de **assinantes** é usado para executar as seguintes tarefas:

-   Recupere o número de certificados na coleção.
-   Recupere um objeto de **assinantes** específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto de **assinantes** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **assinantes** tem essas propriedades.



| Propriedade                                        | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. essa propriedade é oculta no Visual Basic scripting Edition (VBScript).<br/> |
| [**Contagem**](signers-count.md)<br/>       | Somente leitura<br/> | Número de objetos de [**signatário**](signer.md) na coleção.<br/>                                                                                                                                                        |
| [**Item**](signers-item.md)<br/>         | Somente leitura<br/> | Recupera o objeto de [**signatário**](signer.md) que representa o assinante indexado. Essa é a propriedade padrão.<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto de **assinantes** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
