---
title: MCI_SAVE comando (mmsystem. h)
description: O comando de salvamento do MCI \_ salva o arquivo atual.
ms.assetid: 286e6f31-cb93-443b-8191-8c363b366eae
keywords:
- Multimídia do Windows de comando MCI_SAVE
topic_type:
- apiref
api_name:
- MCI_SAVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a241c0379731e870940cd676c33ae192efc5d297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454805"
---
# <a name="mci_save-command"></a>Comando de salvamento do MCI \_

O comando de salvamento do MCI \_ salva o arquivo atual. Dispositivos que modificam arquivos não devem destruir a cópia original até receberem a mensagem de salvamento. Os dispositivos de sobreposição de vídeo e Wave-Audio reconhecem este comando. Embora os dispositivos de vídeo digital e os sequenciadores MIDI também reconheçam esse comando, os drivers MCIAVI e MCISEQ não o implementam.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SAVE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SAVE_PARMS ) lpSave
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

\_Notificação de MCI, \_ espera de MCI ou, para dispositivos de vídeo digital e VCR, \_ teste MCI. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpSave"></span><span id="lpsave"></span><span id="LPSAVE"></span>*lpSave*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de salvamento MCI**](mci-save-parms.md) . (Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Esse comando tem suporte em dispositivos que retornam **true** quando você chama o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) com o \_ GETDEVCAPS MCI que \_ pode \_ salvar o sinalizador.

O seguinte sinalizador adicional se aplica a todos os dispositivos que dão suporte ao [ \_ salvamento de MCI](/windows):

<dl> <dt>

<span id="MCI_SAVE_FILE"></span><span id="mci_save_file"></span>\_arquivo de salvamento de MCI \_
</dt> <dd>

O membro **lpFileName** da estrutura identificada por *lpSave* contém um endereço de um buffer que contém o nome de arquivo de destino.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpSave* contém um retângulo válido. O retângulo especifica uma região do buffer de quadro que será salva no arquivo especificado. O primeiro par de coordenadas especifica o canto superior esquerdo do retângulo; o segundo par especifica a largura e a altura. Dispositivos de vídeo digital devem usar o comando [MCI \_ Capture](mci-capture.md) para capturar o conteúdo do buffer de quadros. (Os dispositivos de sobreposição de vídeo também devem usar o MCI \_ CAPTURA.) Esse sinalizador é para compatibilidade com o conjunto de comandos de sobreposição de vídeo MCI existente.

</dd> <dt>

<span id="MCI_DGV_SAVE_ABORT"></span><span id="mci_dgv_save_abort"></span>\_ \_ anular salvamento de DGV MCI \_
</dt> <dd>

Interrompe uma operação de salvamento em andamento. Esse deve ser o único sinalizador presente.

</dd> <dt>

<span id="MCI_DGV_SAVE_KEEPRESERVE"></span><span id="mci_dgv_save_keepreserve"></span>MCI \_ DGV \_ Salvar \_ KEEPRESERVE
</dt> <dd>

O espaço em disco não utilizado saiu do comando [de \_ reserva do MCI](mci-reserve.md) original não é desalocado.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpSave* aponta para uma estrutura de parâmetros de [**salvamento de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_save_parmsa) .

O seguinte sinalizador adicional é usado com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpSave* contém um retângulo de exibição válido que indica a área do buffer de vídeo a ser salva.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpSave* aponta para uma estrutura de [**parâmetros de \_ \_ salvamento \_ de OVLY MCI**](/previous-versions//dd743447(v=vs.85)) .

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

 

