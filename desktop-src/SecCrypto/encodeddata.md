---
description: Representa um bloco de dados codificados ASN. 1.
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: Objeto EncodedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ba17056aaf2b038abb519c1eff230f6cccb396edea1ee9c1f96077d572e63fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874856"
---
# <a name="encodeddata-object"></a>Objeto EncodedData

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe AsnEncodedData**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1) no namespace [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **EncodedData** representa um bloco de dados codificados pelo ASN. 1.

## <a name="when-to-use"></a>Quando usar

O objeto **EncodedData** é retornado por várias propriedades de objeto CAPICOM. Quando retornado, esse objeto é usado para executar as seguintes tarefas:

-   Obtenha uma representação de cadeia de caracteres dos dados codificados.
-   Obtenha o objeto decodificador, se ele existir, que está associado aos dados codificados.
-   Determine o tipo de dados codificados.

## <a name="members"></a>Membros

O objeto **EncodedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **EncodedData** tem esses métodos.



| Método                                 | Descrição                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**Decodificador**](encodeddata-decoder.md) | Obtém um objeto decodificador, se houver.<br/>             |
| [**Formatar**](encodeddata-format.md)   | Retorna uma representação de cadeia de caracteres dos dados codificados.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **EncodedData** tem essas propriedades.



| Propriedade                                      | Tipo de acesso          | Descrição                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**Valor**](encodeddata-value.md)<br/> | Somente leitura<br/> | Recupera os dados codificados. Essa é a propriedade padrão.<br/> |



 

## <a name="remarks"></a>Comentários

O único tipo de dados codificado com suporte é [**CertificatePolicies**](certificatepolicies.md).

O objeto **EncodedData** não pode ser criado.

As seguintes propriedades de objeto capicor retornam um objeto **EncodedData** :

-   **PublicKey. EncodedKey**
-   **PublicKey. EncodedParameters**
-   **Extensão. EncodedData**
-   **Policy. EncodedData**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
