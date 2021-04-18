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
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752068"
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

 

 




