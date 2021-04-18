---
description: Representa uma coleção de objetos de certificado.
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: Objeto de destinatários
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758159"
---
# <a name="recipients-object"></a>Objeto de destinatários

\[O objeto **Recipients** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe CmsRecipientCollection**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto de **destinatários** representa uma coleção de objetos de [**certificado**](certificate.md) . Cada objeto representa um destinatário pretendido da mensagem envelopada. Os dados em um objeto [**EnvelopedData**](envelopeddata.md) são criptografados com uma chave de sessão [*simétrica*](../secgloss/s-gly.md) e essa chave de sessão simétrica é criptografada para cada destinatário usando a chave pública do certificado do destinatário desejado. Um destinatário com acesso à [*chave privada*](../secgloss/p-gly.md) associada à [*chave pública*](../secgloss/p-gly.md) de um certificado pode descriptografar a [*chave de sessão*](../secgloss/s-gly.md) e usar a chave de sessão descriptografada para descriptografar os dados reais.

## <a name="when-to-use"></a>Quando usar

O objeto **Recipients** é usado para executar as seguintes tarefas:

-   Adicionar ou remover um objeto de [**certificado**](certificate.md) da coleção.
-   Recupere o número de certificados na coleção.
-   Recupere um objeto de **destinatários** específico da coleção.
-   Iterar pela coleção.

## <a name="members"></a>Membros

O objeto de **destinatários** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Recipients** tem esses métodos.



| Método                              | Descrição                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**Agrega**](recipients-add.md)       | Adiciona um objeto de [**certificado**](certificate.md) à coleção.<br/>         |
| [**Formatação**](recipients-clear.md)   | Remove todos os objetos de [**certificado**](certificate.md) da coleção.<br/> |
| [**Remover**](recipients-remove.md) | Remove um objeto de [**certificado**](certificate.md) da coleção.<br/>    |



 

### <a name="properties"></a>Propriedades

O objeto **Recipients** tem essas propriedades.



| Propriedade                                           | Tipo de acesso          | Descrição                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | Somente leitura<br/> | Recupera uma interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) em um objeto que pode ser usado para enumerar a coleção. Essa propriedade é oculta em Visual Basic Scripting Edition (VBScript).<br/> |
| [**Contar**](recipients-count.md)<br/>       |                      | O número de objetos na coleção de **destinatários** .<br/>                                                                                                                                                              |
| [**Item**](recipients-item.md)<br/>         |                      | Um objeto indexado na coleção. Essa é a propriedade padrão.<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Não é possível criar o objeto de **destinatários** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
