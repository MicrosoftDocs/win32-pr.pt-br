---
title: MCI_CUE comando (mmsystem. h)
description: O \_ comando de indicação MCI indicações de um dispositivo para que a reprodução ou a gravação comece com o atraso mínimo. Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 22da4a84-a7af-42df-b950-8d1184fff9ba
keywords:
- MCI_CUE comando Windows multimídia
topic_type:
- apiref
api_name:
- MCI_CUE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 432c3fcd89a4841840559e44400716834df260b533d2cf40daa9da5e6a8fb6f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784596"
---
# <a name="mci_cue-command"></a>\_Comando de indicação MCI

O \_ comando de indicação MCI indicações de um dispositivo para que a reprodução ou a gravação comece com o atraso mínimo. Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpCue
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

<span id="lpCue"></span><span id="lpcue"></span><span id="LPCUE"></span>*lpCue*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_CUE_INPUT"></span><span id="mci_dgv_cue_input"></span>\_entrada de \_ indicação MCI DGV \_
</dt> <dd>

Uma instância de vídeo digital deve se preparar para a gravação. Se o aplicativo não tiver espaço em disco reservado, o dispositivo reservará o espaço em disco usando seus parâmetros padrão. O aplicativo pode omitir esse sinalizador se a fonte da apresentação atual já for a entrada externa. (Esse sinalizador não tem efeito na seleção da origem da apresentação.)

</dd> <dt>

<span id="MCI_DGV_CUE_NOSHOW"></span><span id="mci_dgv_cue_noshow"></span>\_DGV da \_ pista do MCI \_
</dt> <dd>

Uma instância de vídeo digital deve se preparar para reproduzir o quadro especificado com o comando sem exibi-lo. Quando esse sinalizador é especificado, a exibição continua a mostrar a imagem no buffer de quadro, embora seu quadro correspondente não seja a posição atual. Por exemplo, se o buffer de quadros contiver a imagem do quadro 7, o dispositivo continuará a mostrar o quadro 7 quando esse sinalizador for usado para marcar o dispositivo para qualquer outra posição. Um comando de indicação subsequente sem esse sinalizador e sem o MCI \_ para sinalizar exibe o quadro atual.

</dd> <dt>

<span id="MCI_DGV_CUE_OUTPUT"></span><span id="mci_dgv_cue_output"></span>\_saída de \_ indicação MCI DGV \_
</dt> <dd>

Uma instância de vídeo digital deve se preparar para a execução. Se o espaço de trabalho estiver em pausa, nenhum posicionamento ocorrerá. Se o espaço de trabalho for interrompido, a posição poderá mudar para uma imagem de quadro chave anterior. O aplicativo pode omitir esse sinalizador se a fonte da apresentação atual já for o espaço de trabalho.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

Uma posição de espaço de trabalho é incluída no membro **dwTo** da estrutura identificada por *lpCue*. As unidades atribuídas aos valores de posição são especificadas usando \_ o \_ \_ sinalizador de formato de tempo MCI set do comando [MCI \_ set](mci-set.md) . Isso é equivalente a procurar uma posição, exceto que o dispositivo é pausado após o comando.

</dd> </dl>

Para dispositivos **DigitalVideo** , o parâmetro *lpCue* aponta para uma estrutura de [**parâmetros MCI do \_ DGV \_ Cue \_**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cue_parms) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ de
</dt> <dd>

O membro **dwFrom** da estrutura apontada por *lpCue* contém o local inicial especificado no formato de hora atual.

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ para
</dt> <dd>

O membro **dwTo** da estrutura apontada por *lpCue* contém o local final (pausando) especificado no formato de hora atual.

</dd> <dt>

<span id="MCI_VCR_CUE_INPUT"></span><span id="mci_vcr_cue_input"></span>\_entrada de \_ indicação de VCR MCI \_
</dt> <dd>

Prepare-se para a gravação.

</dd> <dt>

<span id="MCI_VCR_CUE_OUTPUT"></span><span id="mci_vcr_cue_output"></span>\_saída de \_ pista de VCR MCI \_
</dt> <dd>

Prepare-se para jogar. Se nenhuma \_ \_ entrada de sinalização de VCR MCI \_ ou \_ \_ saída de sinal de VCR MCI \_ for especificada, a \_ saída de sinalização de VCR MCI \_ \_ será assumida.

</dd> <dt>

<span id="MCI_VCR_CUE_PREROLL"></span><span id="mci_vcr_cue_preroll"></span>preversão de \_ \_ sinalização de VCR MCI \_
</dt> <dd>

Marque o dispositivo para a posição atual ou a posição **dwFrom** , menos a duração de preversão. Isso permitirá que o dispositivo se prepare antes de inserir o modo de gravação ou de reprodução.

</dd> <dt>

<span id="MCI_VCR_CUE_REVERSE"></span><span id="mci_vcr_cue_reverse"></span>inversão de \_ \_ sinalização de videocassete MCI \_
</dt> <dd>

A direção do comando de próxima reprodução ou de registro é inversa.

</dd> </dl>

Quando advertência para reprodução usando o comando de \_ indicação MCI com o \_ sinalizador de \_ saída MCI de sinalização de videocassete \_ , você pode cancelar \_ a indicação de MCI emitindo o comando de [ \_ reprodução MCI](mci-play.md) com MCI \_ de, MCI \_ para ou MCI de \_ reprodução de VCR \_ \_ .

Quando advertência para gravação usando \_ a indicação MCI com o \_ sinalizador de entrada de sinalização de videocassete MCI \_ \_ , você pode cancelar \_ a indicação de MCI emitindo o comando de [ \_ registro MCI](mci-record.md) com a \_ inicialização do registro MCI de, MCI \_ para ou MCI \_ VCR \_ \_ .

Para dispositivos **VCR** , o parâmetro *lpCue* aponta para uma estrutura de [**\_ \_ \_ parâmetros de sinalização VCR MCI**](mci-vcr-cue-parms.md) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_INPUT"></span><span id="mci_wave_input"></span>\_entrada de onda MCI \_
</dt> <dd>

Um dispositivo de entrada de wave-áudio deve ser cued.

</dd> <dt>

<span id="MCI_WAVE_OUTPUT"></span><span id="mci_wave_output"></span>\_saída de onda MCI \_
</dt> <dd>

Um dispositivo de saída de wave-áudio deve ser cued. Esse será o sinalizador padrão se um sinalizador não for especificado.

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

 

