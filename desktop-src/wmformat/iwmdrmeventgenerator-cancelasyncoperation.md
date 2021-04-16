---
title: Método IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: O método CancelAsyncOperation cancela uma operação assíncrona.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Formato de mídia do Windows do método CancelAsyncOperation
- Método CancelAsyncOperation Windows Media Format, interface IWMDRMEventGenerator
- Formato de mídia do Windows de interface IWMDRMEventGenerator, método CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750983"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a>Método IWMDRMEventGenerator:: CancelAsyncOperation

O método **CancelAsyncOperation** cancela uma operação assíncrona.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*punkCancelationCookie* \[ no\]
</dt> <dd>

Ponteiro para o cookie de cancelamento que identifica a operação assíncrona a ser cancelada. Esse cookie é fornecido pelo método usado para iniciar a operação.

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

[**Interface IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





