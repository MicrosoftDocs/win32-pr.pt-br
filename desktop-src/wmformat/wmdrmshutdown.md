---
title: Função WMDRMShutdown (wmdrmsdk. h)
description: a função WMDRMShutdown libera recursos usados pelo Windows as APIs estendidas do cliente DRM de mídia.
ms.assetid: fa99a07a-2f07-464b-b7a2-e8f3110389b5
keywords:
- Formato de mídia do Windows da função WMDRMShutdown
topic_type:
- apiref
api_name:
- WMDRMShutdown
api_location:
- Wmdrmsdk.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f80f0f7264cd0962cb642f0877ccd044e777c3e9f269f87fcffc0037dcc0836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930357"
---
# <a name="wmdrmshutdown-function"></a>Função WMDRMShutdown

a função **WMDRMShutdown** libera recursos usados pelo Windows as APIs estendidas do cliente DRM de mídia.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE WMDRMShutdown(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Para evitar vazamentos de memória, você deve chamar essa função para cada chamada da função [**WMDRMStartup**](wmdrmstartup.md) .

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

 

 





