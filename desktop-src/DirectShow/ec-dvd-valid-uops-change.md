---
description: Sinaliza que o conjunto disponível de métodos de interface IDvdControl2 foi alterado.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: fafdbb5443a32a8029ad73d92a2b23c5f05c96d5dfc32375fd05e6d4502484a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051806"
---
# <a name="ec_dvd_valid_uops_change"></a>\_ \_ \_ alteração UOPS válida do DVD do EC \_

Sinaliza que o conjunto disponível de métodos de interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) foi alterado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que contém uma combinação de zero ou mais sinalizadores da enumeração [**de \_ \_ sinalizador UOP válida**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) . Os bits indicam quais comandos [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) foram explicitamente desabilitados pelo disco DVD.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento indica apenas quais operações são explicitamente desabilitadas pelo conteúdo no disco DVD. Ele não garante que seja válido chamar métodos que não estão desabilitados. Por exemplo, se nenhum botão estiver presente, o método [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) não funcionará, embora o método não esteja explicitamente desabilitado.

Esse evento é gerado em todos os domínios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificação de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




