---
title: Método IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: O método CreateSecureDecryptor cria um objeto de descriptografia seguro. O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o novamente de acordo com as configurações especificadas nos parâmetros desse método.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Formato de mídia do Windows do método CreateSecureDecryptor
- Método CreateSecureDecryptor Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows de interface IWMDRMLicense, método CreateSecureDecryptor
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
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762410"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a>Método IWMDRMLicense:: CreateSecureDecryptor

O método **CreateSecureDecryptor** cria um objeto de descriptografia seguro. O descriptografador seguro difere do descriptografador normal, pois ele descriptografa o conteúdo e, em seguida, criptografa-o novamente de acordo com as configurações especificadas nos parâmetros desse método.

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

*pbCertificate* \[ no\]
</dt> <dd>

Certificado do aplicativo de chamada.

</dd> <dt>

*cbCertificate* \[ no\]
</dt> <dd>

Tamanho do certificado em bytes.

</dd> <dt>

*dwCertificateType* \[ no\]
</dt> <dd>

O tipo de certificado. Defina como \_ XML do tipo de certificado WMDRM \_ \_ .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

O tipo de proteção de sessão a ser usado para nova codificação. Deve ser definido como uma das constantes na tabela a seguir:



| Constante                     | Descrição                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| \_Tipo de proteção WMDRM \_ \_ RC4 | Usa a criptografia RC4 para criptografia de sessão. Esta é a única proteção de sessão com suporte para esta versão. |



 

</dd> <dt>

*pbInitializationVector* \[ fora\]
</dt> <dd>

Recebe o vetor de inicialização. O vetor de inicialização é o RSA Encrypted usando o esquema de preenchimento OAEP com a chave pública RSA encontrada no certificado. Defina como **NULL** para receber o tamanho de buffer necessário em *pcbInitializationVector*.

</dd> <dt>

*pcbInitializationVector* \[ entrada, saída\]
</dt> <dd>

Na entrada, o tamanho do buffer passado como *pbInitializationVector*. Na saída, o tamanho da parte usada do buffer. Se você passar **NULL** para *pbInitializationVector*, esse valor será definido como o tamanho de buffer necessário na saída.

</dd> <dt>

*ppDecryptor* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) do objeto recém-criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





