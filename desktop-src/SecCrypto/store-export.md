---
description: Copia o conteúdo de um repositório de certificados aberto para uma cadeia de caracteres codificada.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Método Store. Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753212"
---
# <a name="storeexport-method"></a>Método Store. Export

\[O método de **exportação** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Em vez disso, use a [**classe X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) no namespace [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

O método de **exportação** copia o conteúdo de um [*repositório de certificados*](../secgloss/c-gly.md) aberto para uma cadeia de caracteres codificada.

## <a name="syntax"></a>Sintaxe


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Salvar como* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [de \_ \_ tipo salvar \_ como \_ do armazenamento capicor](capicom-store-save-as-type.md) que indica o formato da operação de exportação. O valor padrão é capicote \_ Store \_ Save \_ as \_ serializado. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                     | Significado                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <dt>**capicote \_ Store \_ Save \_ as \_ serializado**</dt> </dl> | O repositório é salvo no formato serializado.<br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <dt>**Capicote \_ Store \_ Save \_ as \_ PKCS7**</dt> </dl>                | O repositório é salvo no \# formato PKCS 7.<br/>   |



 

</dd> <dt>

*EncodingType* \[ em, opcional\]
</dt> <dd>

Um valor da enumeração [do \_ \_ tipo de codificação capicor](capicom-encoding-type.md) que indica o tipo de codificação do repositório exportado. O valor padrão é CAPICOM de \_ codificação \_ base64. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                  | Significado                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ codificar \_ qualquer**</dt> </dl>          | Esse tipo de codificação é usado somente quando os dados de entrada têm um tipo de codificação desconhecido. Se esse valor for usado para especificar o tipo de codificação da saída, o CAPICOM de codificação \_ \_ Base64 será usado em seu lugar. Introduzido no CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ codificar \_ Base64**</dt> </dl> | Os dados são salvos como uma cadeia de caracteres codificada em base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**capicote de \_ codificação \_ binário**</dt> </dl> | Os dados são salvos como uma sequência binária pura.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna uma cadeia de caracteres que contém os certificados no repositório no formulário de codificação especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Repositório**](store.md)
</dt> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 
