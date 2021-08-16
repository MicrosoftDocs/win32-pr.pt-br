---
description: Enviado para uma DLL de extensão quando o Gerenciador de Arquivos está descarregando a DLL.
title: FMEVENT_UNLOAD mensagem (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_UNLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 15ffcd46-602f-4ad0-9c58-0b8056b9cac4
ms.openlocfilehash: 5d18d72a43ac1fca6906bb1e3f7a14468dbd02933d801dc3c20e2a933bc18f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860361"
---
# <a name="fmevent_unload-message"></a>Mensagem UNLOAD \_ FMEVENT

Enviado para uma DLL de extensão quando o Gerenciador de Arquivos está descarregando a DLL.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Uma DLL de extensão deverá retornar zero se ela processa essa mensagem.

## <a name="remarks"></a>Comentários

Os *valores hwnd* e **hMenu** passados com as mensagens [**FMEVENT \_ LOAD**](fmevent-load.md) e [**FMEVENT \_ INITMENU**](fmevent-initmenu.md) podem não ser válidos no momento em que essa mensagem é enviada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




