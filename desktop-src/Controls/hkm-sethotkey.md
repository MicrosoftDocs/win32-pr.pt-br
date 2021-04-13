---
title: Mensagem de HKM_SETHOTKEY (commctrl. h)
description: Define a combinação de teclas de acesso para um controle de tecla quente.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- Controles de HKM_SETHOTKEY de mensagens do Windows
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499332"
---
# <a name="hkm_sethotkey-message"></a>Mensagem HKM setde \_ atalho

Define a combinação de teclas de acesso para um controle de tecla quente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) do [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) é o código de chave virtual da tecla de atalho. O [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) do **LOWORD** é o modificador de chave que indica as chaves que definem uma combinação de teclas de acesso. Para obter uma lista de valores de sinalizador modificadores, consulte a descrição da mensagem [**hkm \_ getteclaize**](hkm-gethotkey.md) .

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

