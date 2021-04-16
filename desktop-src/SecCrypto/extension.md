---
description: Representa uma única extensão de certificado.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objeto de extensão (Mmcobj. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extension
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a048cd5f29825c2d96a9d924473159e93d3e0be1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779365"
---
# <a name="extension-object"></a>Objeto de extensão

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O objeto de **extensão** representa uma única extensão de certificado.

## <a name="when-to-use"></a>Quando usar

O objeto de **extensão** é usado para executar as seguintes tarefas:

-   Recupere o OID da extensão do certificado.
-   Recupere os dados de extensão do certificado representados por um objeto [**EncodedData**](encodeddata.md) .
-   Determine se a extensão do certificado está marcada como crítica.

## <a name="members"></a>Membros

O objeto de **extensão** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto de **extensão** tem essas propriedades.



| Propriedade                                                | Tipo de acesso          | Descrição                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | Somente leitura<br/> | Recupera os dados codificados para a extensão.<br/>                                      |
| [**IsCritical**](extension-iscritical.md)<br/>   | Somente leitura<br/> | Recupera um valor booliano que indica se a extensão está marcada como crítica.<br/> |
| [**OIDs**](extension-oid.md)<br/>                 | Somente leitura<br/> | Recupera o identificador de objeto para a extensão. Essa é a propriedade padrão.<br/>   |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto de **extensão** .

O objeto de **extensão** é usado pelo objeto da coleção de [**extensões**](extensions.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| parâmetro<br/>                | <dl> <dt>Mmcobj. h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
