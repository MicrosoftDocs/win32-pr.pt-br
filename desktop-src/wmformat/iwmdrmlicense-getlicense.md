---
title: Método GetLicense do IWMDRMLicense (wmdrmsdk. h)
description: O método GetLicense recupera a licença como dados XML ou XMR.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Método GetLicense Windows Media Format
- Método GetLicense Windows Media Format, interface IWMDRMLicense
- Formato de mídia do Windows da interface IWMDRMLicense, método GetLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773063"
---
# <a name="iwmdrmlicensegetlicense-method"></a>Método IWMDRMLicense:: GetLicense

O método **GetLicense** recupera a licença como dados XML ou XMR.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppbLicense* \[ fora\]
</dt> <dd>

Recebe a licença.

</dd> <dt>

*pcbLicense* \[ fora\]
</dt> <dd>

Recebe o tamanho da licença.

</dd> <dt>

*pdwLicenseType* \[ fora\]
</dt> <dd>

Recebe o tipo da licença retornada. Esse valor é definido como uma das constantes na tabela a seguir.



| Constante                  | Descrição                            |
|---------------------------|----------------------------------------|
| tipo de licença do WMDRM \_ \_ \_ XML | A licença recuperada é formatada como XML. |
| \_XMR do \_ tipo de licença WMDRM \_ | A licença recuperada é formatada como XMR. |



 

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

[**Getlicenciadoproperty**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





