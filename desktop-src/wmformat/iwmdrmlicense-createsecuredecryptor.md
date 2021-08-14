---
title: Método CreateSecureDecryptor IWMDRMLicense (Wmdrmsdk.h)
description: O método CreateSecureDecryptor cria um objeto descriptografador seguro. O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o de acordo com as configurações especificadas nos parâmetros desse método.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Formato de mídia do windows do método CreateSecureDecryptor
- Formato de mídia do windows do método CreateSecureDecryptor, interface IWMDRMLicense
- Formato de mídia da interface IWMDRMLicense, método CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96c562dcafd72a72ecef340688fd709ecbe5446abae53403d403c9a70bdd6f2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433665"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>Método IWMDRMLicense::CreateSecureDecryptor

O **método CreateSecureDecryptor** cria um objeto descriptografador seguro. O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o de acordo com as configurações especificadas nos parâmetros desse método.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbCertificate* \[ Em\]
</dt> <dd>

Certificado do aplicativo de chamada.

</dd> <dt>

*cbCertificate* \[ Em\]
</dt> <dd>

Tamanho do certificado em bytes.

</dd> <dt>

*dwCertificateType* \[ Em\]
</dt> <dd>

O tipo de certificado. Definido como XML DE TIPO DE \_ CERTIFICADO WMDRM. \_ \_

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

O tipo de proteção de sessão a ser usado para codificação. Deve ser definido como uma das constantes na tabela a seguir:



| Constante                     | Descrição                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| TIPO DE \_ PROTEÇÃO WMDRM \_ \_ RC4 | Usa a criptografia RC4 para criptografia de sessão. Essa é a única proteção de sessão com suporte para esta versão. |



 

</dd> <dt>

*pbInitializationVector* \[ out\]
</dt> <dd>

Recebe o vetor de inicialização. O vetor de inicialização é criptografado por RSA usando o esquema de preenchimento OAEP com a chave pública RSA encontrada no certificado. Definido como **NULL** para receber o tamanho do buffer necessário em *pcbInitializationVector*.

</dd> <dt>

*pcbInitializationVector* \[ in, out\]
</dt> <dd>

Na entrada, o tamanho do buffer passado como *pbInitializationVector*. Na saída, o tamanho da parte usada do buffer. Se você passar **NULL** para *pbInitializationVector,* esse valor será definido como o tamanho do buffer necessário na saída.

</dd> <dt>

*ppDecryptor* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto recém-criado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMLicense Interface**](iwmdrmlicense.md)
</dt> </dl>

 

 





