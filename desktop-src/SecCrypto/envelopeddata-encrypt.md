---
description: Gera uma chave de sessão e criptografa os dados e os envelopes.
ms.assetid: 7ae0c908-207b-4a74-a195-d12e9e7dec76
title: Método EnvelopedData. Encrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df4741538ae11dbe1b158fd9b8e8a6c8632c427f9a0e8376e8cd10c9056461fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766077"
---
# <a name="envelopeddataencrypt-method"></a>Método EnvelopedData. Encrypt

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) no namespace [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

O método **Encrypt** gera uma chave de sessão, usa essa chave para criptografar o conteúdo, envelops o conteúdo criptografado para cada destinatário criptografando a chave de sessão com a chave pública de cada destinatário e, em seguida, retorna o [*blob*](../secgloss/b-gly.md) que contém o conteúdo criptografado e as chaves de sessão criptografadas como uma cadeia de caracteres codificada.

## <a name="syntax"></a>Sintaxe


```VB
EnvelopedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que indica o tipo de codificação usado para codificar os dados de envelope. O valor de codificação padrão é capicote Encoding \_ \_ base64. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um BLOB que contém os dados de envelope em uma cadeia de caracteres codificada.

## <a name="remarks"></a>Comentários

O BLOB retornado contém o conteúdo criptografado e uma chave de sessão criptografada para cada destinatário pretendido. Essas chaves de sessão são criptografadas usando a chave pública de cada destinatário. As chaves de sessão criptografadas podem ser descriptografadas somente com a chave privada de um destinatário.

Se a propriedade [**Recipients**](envelopeddata-recipients.md) não contiver nenhuma informação, esse método pesquisará o repositório de certificados catálogo do usuário atual em busca de possíveis destinatários. Se mais de um destinatário potencial for encontrado, será solicitado que o usuário selecione um destinatário em uma caixa de diálogo de seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | capicom 2,0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
