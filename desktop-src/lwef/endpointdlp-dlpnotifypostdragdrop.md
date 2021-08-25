---
description: Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.
title: Função DlpNotifyPostDragDrop (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreDragDrop
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 3d20f9356007973b580d136aef1a74b8206026bf62fe14c5db46eb2cc0cbf1f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062106"
---
# <a name="dlpnotifypostdragdrop-function"></a>Função DlpNotifyPostDragDrop

Fornece ao sistema informações sobre um documento após a conclusão de uma operação de arrastar e soltar.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de arrastar e soltar.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ Em\]
</dt> <dd>

Um ponteiro para uma [estrutura DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a queda de arrastar.

</dd> </dl>


## <a name="return-value"></a>Valor retornado

Retornar nulo.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |