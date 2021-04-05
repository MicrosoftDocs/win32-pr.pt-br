---
title: MCI_PLAY comando (mmsystem. h)
description: O \_ comando MCI Play sinaliza o dispositivo para começar a transmitir dados de saída. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: d912ab49-63f0-40a9-aa4c-f9463782b54c
keywords:
- Multimídia do Windows de comando MCI_PLAY
topic_type:
- apiref
api_name:
- MCI_PLAY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f985a8d5d6be7ad42702afc898b3aaf437ef320
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824824"
---
# <a name="mci_play-command"></a>\_Comando de reprodução MCI

O \_ comando MCI Play sinaliza o dispositivo para começar a transmitir dados de saída. CD de áudio, digital-vídeo, MIDI Sequencer, VIDEODISC, VCR e Wave-Audio Devices reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PLAY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_PLAY_PARMS ) lpPlay
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

<span id="lpPlay"></span><span id="lpplay"></span><span id="LPPLAY"></span>*lpPlay*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de reprodução MCI**](mci-play-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que dão suporte a \_ reprodução MCI:

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

Um local inicial é incluído no membro **dwFrom** da estrutura identificada por *lpPlay*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato MCI set time do comando [MCI \_ set](mci-set.md) . Se \_ o MCI de não for especificado, o local inicial padrão será a posição atual.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Um local final é incluído no membro **dwTo** da estrutura identificada por *lpPlay*. As unidades atribuídas aos valores de posição são especificadas com o \_ \_ \_ sinalizador de formato de hora definido do MCI do conjunto de MCI \_ . Se \_ o MCI para não for especificado, o local final será padronizado para o final da mídia.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_PLAY_REPEAT"></span><span id="mci_dgv_play_repeat"></span>\_repetição de \_ reprodução de DGV MCI \_
</dt> <dd>

A reprodução deve iniciar novamente no início quando o final do conteúdo for atingido.

</dd> <dt>

<span id="MCI_DGV_PLAY_REVERSE"></span><span id="mci_dgv_play_reverse"></span>reversão do MCI \_ DGV \_ reproduzir \_
</dt> <dd>

A reprodução deve ocorrer em ordem inversa.

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_WINDOW"></span><span id="mci_mciavi_play_window"></span>janela de reprodução do MCI \_ Mciavi \_ \_
</dt> <dd>

A reprodução deve ocorrer na janela associada a uma instância de dispositivo (o padrão). (Esse sinalizador é específico do MCIAVI. DRV.)

</dd> <dt>

<span id="MCI_MCIAVI_PLAY_FULLSCREEN"></span><span id="mci_mciavi_play_fullscreen"></span>tela de execução do MCI \_ Mciavi \_ \_
</dt> <dd>

A reprodução deve usar uma exibição de tela inteira. Use este sinalizador somente ao executar arquivos compactados ou de 8 bits.

</dd> </dl>

Para dispositivos de vídeo digital, o *lpPlay* aponta para uma estrutura de parâmetros de [**reprodução de \_ DGV \_ \_ MCI**](/previous-versions//dd743396(v=vs.85)) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_PLAY_AT"></span><span id="mci_vcr_play_at"></span>\_ \_ reprodução de VCR MCI \_ em
</dt> <dd>

O membro **dwAt** da estrutura identificada por *lpPlay* contém uma hora em que o comando inteiro começa, ou se o dispositivo for cued, quando o dispositivo atingir a posição from fornecida pelo comando de [ \_ indicação MCI](mci-cue.md) .

</dd> <dt>

<span id="MCI_VCR_PLAY_REVERSE"></span><span id="mci_vcr_play_reverse"></span>reversão de \_ reprodução de VCR MCI \_ \_
</dt> <dd>

A reprodução deve ocorrer em ordem inversa.

</dd> <dt>

<span id="MCI_VCR_PLAY_SCAN"></span><span id="mci_vcr_play_scan"></span>\_verificação de \_ reprodução de VCR MCI \_
</dt> <dd>

A reprodução deve ser a mais rápida possível e manter a saída de vídeo.

</dd> </dl>

Para dispositivos VCR, o *lpPlay* aponta para uma estrutura de parâmetros de [**reprodução de \_ VCR \_ \_ MCI**](mci-vcr-play-parms.md) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VIDEODISC** :

<dl> <dt>

<span id="MCI_VD_PLAY_FAST"></span><span id="mci_vd_play_fast"></span>\_ \_ reprodução rápida de VD do MCI \_
</dt> <dd>

Jogue rapidamente.

</dd> <dt>

<span id="MCI_VD_PLAY_REVERSE"></span><span id="mci_vd_play_reverse"></span>reversão de \_ reprodução de VD MCI \_ \_
</dt> <dd>

Reproduzir em ordem inversa.

</dd> <dt>

<span id="MCI_VD_PLAY_SCAN"></span><span id="mci_vd_play_scan"></span>\_exame de \_ reprodução de VD do MCI \_
</dt> <dd>

Verificar rapidamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SLOW"></span><span id="mci_vd_play_slow"></span>\_reprodução de VD MCI \_ \_ lenta
</dt> <dd>

Reproduzir lentamente.

</dd> <dt>

<span id="MCI_VD_PLAY_SPEED"></span><span id="mci_vd_play_speed"></span>\_velocidade de \_ reprodução de VD do MCI \_
</dt> <dd>

A velocidade de reprodução é incluída no membro **dwSpeed** na estrutura identificada por *lpPlay*.

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

 

