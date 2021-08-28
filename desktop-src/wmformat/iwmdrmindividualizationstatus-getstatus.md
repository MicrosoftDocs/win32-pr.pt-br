---
title: Método GetStatus IWMDRMIndividualizationStatus (wmdrmsdk. h)
description: O método GetStatus recupera informações detalhadas sobre o progresso de individualização.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Método GetStatus Windows Media Format
- Método GetStatus Windows Media Format, interface IWMDRMIndividualizationStatus
- Formato de mídia do Windows da interface IWMDRMIndividualizationStatus, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b5408a71dcbedc98ccfdd70517cdae086620a05d8f648fcb327a608a2612bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701617"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a>Método IWMDRMIndividualizationStatus:: GetStatus

O método **GetStatus** recupera informações detalhadas sobre o progresso de individualização.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pStatus* \[ fora\]
</dt> <dd>

Recebe uma estrutura de [**\_ \_ status de individualização do WM**](drmwm-individualize-status.md) que contém informações detalhadas sobre o status da tentativa de individualização.

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

[**Interface IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





