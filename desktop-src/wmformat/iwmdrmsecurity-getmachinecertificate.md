---
title: Método GetMachineCertificate de IWMDRMSecurity (Wmdrmsdk.h)
description: O método GetMachineCertificate recupera o certificado do computador do subsistema DRM no computador cliente.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Formato de mídia do windows do método GetMachineCertificate
- Método GetMachineCertificate windows Formato de Mídia, interface IWMDRMSecurity
- Formato de mídia da interface IWMDRMSecurity , método GetMachineCertificate
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
ms.openlocfilehash: 4fd85a3b74ee28e5faa8df5fc264d50366803f4073ec97a36920577d417e4f97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084693"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a>Método IWMDRMSecurity::GetMachineCertificate

O **método GetMachineCertificate** recupera o certificado do computador do subsistema DRM no computador cliente.

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

*dwCertificateType* \[ Em\]
</dt> <dd>

Tipo de certificado a ser recuperado. De definido como um dos valores na tabela a seguir.



| Valor                        | Descrição                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| TIPO DE CERTIFICADO WMDRM \_ \_ \_ V1 | O certificado será recuperado no formato usado pelos componentes herdados.            |
| TIPO DE CERTIFICADO WMDRM \_ \_ \_ V2 | O certificado será recuperado no formato usado pelos componentes Windows Vista. |



 

</dd> <dt>

*rgbVersion \[ 4 \]* \[ out\]
</dt> <dd>

Matriz de quatro bytes especificando a versão do subsistema DRM no computador cliente.

</dd> <dt>

*ppbCertificate* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para os dados do certificado. Definido como **NULL** para que o método forneça o tamanho do buffer necessário para manter o certificado em *pcbCertificate*.

</dd> <dt>

*pcbCertificate* \[ in, out\]
</dt> <dd>

Tamanho do certificado em bytes. Se *ppbCertificate* for **NULL,** esse valor será definido como o tamanho do certificado. Se *ppbCertificate* não for **NULL,** esse valor deverá ser definido como o tamanho do buffer.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMSecurity Interface**](iwmdrmsecurity.md)
</dt> </dl>

 

 





