---
title: Função WMDRMStartup (wmdrmsdk. h)
description: A função WMDRMStartup Inicializa os recursos usados pelas APIs estendidas do cliente DRM do Windows Media.
ms.assetid: 2fd26bcc-8106-4356-933a-d4cf3536f4fb
keywords:
- Formato de mídia do Windows da função WMDRMStartup
topic_type:
- apiref
api_name:
- WMDRMStartup
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c152a5160750f3c1943b455a8877b4615781b6ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752324"
---
# <a name="wmdrmstartup-function"></a>Função WMDRMStartup

A função **WMDRMStartup** Inicializa os recursos usados pelas APIs estendidas do cliente DRM do Windows Media.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMStartup(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Para cada chamada dessa função, você deve chamar [**WMDRMShutdown**](wmdrmshutdown.md) para liberar os recursos usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Wmdrmsdk.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Funções**](drm-functions.md)
</dt> </dl>

 

 





