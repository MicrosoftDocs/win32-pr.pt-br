---
title: Método IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: O método CheckCertForRevocation determina se um certificado foi revogado.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Formato de mídia do Windows do método CheckCertForRevocation
- Método CheckCertForRevocation Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método CheckCertForRevocation
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
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752558"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a>Método IWMDRMSecurity:: CheckCertForRevocation

O método **CheckCertForRevocation** determina se um certificado foi revogado.

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

*rguidRevocationList* \[ no\]
</dt> <dd>

GUID que identifica a lista de revogação a ser usada. Defina como um dos valores na tabela a seguir.



| Constante de GUID                 | Descrição                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| \_aplicativo WMDRM RErevocationtype \_    | Especifica a lista de certificados revogados do aplicativo.                                     |
| \_dispositivo WMDRM RErevocationtype \_ | Especifica a lista de certificados revogados do dispositivo.                                          |
| WMDRM \_ RErevocationtype \_ CARDEA | Especifica a lista de revogação de certificados do Microsoft Windows Media DRM para dispositivos de rede. |



 

</dd> <dt>

*pbCert* \[ no\]
</dt> <dd>

Buffer que contém o certificado a ser pesquisado.

</dd> <dt>

*cbCert* \[ no\]
</dt> <dd>

Tamanho do buffer *pbCert*, em bytes.

</dd> <dt>

*fRevoked* \[ fora\]
</dt> <dd>

Na saída, indica se o certificado está presente na lista de revogação.

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

 

 





