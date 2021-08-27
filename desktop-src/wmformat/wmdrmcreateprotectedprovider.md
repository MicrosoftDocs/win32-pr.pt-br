---
title: Função WMDRMCreateProtectedProvider (wmdrmsdk. h)
description: a função WMDRMCreateProtectedProvider cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM de mídia Windows.
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
ms.openlocfilehash: f4b5d71ff1deed01cc10d7342286b443b9f64b1a1c192af575a599a2fc8d8c9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026924"
---
# <a name="wmdrmcreateprotectedprovider-function"></a>Função WMDRMCreateProtectedProvider

a função **WMDRMCreateProtectedProvider** cria uma fábrica de classes que pode criar os outros objetos das APIs estendidas do cliente DRM de mídia Windows. Essa função requer uma biblioteca de stub da Microsoft e cria objetos que dão suporte aos recursos protegidos do DRM.

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

## <a name="return-value"></a>Valor retornado

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

 

 





