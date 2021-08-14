---
title: Estrutura de WM_INDIVIDUALIZE_STATUS (Drmexternals. h)
description: A \_ estrutura de status de individualização do WM \_ registra o status do processo de individualização.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- Formato de mídia do Windows de estrutura de WM_INDIVIDUALIZE_STATUS
topic_type:
- apiref
api_name:
- WM_INDIVIDUALIZE_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb083c2a90a791099f6438f2911ac9735ecd4dada9118811aa0ff581a8db37ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699016"
---
# <a name="wm_individualize_status-structure-drmexternalsh"></a>Estrutura de WM_INDIVIDUALIZE_STATUS (Drmexternals. h)

A estrutura de **\_ \_ status de individualização do WM** registra o status do processo de [*individualização*](wmformat-glossary.md) .

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

Valor do tipo de enumeração de [**\_ \_ status de individualização de DRM**](drm-individualization-status.md) .

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém a URL de resposta de individualização.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD** que indica o número de viagens de ida e volta http para o serviço de individualização que foram concluídas.

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor do tipo de enumeração de [**\_ \_ status http DRM**](drm-http-status.md) .

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** que contém o número de bytes baixados até agora..

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** que contém o número total de bytes a serem baixados. Use esse valor e **dwHTTPReadProgress** para exibir uma interface do usuário que indica a quantidade de download concluído e quanto resta ser feito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é preenchida pelos componentes de tempo de execução do DRM e é enviada para aplicativos no *parâmetro época* do método Applications [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) quando o evento é igual a WMT \_ individualize. O aplicativo recebe esse evento várias vezes durante o processo de download.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | Windows SDK do Media Format 7 ou versões posteriores do SDK<br/>                       |
| parâmetro<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_status do http DRM \_**](drm-http-status.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





