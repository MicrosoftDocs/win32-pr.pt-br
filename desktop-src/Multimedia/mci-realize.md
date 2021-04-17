---
title: MCI_REALIZE comando (mmsystem. h)
description: O \_ comando de concretização do MCI faz com que um dispositivo gráfico perceba sua paleta em um DC (contexto de dispositivo). Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- Multimídia do Windows de comando MCI_REALIZE
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f2e59bfe9bbe1443f55ae0fbcf8819b932bb1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751174"
---
# <a name="mci_realize-command"></a>\_Comando de concretização do MCI

O \_ comando de concretização do MCI faz com que um dispositivo gráfico perceba sua paleta em um DC (contexto de dispositivo). Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

**MCI \_ NOTIFICAr**, **\_ espera de MCI** ou, para dispositivos de vídeo digital **, \_ teste MCI**. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*lpRealize*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Você deve usar esse comando quando seu aplicativo receber a [**mensagem \_ QUERYNEWPALETTE do WM**](/windows/desktop/gdi/wm-querynewpalette) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "DigitalVideo":

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ DGV \_ perceber \_ BKGD
</dt> <dd>

Percebe a paleta como uma paleta de plano de fundo.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>DGV de MCI \_ \_ perceba \_ normal
</dt> <dd>

O percebe normalmente a paleta. Esse é o padrão.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpRealize* aponta para uma estrutura de **\_ \_ parâmetros de reprovação MCI** . Para obter mais informações, consulte comentários na estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) .

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

 

