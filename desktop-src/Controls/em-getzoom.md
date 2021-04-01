---
title: Mensagem de EM_GETZOOM (RichEdit. h)
description: Obtém a taxa de zoom atual. O ração de zoom sempre está entre 1/64 e 64. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: d4a1daee-4af7-44d1-80d6-0fcaaf3672a8
keywords:
- Controles de EM_GETZOOM de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a88aa96787e1fda5cdeb8f77f478a4d51635cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644348"
---
# <a name="em_getzoom-message"></a>\_Mensagem em GETzoom

Obtém a taxa de zoom atual para um controle de edição de várias linhas ou um controle de edição rico. O ração de zoom sempre está entre 1/64 e 64.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Recebe o numerador da taxa de zoom.

</dd> <dt>

*lParam* 
</dt> <dd>

Recebe o denominador da taxa de zoom.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A mensagem retornará **true** se a mensagem for processada, que será se *wParam* e *lParam* não forem **nulos**.

## <a name="remarks"></a>Comentários

**Editar:** Com suporte no Windows 10 1809 e posterior. O controle de edição precisa ter o estilo estendido de **s \_ ex \_ zoom** definido, para que essa mensagem tenha um efeito, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md). Para obter informações sobre o controle de edição, consulte [Editar controles](edit-controls.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| Redistribuível<br/>          | Edição avançada 3,0<br/>                                                              |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h/commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ SETzoom**](em-setzoom.md)
</dt> </dl>

 

 





