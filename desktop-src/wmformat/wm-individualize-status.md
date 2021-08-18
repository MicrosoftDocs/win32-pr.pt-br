---
title: WM_INDIVIDUALIZE_STATUS estrutura (Drmexternals.h)
description: A estrutura WM \_ INDIVIDUALIZE \_ STATUS registra o status do processo de individualização.
ms.assetid: 3779ed6f-c133-4a9d-b60c-ef8c41fcc4af
keywords:
- WM_INDIVIDUALIZE_STATUS formato de mídia do Windows
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
# <a name="wm_individualize_status-structure-drmexternalsh"></a>WM_INDIVIDUALIZE_STATUS estrutura (Drmexternals.h)

A **estrutura WM \_ INDIVIDUALIZE \_ STATUS** registra o status do processo [*de individualização.*](wmformat-glossary.md)

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

Valor do tipo [**de enumeração \_ DRM INDIVIDUALIZATION \_ STATUS.**](drm-individualization-status.md)

</dd> <dt>

**pszIndiRespUrl**
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em nulo que contém a URL de resposta de individualização.

</dd> <dt>

**dwHTTPRequest**
</dt> <dd>

**DWORD** que indica o número de viagens de ida e volta HTTP para o serviço de individualização que foram concluídas..

</dd> <dt>

**enHTTPStatus**
</dt> <dd>

Valor do tipo [**de enumeração \_ STATUS HTTP \_ DO DRM.**](drm-http-status.md)

</dd> <dt>

**dwHTTPReadProgress**
</dt> <dd>

**DWORD** que contém o número de bytes baixados até agora..

</dd> <dt>

**dwHTTPReadTotal**
</dt> <dd>

**DWORD** que contém o número total de bytes a serem baixados. Use esse valor e **dwHTTPReadProgress** para exibir uma interface do usuário que indica quanto do download foi concluído e quanto ainda deve ser feito.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é preenchida pelos componentes de tempo de run time do DRM e é enviada aos aplicativos no parâmetro *pValue* do método [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) quando o evento é igual a WMT \_ INDIVIDUALIZE. O aplicativo recebe esse evento várias vezes durante o processo de download.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | Windows SDK de Formato de Mídia 7 ou versões posteriores do SDK<br/>                       |
| Cabeçalho<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**STATUS \_ HTTP DO DRM \_**](drm-http-status.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





