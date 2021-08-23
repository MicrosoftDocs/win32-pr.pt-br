---
title: WM_INDIVIDUALIZE_STATUS estrutura (Wmdrmsdk.h)
description: A estrutura WM \_ INDIVIDUALIZE \_ STATUS contém informações sobre um processo de individualização pendente.
ms.assetid: af7e8758-489b-461f-b241-d7e40c8d61da
keywords:
- WM_INDIVIDUALIZE_STATUS formato de mídia do Windows
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
ms.openlocfilehash: c139631fe737e07d011e43920ab63c7394f03c3319abb2f7936153ae06c596ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708296"
---
# <a name="wm_individualize_status-structure-wmdrmsdkh"></a>WM_INDIVIDUALIZE_STATUS estrutura (Wmdrmsdk.h)

A **estrutura WM \_ INDIVIDUALIZE \_ STATUS** contém informações sobre um processo de individualização pendente.

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

**Código de retorno HRESULT.**

</dd> <dt>

**enIndiStatus**
</dt> <dd>

Valor do tipo [**de enumeração \_ STATUS DE \_ INDIVIDUALIZAÇÃO**](drmdrm-individualization-status.md) DO DRM que indica o status atual do processo de individualização.

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

Valor do tipo [**de enumeração \_ STATUS HTTP \_ DO DRM.**](drmdrm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

O número de bytes baixados.

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

O número total de bytes a serem baixados. Você pode usar esse valor e **dwHTTPReadProgress** para exibir uma interface do usuário que indica quanto do download foi concluído e quanto ainda deve ser feito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recebida quando você chama o [**método IWMDRMIndividualizationStatus::GetStatus.**](iwmdrmindividualizationstatus-getstatus.md) Ele contém o status do processo de individualização pendente no momento da chamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





