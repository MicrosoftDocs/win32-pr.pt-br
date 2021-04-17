---
title: Função WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: A função WMDRMCreateProtectedProvider cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- Formato de mídia do Windows da função WMDRMCreateProtectedProvider
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783778"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>Função WMDRMCreateProtectedProvider

A função **WMDRMCreateProtectedProvider** cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM do Windows Media. Essa função requer uma biblioteca de stub da Microsoft e cria objetos que dão suporte aos recursos protegidos do DRM.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
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



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções**](drm-functions.md)
</dt> <dt>

[**WMDRMCreateProvider**](wmdrmcreateprovider.md)
</dt> </dl>

 

 





