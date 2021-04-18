---
description: Fornece acesso às informações de política de uma extensão.
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: Objeto PolicyInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755040"
---
# <a name="policyinformation-object"></a>Objeto PolicyInformation

\[O objeto **PolicyInformation** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) chamando o construtor que usa um OID como parâmetro e, em seguida, use o OID para políticas de certificado para processar informações de política na extensão de políticas de certificado.\]

O objeto **PolicyInformation** fornece acesso às informações de política de uma extensão.

## <a name="when-to-use"></a>Quando usar

O objeto **PolicyInformation** é usado para executar as seguintes tarefas:

-   Recupere a OID da política.
-   Recupere uma coleção dos qualificadores da política.

## <a name="members"></a>Membros

O objeto **PolicyInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **PolicyInformation** tem essas propriedades.



| Propriedade                                                      | Descrição                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**OIDs**](policyinformation-oid.md)<br/>               | Recupera o OID da política, como um objeto [**OID**](oid.md) . Essa é a propriedade padrão.<br/>       |
| [**Qualificadores**](policyinformation-qualifiers.md)<br/> | Recupera uma coleção de qualificadores de política, como um objeto de [**qualificadores**](qualifiers.md) .<br/> |



 

## <a name="remarks"></a>Comentários

O objeto **PolicyInformation** não pode ser criado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
