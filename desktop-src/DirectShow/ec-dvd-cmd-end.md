---
description: Sinaliza que um comando específico do Navegador de DVD foi concluído.
ms.assetid: f460db8e-b966-41fa-bfa1-4ad3fa65c3e3
title: EC_DVD_CMD_END (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_END
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 869da360f3321059df81a609d5ce953ad64f60485126fe7ae8f5e5a7df21753a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965876"
---
# <a name="ec_dvd_cmd_end"></a>EC \_ DVD \_ CMD \_ END

Sinaliza que um comando [específico do Navegador de DVD](dvd-navigator-filter.md) foi concluído.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Identificador do comando. Passe esse parâmetro para o [**método IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar um ponteiro de interface [**IDvdCmd.**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valor HRESULT** que indica o status do comando.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento só será acionado se seu aplicativo define o sinalizador SendEvents do SINALIZADOR DE CMD de DVD em um \_ \_ método \_ [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que recebe um sinalizador [**\_ \_ FLAGS de CMD DE DVD.**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags)

Esse evento é gerado no domínio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdevcode.h (inclua Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificação de evento de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Sincronizando comandos de DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




