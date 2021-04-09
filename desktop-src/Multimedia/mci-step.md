---
title: MCI_STEP comando (mmsystem. h)
description: O \_ comando da etapa MCI percorre o jogador um ou mais quadros. Dispositivos Digital-Video, VCR e CAV-Format VIDEODISC reconhecem este comando.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- Multimídia do Windows de comando MCI_STEP
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085146"
---
# <a name="mci_step-command"></a>\_Comando de etapa MCI

O \_ comando da etapa MCI percorre o jogador um ou mais quadros. Dispositivos Digital-Video, VCR e CAV-Format VIDEODISC reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Esse comando dá suporte a dispositivos que retornam **true** para o MCI \_ GETDEVCAPS \_ tem \_ um sinalizador de vídeo do comando [ \_ GETDEVCAPS MCI](mci-getdevcaps.md) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_quadros de \_ etapa MCI DGV \_
</dt> <dd>

O membro **dwFrames** da estrutura identificada por *lpStep* especifica o número de quadros a serem adiantados antes de exibir outra imagem.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>etapa do MCI \_ DGV \_ \_ inversa
</dt> <dd>

Etapas em ordem inversa.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpStep* aponta para uma estrutura de [**\_ \_ \_ parâmetros de etapa DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_quadros de \_ etapa do VCR MCI \_
</dt> <dd>

O membro **dwFrames** da estrutura identificada por *lpStep* especifica o número de quadros a serem adiantados antes de exibir outra imagem.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_etapa do VCR MCI \_ \_ inverso
</dt> <dd>

Etapas em ordem inversa.

</dd> </dl>

Para dispositivos VCR, o parâmetro *lpStep* aponta para uma estrutura de parâmetros de [**etapa de \_ VCR \_ \_ MCI**](mci-vcr-step-parms.md) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VIDEODISC** :

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>\_quadros de \_ etapa de VD do MCI \_
</dt> <dd>

O membro **dwFrames** da estrutura identificada por *lpStep* especifica o número de quadros a serem etapa.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>reversão de \_ etapa de VD MCI \_ \_
</dt> <dd>

Etapas em ordem inversa.

</dd> </dl>

Para dispositivos VIDEODISC, o parâmetro *lpStep* aponta para uma estrutura de parâmetros de etapa de VD do [**MCI \_ \_ \_**](mci-vd-step-parms.md) .

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

 

