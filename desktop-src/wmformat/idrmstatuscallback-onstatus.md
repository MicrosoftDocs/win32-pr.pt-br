---
title: Método OnStatus IDRMStatusCallback
description: O método OnStatus recebe mensagens de status de processos DRM assíncronos.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Método OnStatus Windows Media Format
- Método OnStatus Windows Media Format, interface IDRMStatusCallback
- IDRMStatusCallback interface formato Windows Media, método OnStatus
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c9f8c0424752ababe684b426d78001f2783d62db9781fe3d6a23ed002e91773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847450"
---
# <a name="idrmstatuscallbackonstatus-method"></a>Método IDRMStatusCallback:: OnStatus

O método **OnStatus** recebe mensagens de status de processos DRM assíncronos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Status* \[ do no\]
</dt> <dd>

Código de status. Os códigos de mensagem são definidos no tipo de enumeração **\_ status Msdrm** .

</dd> <dt>

*HR* \[ no\]
</dt> <dd>

Código de retorno que dá suporte à mensagem de status.

</dd> <dt>

*dwType* \[ no\]
</dt> <dd>

Tipo dos dados apontados *por era*. Defina como um dos valores da enumeração de [**\_ tipo de \_ dados attr do DRM**](drm-attr-datatype.md) .

</dd> <dt>

*valores* \[ no\]
</dt> <dd>

Ponteiro para dados relacionados à mensagem de status. O tipo de dados é determinado pelo valor do parâmetro *dwType* . Para obter mais informações, consulte a enumeração do [**\_ tipo de \_ dados attr do DRM**](drm-attr-datatype.md) .

</dd> <dt>

*pvContext* \[ no\]
</dt> <dd>

Parâmetro opcional que pode ser usado para identificar o objeto que enviou a mensagem. Ao definir *pvContext* quando você registra esse retorno de chamada, você pode usar o mesmo retorno de chamada para lidar com vários processos assíncronos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Nenhum.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tipo de \_ dados attr DRM**](drm-attr-datatype.md)
</dt> <dt>

[**Interface IDRMStatusCallback**](idrmstatuscallback.md)
</dt> </dl>

 

 





