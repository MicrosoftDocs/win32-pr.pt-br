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
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787450"
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
| [**\_NewEnum**](signers-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](signers-count.md)<br/>       | Somente leitura<br/> | Número de objetos de [**signatário**](signer.md) na coleção.<br/>                                                                                                                                                        |
| [**Item**](signers-item.md)<br/>         | Somente leitura<br/> | Recupera o objeto de [**signatário**](signer.md) que representa o assinante indexado. Essa é a propriedade padrão.<br/>                                                                                                      |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto de **assinantes** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
