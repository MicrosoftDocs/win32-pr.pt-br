---
title: MCI_RESTORE comando (mmsystem. h)
description: O \_ comando MCI Restore copia um bitmap de um arquivo para o buffer de quadros. Dispositivos de vídeo digital reconhecem este comando. Esse comando executa a ação oposta do comando de \_ captura MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- Multimídia do Windows de comando MCI_RESTORE
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644977"
---
# <a name="mci_restore-command"></a>\_Comando de restauração MCI

O \_ comando MCI Restore copia um bitmap de um arquivo para o buffer de quadros. Dispositivos de vídeo digital reconhecem este comando. Esse comando executa a ação oposta do comando [de \_ captura MCI](mci-capture.md) .

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*lpRestore*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de restauração DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A implementação pode reconhecer uma variedade de formatos de imagem, mas um DIB (bitmap independente de dispositivo) do Windows é sempre aceito.

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_restaurar DGV \_ MCI \_ de
</dt> <dd>

O membro **lpstrFileName** da estrutura identificada por *lpRestore* contém um endereço de um buffer que contém o nome de arquivo de origem. O nome do arquivo é necessário.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>restauração do MCI \_ DGV \_ \_ em
</dt> <dd>

O membro **RC** da estrutura identificada por *lpRestore* contém um retângulo válido. O retângulo especifica uma região do buffer de quadro em relação à sua origem. O primeiro par de coordenadas especifica o canto superior esquerdo do retângulo; o segundo par especifica a largura e a altura. Se esse sinalizador não for especificado, a imagem será copiada para o canto superior esquerdo do buffer de quadros.

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

 

