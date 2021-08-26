---
title: MCI_CAPTURE comando (Mmsystem.h)
description: O comando MCI CAPTURE captura o conteúdo do buffer de quadro e \_ o armazena em um arquivo especificado. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: bdebddc5-a0a0-449e-889e-37c7d6612c60
keywords:
- MCI_CAPTURE comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_CAPTURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc6bc6e31fd66153a8ea867f56a4e2638ad1f3392a284a61818e521327e52d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039446"
---
# <a name="mci_capture-command"></a>Comando MCI \_ CAPTURE

O comando MCI CAPTURE captura o conteúdo do buffer de quadro e \_ o armazena em um arquivo especificado. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CAPTURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CAPTURE_PARMS) lpCapture
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT ou MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpCapture"></span><span id="lpcapture"></span><span id="LPCAPTURE"></span>*lpCapture*
</dt> <dd>

Ponteiro para uma [**estrutura \_ MCI DGV \_ CAPTURE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_capture_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_CAPTURE_AS"></span><span id="mci_dgv_capture_as"></span>MCI \_ DGV \_ CAPTURE \_ AS
</dt> <dd>

O **membro lpstrFileName** da estrutura identificada por *lpCapture* contém um endereço de um buffer especificando o caminho de destino e o nome do arquivo. (Esse sinalizador é necessário.)

</dd> <dt>

<span id="MCI_DGV_CAPTURE_AT"></span><span id="mci_dgv_capture_at"></span>CAPTURA \_ DE DGV DA MCI \_ \_ EM
</dt> <dd>

O **membro rc** da estrutura identificada por *lpCapture contém* um retângulo válido. O retângulo especifica a região retangular dentro do buffer de quadro que é cortada e salva em disco. Se omitida, a região cortada assume como padrão o retângulo especificado ou padrão em um comando [ \_ PUT da MCI](mci-put.md) anterior que especifica a área de origem para essa instância do driver de dispositivo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

