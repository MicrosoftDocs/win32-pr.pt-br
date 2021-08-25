---
title: Método IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: O método GetRevocationData recupera uma lista de certificados revogados do repositório local.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Formato de mídia do Windows do método GetRevocationData
- Método GetRevocationData Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5035bc94051c61baaef7bcf474b4d6ebb4413b549dfff038bae7105f32d087b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808476"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a>Método IWMDRMSecurity:: GetRevocationData

O método **GetRevocationData** recupera uma lista de certificados revogados do repositório local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*f \_ guidRevocationType* \[ em\]
</dt> <dd>

GUID que identifica o tipo de lista de revogação a ser recuperada. Use uma das constantes na tabela a seguir.



| Constante de GUID                 | Descrição                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| \_aplicativo WMDRM RErevocationtype \_    | Especifica a lista de certificados revogados do aplicativo.                           |
| \_dispositivo WMDRM RErevocationtype \_ | Especifica a lista de certificados revogados do dispositivo.                                |
| WMDRM \_ RErevocationtype \_ CARDEA | especifica o Windows Media DRM para a lista de certificados revogados de dispositivos de rede. |



 

</dd> <dt>

saída de *f \_ pbCRL* \[\]
</dt> <dd>

Buffer que recebe a lista de revogação. Defina como **NULL** para obter o tamanho de buffer necessário.

</dd> <dt>

*f \_ pcbCRL* \[ in, out\]
</dt> <dd>

O tamanho do buffer em bytes. Se *f \_ PbCRL* for **NULL**, esse valor será definido como o tamanho de buffer necessário na saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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

[**Revogação e renovação de componentes automatizados**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





