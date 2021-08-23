---
title: Método GetChallenge IWMDRMNonSilentLicenseAquisition (Wmdrmsdk.h)
description: O método GetChallenge recupera o desafio de licença que deve ser postado no servidor de licença.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Formato de mídia do windows do método GetChallenge
- Formato de mídia do windows do método GetChallenge, interface IWMDRMNonSilentLicenseAquisition
- IWMDRMNonSilentLicenseNãosition interface windows Formato de mídia , método GetChallenge
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
ms.openlocfilehash: cf495652033bdb5201f2b4e5bd9dc1d6a222cc3ebdf4ec6438fe391ed06fac85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027514"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>Método IWMDRMNonSilentLicenseAquisition::GetChallenge

O **método GetChallenge** recupera o desafio de licença que deve ser postado no servidor de licença.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbstrChallenge* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe o desafio de licença.

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
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWMDRMNonSilentLicenseAquisition Interface**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





