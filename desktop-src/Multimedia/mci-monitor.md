---
title: MCI_MONITOR comando (mmsystem. h)
description: O \_ comando monitor MCI especifica a origem da apresentação. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- Multimídia do Windows de comando MCI_MONITOR
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918757"
---
# <a name="mci_monitor-command"></a>\_Comando do monitor MCI

O \_ comando monitor MCI especifica a origem da apresentação. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação MCI, \_ espera MCI ou teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*lpMonitor*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ parâmetros de \_ Monitor \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_método de \_ Monitor de DGV MCI \_
</dt> <dd>

Uma constante indicando que o método de monitoramento está incluído no membro **dwMethod** da estrutura identificada por *lpMonitor*.

Quando o \_ sinalizador de entrada do monitor MCI DGV \_ \_ é usado no membro **dwSource** , isso seleciona o método de monitoramento. Normalmente, diferentes métodos de monitoramento têm diferentes implicações sobre como o hardware é usado. O método de monitoramento padrão é selecionado pelo dispositivo.

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_origem do \_ Monitor MCI DGV \_
</dt> <dd>

Uma constante indicando que a origem do monitor está incluída no membro **dwSource** da estrutura identificada por *lpMonitor*.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

