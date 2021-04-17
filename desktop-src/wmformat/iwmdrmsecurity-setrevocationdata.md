---
title: Método IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: O método SetRevocationData define uma lista de certificados revogados no repositório local.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Formato de mídia do Windows do método SetRevocationData
- Método SetRevocationData Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754693"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a>Método IWMDRMSecurity:: SetRevocationData

O método **SetRevocationData** define uma lista de certificados revogados no repositório local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*f \_ guidRevocationType* \[ em\]
</dt> <dd>

GUID que especifica o tipo de lista de revogação. Defina como uma das constantes na tabela a seguir.



| Constante de GUID                 | Descrição                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_aplicativo WMDRM RErevocationtype \_    | Especifica a lista de certificados revogados do aplicativo.                           |
| \_dispositivo WMDRM RErevocationtype \_ | Especifica a lista de certificados revogados do dispositivo.                                |
| WMDRM \_ RErevocationtype \_ CARDEA | Especifica a lista de revogação de certificados do Windows Media DRM para dispositivos de rede. |



 

</dd> <dt>

*f \_ pbCRL* \[ em\]
</dt> <dd>

Buffer que contém a lista de certificados revogados.

</dd> <dt>

*f \_ cbCRL* \[ em\]
</dt> <dd>

Tamanho do buffer, em bytes.

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

[**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





