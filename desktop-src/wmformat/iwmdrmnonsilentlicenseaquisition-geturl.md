---
title: Método GetURL IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: O método GetURL recupera a URL para a qual o desafio de licença deve ser lançado.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Método GetURL Windows Media Format
- Método GetURL Windows Media Format, interface IWMDRMNonSilentLicenseAquisition
- Formato de mídia do Windows da interface IWMDRMNonSilentLicenseAquisition, método GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779504"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>Método IWMDRMNonSilentLicenseAquisition:: GetURL

O método **getURL** recupera a URL para a qual o desafio de licença deve ser lançado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrURL* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe a URL.

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
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





