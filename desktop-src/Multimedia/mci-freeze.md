---
title: MCI_FREEZE comando (mmsystem. h)
description: O \_ comando congelar do MCI congela o movimento na tela. Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.
ms.assetid: 6f90984a-24dc-4046-8234-986b2125bab4
keywords:
- Multimídia do Windows de comando MCI_FREEZE
topic_type:
- apiref
api_name:
- MCI_FREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705117aef85fe69382657c647240849b515afa07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009062"
---
# <a name="mci_freeze-command"></a>\_Comando congelar MCI

O \_ comando congelar do MCI congela o movimento na tela. Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_FREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpFreeze
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

<span id="lpFreeze"></span><span id="lpfreeze"></span><span id="LPFREEZE"></span>*lpFreeze*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais são usados pelo tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_FREEZE_AT"></span><span id="mci_dgv_freeze_at"></span>\_ \_ congelamento de DGV MCI \_ em
</dt> <dd>

O membro **RC** da estrutura identificada por *lpFreeze* contém um retângulo válido. O retângulo especifica uma região dentro do buffer de quadro que terá o bit de máscara de bloqueio para cada pixel ativado. Os pixels especificados não serão atualizados até que o bit de máscara de bloqueio seja desativado. Se esse sinalizador não for especificado, o retângulo padronizará para todo o buffer de quadro. Esse sinalizador só terá suporte se o comando [MCI \_ GETDEVCAPS](mci-getdevcaps.md) retornar **true** para o \_ DGV MCI \_ GETDEVCAPS \_ puder \_ bloquear o sinalizador.

</dd> <dt>

<span id="MCI_DGV_FREEZE_OUTSIDE"></span><span id="mci_dgv_freeze_outside"></span>\_congelamento de DGV MCI \_ \_ fora do
</dt> <dd>

A área fora da região especificada para o \_ sinalizador MCI DGV \_ congelar \_ em está congelada.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpFreeze* aponta para uma estrutura [**MCI de \_ DGV \_ congelable \_ parms**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_rect_parms) .

Os seguintes sinalizadores adicionais são usados pelo tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_FREEZE_FIELD"></span><span id="mci_vcr_freeze_field"></span>\_campo de \_ congelamento de VCR MCI \_
</dt> <dd>

Congelar apenas um membro do quadro atual.

</dd> <dt>

<span id="MCI_VCR_FREEZE_FRAME"></span><span id="mci_vcr_freeze_frame"></span>\_quadro de \_ congelamento de VCR MCI \_
</dt> <dd>

Congele os dois campos do quadro atual.

</dd> <dt>

<span id="MCI_VCR_FREEZE_INPUT"></span><span id="mci_vcr_freeze_input"></span>\_entrada de \_ congelamento de VCR MCI \_
</dt> <dd>

Congelar o quadro atual na tela (usado para gravação).

</dd> <dt>

<span id="MCI_VCR_FREEZE_OUTPUT"></span><span id="mci_vcr_freeze_output"></span>\_saída de \_ congelamento de VCR MCI \_
</dt> <dd>

Congele o quadro atual do VCR (usado com a captura de quadros).

</dd> </dl>

Para dispositivos VCR, o parâmetro *lpFreeze* aponta para uma estrutura de [**\_ \_ parâmetros genéricos MCI**](mci-generic-parms.md) .

O seguinte sinalizador adicional é usado pelo tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpFreeze* contém um retângulo válido. Se esse sinalizador não for especificado, o driver do dispositivo congelará o quadro inteiro.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpFreeze* aponta para uma estrutura de [**parâmetros MCI do \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) .

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

 

