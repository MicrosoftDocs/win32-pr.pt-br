---
title: Método IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: O método GetMachineCertificate recupera o certificado do computador do subsistema DRM no computador cliente.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Formato de mídia do Windows do método GetMachineCertificate
- Método GetMachineCertificate Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752156"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>Método IWMDRMSecurity:: GetMachineCertificate

O método **GetMachineCertificate** recupera o certificado do computador do subsistema DRM no computador cliente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwCertificateType* \[ no\]
</dt> <dd>

Tipo de certificado a recuperar. Defina como um dos valores na tabela a seguir.



| Valor                        | Descrição                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| \_Tipo de certificado WMDRM \_ \_ v1 | O certificado será recuperado no formato usado por componentes herdados.            |
| \_Tipo de certificado WMDRM \_ \_ v2 | O certificado será recuperado no formato usado pelos componentes do Windows Vista. |



 

</dd> <dt>

saída de *rgbVersion \[ 4 \]* \[\]
</dt> <dd>

Matriz de quatro bytes especificando a versão do subsistema DRM no computador cliente.

</dd> <dt>

*ppbCertificate* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para os dados do certificado. Defina como **NULL** para que o método forneça o tamanho do buffer necessário para manter o certificado em *pcbCertificate*.

</dd> <dt>

*pcbCertificate* \[ entrada, saída\]
</dt> <dd>

Tamanho do certificado em bytes. Se *ppbCertificate* for **NULL**, esse valor será definido como o tamanho do certificado. Se *ppbCertificate* não for **NULL**, esse valor deverá ser definido como o tamanho do buffer.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





