---
title: Mensagem de PSM_SETHEADERSUBTITLE (Prsht. h)
description: Define o texto do subtítulo para o cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a \_ macro PropSheet SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- controles de Windows de mensagem de PSM_SETHEADERSUBTITLE
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e030b75a933ba7f647f8b3dffa5e45637999d45f3299f8280fd1db3afb9857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088496"
---
# <a name="psm_setheadersubtitle-message"></a>Mensagem de PSM \_ SETHEADERSUBTITLE

Define o texto do subtítulo para o cabeçalho da página interior de um assistente. Você pode enviar essa mensagem explicitamente ou usar a macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .

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

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Se você especificar a página atual, ela será repintada imediatamente para exibir o novo subtítulo.

> [!Note]  
> Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Prsht. h</dt> </dl>      |
| Nomes Unicode e ANSI<br/>   | **PSM \_ SETHEADERSUBTITLEW** (Unicode) e **PSM \_ SETHEADERSUBTITLEA** (ANSI)<br/> |



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

 

 





