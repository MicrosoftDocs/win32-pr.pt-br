---
title: Método IWMDRMLicenseManagement StoreLicense (wmdrmsdk. h)
description: O método StoreLicense inclui uma licença que foi gerada fora do subsistema DRM local no repositório de licenças local.
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- Formato de mídia do Windows do método StoreLicense
- Método StoreLicense Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método StoreLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c509fdbc89acfd2d31ad5ead7ce63cd7f3b501b304d82240475c845c013e03b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117655044"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a>Método IWMDRMLicenseManagement:: StoreLicense

O método **StoreLicense** inclui uma licença que foi gerada fora do subsistema DRM local no repositório de licenças local.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrLicenseResponse* \[ no\]
</dt> <dd>

Cadeia de caracteres de resposta de licença a ser decodificada e adicionada ao repositório de licenças local.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Você pode usar esse método para adicionar licenças do XMR que você criou ao armazenamento de licença local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





