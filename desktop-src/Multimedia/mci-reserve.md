---
title: MCI_RESERVE comando (mmsystem. h)
description: O comando de reserva do MCI \_ aloca espaço em disco contíguo para o espaço de trabalho da instância de driver de dispositivo para uso com a gravação subsequente. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 01f0a377-0179-4b05-a642-af152a7a12ae
keywords:
- Multimídia do Windows de comando MCI_RESERVE
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
ms.openlocfilehash: b89eb457b63012aa9ee5624efef95945258d42c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918915"
---
# <a name="mci_reserve-command"></a>Comando de reserva do MCI \_

O comando de reserva do MCI \_ aloca espaço em disco contíguo para o espaço de trabalho da instância de driver de dispositivo para uso com a gravação subsequente. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação MCI, \_ espera MCI ou teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpReserve"></span><span id="lpreserve"></span><span id="LPRESERVE"></span>*lpReserve*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ parâmetros de \_ reserva \_ de DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_reserve_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Se o espaço de trabalho contiver dados não salvos, esses dados serão perdidos. Se o espaço em disco não for reservado antes da gravação, o comando de [ \_ registro MCI](mci-record.md) executará uma reserva implícita com parâmetros padrão específicos do dispositivo. Em algumas implementações, a reserva não é necessária e pode ser ignorada pelo driver de dispositivo. Reservar espaço explicitamente proporciona a você um melhor controle sobre quando o atraso de alocação de disco ocorre, quanto espaço é alocado e onde o espaço em disco é alocado. A quantidade e o local do espaço em disco já reservados para esta instância de dispositivo podem ser alterados emitindo \_ novamente a reserva MCI. Qualquer espaço em disco alocado e ainda não utilizado não será desalocado até que os dados gravados sejam salvos ou até que a instância do driver de dispositivo seja fechada.

Se o vídeo for desativado com o \_ sinalizador MCI off do comando [de \_ vídeo MCI](mci-setvideo.md) , o espaço reservado não inclui nenhum vídeo. Se o áudio for desativado com o \_ sinalizador MCI off do comando [ \_ SetAudio do MCI](mci-setaudio.md) , o espaço reservado não incluirá nenhum áudio. Se o áudio e o vídeo estiverem desligados ou se o tamanho solicitado for zero, nenhum espaço será reservado e qualquer espaço reservado existente será desalocado.

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_DGV_RESERVE_IN"></span><span id="mci_dgv_reserve_in"></span>\_ \_ reserva de DGV MCI \_ em
</dt> <dd>

O membro **lpstrPath** da estrutura identificada por *lpReserve* contém um endereço de um buffer que contém o local de um arquivo temporário. O buffer contém apenas a unidade e o caminho de diretório do arquivo usado para armazenar dados gravados; o nome de arquivo é especificado pelo driver de dispositivo. Esse arquivo temporário é excluído quando a instância do dispositivo é fechada, a menos que seja salva explicitamente. Se esse sinalizador for omitido, o driver de dispositivo especificará onde o espaço em disco está alocado.

</dd> <dt>

<span id="MCI_DGV_RESERVE_SIZE"></span><span id="mci_dgv_reserve_size"></span>\_tamanho de \_ reserva do DGV MCI \_
</dt> <dd>

O membro **dwSize** da estrutura identificada por *lpReserve* especifica a quantidade aproximada de espaço em disco a ser reservada no espaço de trabalho para gravação. O valor é especificado no formato de hora atual. A quantidade de espaço em disco é estimada a partir da hora solicitada e de qual formato de arquivo e algoritmo de vídeo e áudio e os valores de qualidade estão em vigor. Se esse sinalizador for omitido, o driver de dispositivo poderá usar um valor padrão definido por ele.

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

 

