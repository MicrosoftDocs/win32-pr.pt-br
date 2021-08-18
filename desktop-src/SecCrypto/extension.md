---
description: Representa uma única extensão de certificado.
ms.assetid: cca3121d-0f0f-4de2-a225-6dd3910078d7
title: Objeto de extensão (Mmcobj.h)
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
ms.openlocfilehash: e311c6dc69f40d32163c70cabf6a38780a989764bd77f4023c61ede5c1ba713c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006954"
---
# <a name="extension-object"></a>Objeto de extensão

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, [**use a Classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) no namespace [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

O **objeto Extension** representa uma única extensão de certificado.

## <a name="when-to-use"></a>Quando usar

O **objeto** Extension é usado para executar as seguintes tarefas:

-   Recupere o OID da extensão de certificado.
-   Recupere os dados de extensão de certificado representados por [**um objeto EncodedData.**](encodeddata.md)
-   Determine se a extensão de certificado está marcada como crítica.

## <a name="members"></a>Membros

O **objeto** Extension tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O **objeto Extension** tem essas propriedades.



| Propriedade                                                | Tipo de acesso          | Descrição                                                                                   |
|:--------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**EncodedData**](extension-encodeddata.md)<br/> | Somente leitura<br/> | Recupera os dados codificados para a extensão.<br/>                                      |
| [**Iscritical**](extension-iscritical.md)<br/>   | Somente leitura<br/> | Recupera um valor booliana que indica se a extensão está marcada como crítica.<br/> |
| [**Oid**](extension-oid.md)<br/>                 | Somente leitura<br/> | Recupera o identificador de objeto para a extensão. Essa é a propriedade padrão.<br/>   |



 

## <a name="remarks"></a>Comentários

O **objeto Extension** não pode ser criado.

O **objeto** Extension é usado pelo [**objeto de coleção**](extensions.md) Extensões.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| Cabeçalho<br/>                | <dl> <dt>Mmcobj.h</dt> </dl>    |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
