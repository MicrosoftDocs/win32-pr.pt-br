---
title: Método IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: O método SetActionAllowedQueryParams define informações específicas do ambiente para obter resultados de consulta mais precisos ao usar o método QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Formato de mídia do Windows do método SetActionAllowedQueryParams
- Método SetActionAllowedQueryParams Windows Media Format, interface IWMDRMLicenseQuery
- Formato de mídia do Windows de interface IWMDRMLicenseQuery, método SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812792"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a>Método IWMDRMLicenseQuery:: SetActionAllowedQueryParams

O método **SetActionAllowedQueryParams** define informações específicas do ambiente para obter resultados de consulta mais precisos ao usar o método [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fIsMF* \[ no\]
</dt> <dd>

Especifica se o conteúdo será renderizado usando os objetos do SDK do Microsoft Media Foundation. **False** indica a renderização pelos objetos do SDK do Windows Media Format. Esse parâmetro é opcional.

</dd> <dt>

*dwAppSecLevel* \[ no\]
</dt> <dd>

Nível de segurança do aplicativo de consulta. Esse valor só será importante se os objetos do Windows Media Format SDK forem usados, caso em que *fIsMF* deve ser definido como **false**. Esse parâmetro é opcional.

</dd> <dt>

*fHasSerialNumber* \[ no\]
</dt> <dd>

Especifica se o dispositivo de destino para uma operação de cópia tem um número de série. Esse parâmetro é opcional e só se aplica a consultas para operações de cópia.

</dd> <dt>

*bstrDeviceCert* \[ no\]
</dt> <dd>

Certificado de dispositivo do dispositivo de destino ao usar o DRM do Windows Media para dispositivos portáteis. Esse parâmetro é opcional e só se aplica a consultas para operações de cópia.

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

[**Interface IWMDRMLicenseQuery**](iwmdrmlicensequery.md)
</dt> <dt>

[**Consultando informações detalhadas sobre direitos**](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





