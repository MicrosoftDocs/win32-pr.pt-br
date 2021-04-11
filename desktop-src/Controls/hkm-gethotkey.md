---
title: Mensagem de HKM_GETHOTKEY (commctrl. h)
description: Obtém o código de chave virtual e os sinalizadores de modificador de uma tecla de acesso de um controle de tecla de atalho.
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- Controles de HKM_GETHOTKEY de mensagens do Windows
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455014"
---
# <a name="hkm_gethotkey-message"></a>\_Mensagem hkm GETtecla de atalho

Obtém o código de chave virtual e os sinalizadores de modificador de uma tecla de acesso de um controle de tecla de atalho.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o código de chave virtual e os sinalizadores de modificador. O [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) do [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é o código de chave virtual da tecla de atalho. O [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de **LOWORD** é o modificador de chave que especifica as chaves que definem uma combinação de teclas de acesso. Os sinalizadores de modificadores podem ser uma combinação dos valores a seguir.



| Valor            | Significado      |
|------------------|--------------|
| \_ALT HOTKEYF     | tecla ALT      |
| \_controle HOTKEYF | Chave de controle  |
| HOTKEYF \_ ext     | Chave estendida |
| HOTKEYF \_ Shift   | Tecla SHIFT    |



 

## <a name="remarks"></a>Comentários

O valor de 16 bits retornado por essa mensagem pode ser usado como o parâmetro *wParam* na mensagem do [**WM \_ settecla**](/windows/desktop/inputdev/wm-sethotkey) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

