---
title: Estrutura de WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)
description: A \_ estrutura de status de individualização do WM \_ contém informações sobre um processo de individualização pendente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- Formato de mídia do Windows de estrutura de WM_INDIVIDUALIZE_STATUS
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef7617fe6dcddf3397ab1a123132e843f0b1461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788997"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>Estrutura de WM_INDIVIDUALIZE_STATUS (wmdrmsdk. h)

A estrutura de **\_ \_ status de individualização do WM** contém informações sobre um processo de individualização pendente.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WMIndividualizeStatus {
  HRESULT                      hr;
  DRM_INDIVIDUALIZATION_STATUS enIndiStatus;
  LPSTR                        pszIndiRespUrl;
  DWORD                        dwHTTPRequest;
  DRM_HTTP_STATUS              enHTTPStatus;
  DWORD                        dwHTTPReadProgress;
  DWORD                        dwHTTPReadTotal;
} WM_INDIVIDUALIZE_STATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**h**
</dt> <dd>

Código de retorno **HRESULT** .

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valor do tipo de enumeração de [**\_ \_ status de individualização de DRM**](drmdrm-individualization-status.md) que indica o status atual do processo de individualização.

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém a URL de resposta de individualização.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

O número de viagens de ida e volta HTTP para o serviço de individualização que foram concluídas.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor do tipo de enumeração de [**\_ \_ status http DRM**](drmdrm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

O número de bytes baixados.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

O número total de bytes a serem baixados. Você pode usar esse valor e **dwHTTPReadProgress** para exibir uma interface do usuário que indica a quantidade de download concluída e quanto resta.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recebida quando você chama o método [**IWMDRMIndividualizationStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md) . Ele contém o status do processo de individualização pendente no momento da chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





