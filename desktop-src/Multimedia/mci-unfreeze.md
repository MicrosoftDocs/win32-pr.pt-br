---
title: MCI_UNFREEZE comando (mmsystem. h)
description: O \_ comando de descongelar do MCI restaura o movimento para uma área do buffer de vídeo congelada com o \_ comando MCI Freeze. Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 79ff1be5-6e30-4ef4-ab81-fc5643e3a72d
keywords:
- MCI_UNFREEZE comando Windows multimídia
topic_type:
- apiref
api_name:
- MCI_UNFREEZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3011f3d2c05c304b37957c6f4cb78f2ada9389ab727a7af63a358fd4b5afdd3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525566"
---
# <a name="mci_unfreeze-command"></a>\_Comando de DEScongelar do MCI

O \_ comando de descongelar do MCI restaura o movimento para uma área do buffer de vídeo congelada com o comando [MCI \_ Freeze](mci-freeze.md) . Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNFREEZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUnfreeze
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

<span id="lpUnfreeze"></span><span id="lpunfreeze"></span><span id="LPUNFREEZE"></span>*lpUnfreeze*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O seguinte sinalizador adicional é usado com o tipo de dispositivo **DigitalVideo** :

\_DGV \_ Rect MCI

O membro **RC** da estrutura identificada por *lpUnfreeze* contém um retângulo de exibição válido. O retângulo especifica uma região dentro do buffer de quadro cujos pixels devem ter seu bit de máscara de bloqueio desativado. Regiões retangulares são especificadas conforme descrito para o comando [MCI \_ Put](mci-put.md) . Se omitido, o retângulo assume como padrão o buffer de quadro inteiro. Usando uma sequência de comandos congelar e descongelar com retângulos diferentes, os padrões arbitrários de bits de máscara de bloqueio podem ser descritos.

Para dispositivos de vídeo digital, o parâmetro *lpUnfreeze* aponta para uma estrutura **MCI \_ DGV \_ descongelar \_ parâmetros** . Para obter mais informações, consulte os comentários para a estrutura de [**parâmetros do MCI \_ DGV \_ Rect \_**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_UNFREEZE_INPUT"></span><span id="mci_vcr_unfreeze_input"></span>\_entrada de \_ descongelar do VCR MCI \_
</dt> <dd>

Descongele a entrada.

</dd> <dt>

<span id="MCI_VCR_UNFREEZE_OUTPUT"></span><span id="mci_vcr_unfreeze_output"></span>\_saída de \_ descongelar do VCR MCI \_
</dt> <dd>

Descongele a saída.

</dd> </dl>

O seguinte sinalizador adicional é usado com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpUnfreeze* contém um retângulo de exibição válido. Esse é um parâmetro necessário.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpUnfreeze* aponta para uma estrutura de [**parâmetros MCI do \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) .

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

 

