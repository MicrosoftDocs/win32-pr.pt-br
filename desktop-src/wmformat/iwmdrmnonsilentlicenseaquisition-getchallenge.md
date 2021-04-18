---
title: Método getchallenge IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: O método getchallenge recupera o desafio de licença que deve ser postado no servidor de licença.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Método getchallenge formato de mídia do Windows
- Método getchallenge Windows Media Format, interface IWMDRMNonSilentLicenseAquisition
- IWMDRMNonSilentLicenseAquisition interface formato Windows Media, método getchallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789912"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>Método IWMDRMNonSilentLicenseAquisition:: getchallenge

O método **getchallenge** recupera o desafio de licença que deve ser postado no servidor de licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrChallenge* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe o desafio de licença.

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

 

 





