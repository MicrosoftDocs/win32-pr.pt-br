---
title: MCI_UPDATE comando (mmsystem. h)
description: O comando de atualização do MCI \_ atualiza o retângulo de exibição. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE comando Windows multimídia
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58333b108891a8bcd0e0548d4dcd0db2f2606d1259f0934f19b8f6804afab3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689676"
---
# <a name="mci_update-command"></a>Comando de atualização do MCI \_

O comando de atualização do MCI \_ atualiza o retângulo de exibição. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo "DigitalVideo":

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>DGV de atualização do MCI ( \_ \_ \_ HDC)
</dt> <dd>

O membro **HDC** da estrutura identificada por *lpDest* contém uma janela válida do DC a ser pintada. Esse sinalizador é necessário.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpUnfreeze* contém um retângulo de exibição válido. O retângulo especifica o retângulo de recorte relativo ao retângulo do cliente.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>pintura de atualização do MCI \_ DGV \_ \_
</dt> <dd>

Um aplicativo usa esse sinalizador quando recebe uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) que é destinada a um controlador de domínio de vídeo. Um dispositivo de buffer de quadro geralmente pinta a cor da chave. Se o dispositivo de vídeo não tiver um buffer de quadros, ele poderá ignorar o \_ comando de atualização do MCI quando o sinalizador de **pintura de atualização do MCI \_ \_ \_ DGV** for usado porque a exibição será repintada durante a operação de reprodução.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpDest* aponta para uma estrutura de parâmetros de [**atualização de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .

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

 

