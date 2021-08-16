---
description: O objeto EnvelopedData fornece propriedades e métodos para envolver dados para privacidade por criptografia.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Objeto EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: af88fd9b4be0c7ddd9fe5dfc204558c1a36cab418166f73c8de0ec0c06c0a8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766107"
---
# <a name="envelopeddata-object"></a>Objeto EnvelopedData

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use [**a Classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

O **objeto EnvelopedData** fornece propriedades e métodos para envolver dados para privacidade por criptografia. Para envelopar dados, uma chave de criptografia de sessão é gerada. Essa [*chave de*](../secgloss/s-gly.md) sessão é criptografada para cada destinatário pretendido usando a chave pública do destinatário pretendido do certificado do destinatário. [](../secgloss/p-gly.md) Os dados criptografados e o conjunto de chaves de sessão criptografadas podem ser enviados a todos os destinatários pretendido. A mensagem gerada está no formato PKCS \# 7.

## <a name="members"></a>Membros

O **objeto EnvelopedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto EnvelopedData** tem esses métodos.



| Método                                   | Descrição                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Descriptografar**](envelopeddata-decrypt.md) | Descriptografa o conteúdo envelhado.<br/>                                                                      |
| [**Encrypt**](envelopeddata-encrypt.md) | Criptografa o conteúdo, criptografa uma chave de sessão para cada destinatário e retorna o BLOB criptografado.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto EnvelopedData** tem essas propriedades.



| Propriedade                                                  | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](envelopeddata-algorithm.md)<br/>   | Leitura/gravação<br/> | Algoritmo de criptografia e [*comprimento da chave.*](../secgloss/k-gly.md)<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Conteúdo**](envelopeddata-content.md)<br/>       | Leitura/gravação<br/> | O conteúdo de texto não criptografado de uma mensagem a ser enveloada. A definição dessa propriedade deve ser feita antes que [**o método Encrypt**](envelopeddata-encrypt.md) seja chamado.<br/> Quando o valor dessa propriedade é redefinido, [](../secgloss/s-gly.md) direta ou indiretamente, todo o estado do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.<br/> Essa é a propriedade padrão.<br/> |
| [**Destinatários**](envelopeddata-recipients.md)<br/> | Somente leitura<br/>  | Coleção de [**objetos certificate**](certificate.md) para receber a mensagem envelocada.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentários

O **objeto EnvelopedData** pode ser criado e é seguro para scripts. O ProgID para o **objeto EnvelopedData** é CAPICOM. EnvelopedData.1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
