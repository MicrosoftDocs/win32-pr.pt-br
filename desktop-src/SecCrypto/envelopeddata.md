---
description: O objeto EnvelopedData fornece propriedades e métodos para envelope dados para privacidade por criptografia.
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
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747641"
---
# <a name="envelopeddata-object"></a>Objeto EnvelopedData

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O objeto **EnvelopedData** fornece propriedades e métodos para envelope dados para privacidade por criptografia. Para envelope dados, uma chave criptográfica da sessão é gerada. Essa [*chave de sessão*](../secgloss/s-gly.md) é criptografada para cada destinatário pretendido usando a [*chave pública*](../secgloss/p-gly.md) do destinatário pretendido do certificado do destinatário. Os dados criptografados e o conjunto de chaves de sessão criptografadas podem ser enviados a todos os destinatários pretendidos. A mensagem gerada está no \# formato PKCS 7.

## <a name="members"></a>Membros

O objeto **EnvelopedData** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **EnvelopedData** tem esses métodos.



| Método                                   | Descrição                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Descriptografar**](envelopeddata-decrypt.md) | Descriptografa o conteúdo Envelopado.<br/>                                                                      |
| [**Encrypt**](envelopeddata-encrypt.md) | Criptografa o conteúdo, criptografa uma chave de sessão para cada destinatário e retorna o BLOB criptografado.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **EnvelopedData** tem essas propriedades.



| Propriedade                                                  | Tipo de acesso           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](envelopeddata-algorithm.md)<br/>   | Leitura/gravação<br/> | Algoritmo de criptografia e [*comprimento da chave*](../secgloss/k-gly.md).<br/>                                                                                                                                                                                                                                                                                                                              |
| [**Disputa**](envelopeddata-content.md)<br/>       | Leitura/gravação<br/> | O conteúdo de texto não criptografado de uma mensagem a ser envelopada. A definição dessa propriedade deve ser feita antes que o método [**Encrypt**](envelopeddata-encrypt.md) seja chamado.<br/> Quando o valor dessa propriedade é redefinido, direta ou indiretamente, o [*estado*](../secgloss/s-gly.md) inteiro do objeto é redefinido e qualquer conteúdo criptografado no objeto é perdido.<br/> Essa é a propriedade padrão.<br/> |
| [**Destinatários**](envelopeddata-recipients.md)<br/> | Somente leitura<br/>  | Coleção de objetos de [**certificado**](certificate.md) para receber a mensagem envelopada.<br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Comentários

O objeto **EnvelopedData** pode ser criado e é seguro para scripts. O ProgID do objeto **EnvelopedData** é CAPICOM. EnvelopedData. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
