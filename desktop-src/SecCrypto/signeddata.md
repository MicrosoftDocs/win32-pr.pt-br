---
description: Fornece propriedades e métodos para estabelecer o conteúdo a ser assinado com uma assinatura digital, assinar ou coassinar dados digitalmente e verificar a assinatura digital de dados assinados. A mensagem assinada está no \# formato PKCS 7.
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: Objeto SignedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788102"
---
# <a name="signeddata-object"></a>Objeto SignedData

\[O objeto **SignedData** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe SignedCms**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **SignedData** fornece propriedades e métodos para estabelecer o conteúdo a ser assinado com uma [*assinatura digital*](../secgloss/d-gly.md), para assinar ou coassinar dados digitalmente e para verificar a assinatura digital de dados assinados. A mensagem assinada está no \# formato PKCS 7.

Uma assinatura de dados, se verificada, comprova a associação entre um signatário e dados e mostra que os dados não foram alterados de nenhuma forma após a criação da assinatura.

## <a name="members"></a>Membros

O objeto **SignedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **SignedData** tem esses métodos.



| Método                              | Descrição                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**Coassinar**](signeddata-cosign.md) | Assina uma mensagem já assinada.<br/>                       |
| [**Assinar**](signeddata-sign.md)     | Cria uma assinatura digital no conteúdo a ser assinado.<br/> |
| [**Verificar**](signeddata-verify.md) | Determina a validade de uma assinatura ou assinaturas.<br/>    |



 

### <a name="properties"></a>Propriedades

O objeto **SignedData** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificados**](signeddata-certificates.md)<br/> | Somente leitura<br/>  | Recupera a coleção de [**certificados**](certificates.md) dos dados assinados.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**Disputa**](signeddata-content.md)<br/>           | Leitura/gravação<br/> | Dados a serem assinados. Essa propriedade deve ser inicializada antes que o método [**Sign**](signeddata-sign.md) seja chamado.<br/> Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer assinatura associada ao objeto antes da alteração da propriedade é perdida.<br/> Essa é a propriedade padrão.<br/> |
| [**Signatários**](signeddata-signers.md)<br/>           | Somente leitura<br/>  | Recupera a coleção de [**assinantes**](signers.md) que representa os criadores de assinatura dos dados.<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>Comentários

O objeto **SignedData** pode ser criado e é seguro para scripts. O ProgID do objeto **SignedData** é CAPICOM. SignedData. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
