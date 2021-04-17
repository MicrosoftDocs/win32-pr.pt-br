---
title: Função WMDRMCreateProvider (wmdrmsdk. h)
description: A função WMDRMCreateProvider cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- Formato de mídia do Windows da função WMDRMCreateProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771310"
---
# <a name="wmdrmcreateprovider-function"></a>Função WMDRMCreateProvider

A função **WMDRMCreateProvider** cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media. Essa função não requer uma biblioteca de stub da Microsoft e cria objetos que não dão suporte aos recursos protegidos do DRM.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppDRMProvider* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IWMDRMProvider**](iwmdrmprovider.md) do objeto recém-criado.

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
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





