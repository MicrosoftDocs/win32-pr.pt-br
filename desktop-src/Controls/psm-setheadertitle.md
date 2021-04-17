---
title: Mensagem de PSM_SETHEADERTITLE (Prsht. h)
description: Define o texto do título do cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet SetHeaderTitle.
ms.assetid: 19d4badf-d99d-4a28-92d4-33bcf5d23944
keywords:
- Controles de PSM_SETHEADERTITLE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETHEADERTITLE
- PSM_SETHEADERTITLEA
- PSM_SETHEADERTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8140eef4aa09e9dd19d8baaf8193a836b105482e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811140"
---
# <a name="psm_setheadertitle-message"></a>Mensagem de PSM \_ SETHEADERTITLE

Define o texto do título do cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ SetHeaderTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadertitle) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da página do assistente.

</dd> <dt>

*lParam* 
</dt> <dd>

Novo subtítulo do cabeçalho.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se você especificar a página atual, ela será repintada imediatamente para exibir o novo título.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETHEADERTITLEW** (Unicode) e **PSM \_ SETHEADERTITLEA** (ANSI)<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HWNDTOINDEX de PSM \_**](psm-hwndtoindex.md)
</dt> <dt>

[**IDTOINDEX de PSM \_**](psm-idtoindex.md)
</dt> <dt>

[**PAGETOINDEX de PSM \_**](psm-pagetoindex.md)
</dt> </dl>

 

 





