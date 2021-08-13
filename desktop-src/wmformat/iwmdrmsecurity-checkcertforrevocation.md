---
title: Método IWMDRMSecurity CheckCertForRevocation (Wmdrmsdk.h)
description: O método CheckCertForRevocation determina se um certificado foi revogado.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Formato de mídia do método CheckCertForRevocation
- Método CheckCertForRevocation windows Formato de mídia, interface IWMDRMSecurity
- Formato de mídia da interface IWMDRMSecurity , método CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e090dfb655837ad2cf36cf45486488fde1440b499b73f16fdfbdaf2989532687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700782"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>Método IWMDRMSecurity::CheckCertForRevocation

O **método CheckCertForRevocation** determina se um certificado foi revogado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rguidRevocationList* \[ Em\]
</dt> <dd>

GUID que identifica a lista de revogação a ser usada. De definido como um dos valores na tabela a seguir.



| Constante GUID                 | Descrição                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| APLICATIVO WMDRM \_ \_ REVOCATIONTYPE    | Especifica a lista de certificados revogados do aplicativo.                                     |
| DISPOSITIVO WMDRM \_ \_ REVOCATIONTYPE | Especifica a lista de certificados revogados do dispositivo.                                          |
| WMDRM \_ REVOCATIONTYPE \_ LTD | Especifica a lista de certificados Windows DRM de Mídia para Dispositivos de Rede. |



 

</dd> <dt>

*pbCert* \[ Em\]
</dt> <dd>

Buffer que contém o certificado a ser procurar.

</dd> <dt>

*cbCert* \[ Em\]
</dt> <dd>

Tamanho do buffer *pbCert*, em bytes.

</dd> <dt>

*fRevoked* \[ out\]
</dt> <dd>

Na saída, indica se o certificado está presente na lista de revogação.

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

 

 





