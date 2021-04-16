---
description: Sinaliza que um comando de DVD Navigator foi iniciado.
ms.assetid: 230116b4-23f1-4c37-a781-da2c5aa20a1f
title: EC_DVD_CMD_START (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CMD_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 0fb723b220bf8aa12baa7133c9985225d6051921
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752479"
---
# <a name="ec_dvd_cmd_start"></a>\_início do \_ cmd de DVD do EC \_

Sinaliza que um comando de [DVD Navigator](dvd-navigator-filter.md) foi iniciado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador do comando. Passe este parâmetro para o método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) para recuperar um ponteiro de interface [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor **HRESULT** que indica o status do comando.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse evento só será disparado se o aplicativo definir o sinalizador de **sinalizador de comando de DVD \_ \_ \_ SendEvents** em um método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) que usa um sinalizador de [**sinalizadores de DVD \_ cmd \_**](/windows/win32/api/strmif/ne-strmif-dvd_cmd_flags) .

Esse evento é gerado no domínio do título.

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
</dt> <dt>

[Sincronizando comandos de DVD](synchronizing-dvd-commands.md)
</dt> </dl>

 

 




