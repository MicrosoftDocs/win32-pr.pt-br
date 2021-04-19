---
description: Copia um certificado para uma cadeia de caracteres codificada.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'Método ICertificate2:: Export'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756686"
---
# <a name="icertificate2export-method"></a>Método ICertificate2:: Export

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use a [**classe X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método **Export** copia um certificado para uma cadeia de caracteres codificada. A cadeia de caracteres codificada pode ser gravada em um arquivo ou importada para um novo objeto de [**certificado**](certificate.md) .

## <a name="syntax"></a>Sintaxe


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [**do \_ \_ tipo de codificação capicor**](capicom-encoding-type.md) que especifica o tipo de codificação para a operação de exportação. O valor padrão é **CAPICOM de \_ codificação \_ Base64**. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Uma cadeia de caracteres que contém o certificado exportado no formulário de codificação especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte do servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de criptografia](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
