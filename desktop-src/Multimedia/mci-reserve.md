---
title: MCI_RESERVE comando (Mmsystem.h)
description: O comando MCI RESERVE aloca espaço em disco contíguo para o workspace da instância do driver de dispositivo \_ para uso com gravação subsequente. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- MCI_RESERVE comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_RESERVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f21570d37fba9bc0c9595715715a9291aedd30650081edfa5d50f7264cf16c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803457"
---
# <a name="mci_reserve-command"></a>Comando MCI \_ RESERVE

O comando MCI RESERVE aloca espaço em disco contíguo para o workspace da instância do driver de dispositivo \_ para uso com gravação subsequente. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESERVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESERVE_PARMS) lpReserve
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

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Ponteiro para uma [**estrutura \_ MCI DGV \_ RESERVE \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Se o workspace contiver dados não savados, esses dados serão perdidos. Se o espaço em disco não estiver reservado antes da gravação, o comando [MCI \_ RECORD](mci-record.md) executará uma reserva implícita com parâmetros padrão específicos do dispositivo. Em algumas implementações, a reserva não é necessária e pode ser ignorada pelo driver de dispositivo. Reservar espaço explicitamente proporciona um melhor controle sobre quando ocorre o atraso para alocação de disco, quanto espaço é alocado e onde o espaço em disco é alocado. A quantidade e o local do espaço em disco já reservado para essa instância de dispositivo podem ser alterados em emissão de MCI \_ RESERVE novamente. Qualquer espaço em disco alocado e ainda não usuário não é desaloqueado até que todos os dados gravados são salvos ou até que a instância do driver de dispositivo seja fechada.

Se o vídeo for desligado com o sinalizador MCI OFF do comando \_ [MCI \_ SETVIDEO,](mci-setvideo.md) o espaço reservado não incluirá nenhum vídeo. Se o áudio for desligado com o sinalizador MCI OFF do comando \_ [MCI \_ SETAUDIO,](mci-setaudio.md) o espaço reservado não incluirá nenhum áudio. Se áudio e vídeo estão desligados ou se o tamanho solicitado for zero, nenhum espaço será reservado e qualquer espaço reservado existente será desaloqueado.

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>MCI \_ DGV \_ RESERVE \_ IN
</dt> <dd>

O **membro lpstrPath** da estrutura identificada por *lpReserve* contém um endereço de um buffer que contém o local de um arquivo temporário. O buffer contém apenas a unidade e o caminho do diretório do arquivo usado para manter os dados gravados; o nome do arquivo é especificado pelo driver de dispositivo. Esse arquivo temporário é excluído quando a instância do dispositivo é fechada, a menos que ela seja salva explicitamente. Se esse sinalizador for omitido, o driver de dispositivo especificará onde o espaço em disco é alocado.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>MCI \_ DGV \_ RESERVE \_ SIZE
</dt> <dd>

O **membro dwSize** da estrutura identificada por *lpReserve* especifica a quantidade aproximada de espaço em disco a ser reservado no workspace para gravação. O valor é especificado no formato de hora atual. A quantidade de espaço em disco é estimada a partir do tempo solicitado e a partir do qual o formato de arquivo, o algoritmo de vídeo e áudio e os valores de qualidade estão em vigor. Se esse sinalizador for omitido, o driver de dispositivo poderá usar um valor padrão definido por ele.

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

 

