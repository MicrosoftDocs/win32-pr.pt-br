---
title: MCI_PUT comando (mmsystem. h)
description: O \_ comando MCI Put define os retângulos de origem, destino e quadro. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- Multimídia do Windows de comando MCI_PUT
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086508"
---
# <a name="mci_put-command"></a>Comando de put do MCI \_

O \_ comando MCI Put define os retângulos de origem, destino e quadro. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

\_Notificação MCI, \_ espera MCI ou, para dispositivos de vídeo digital, teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>\_cliente DGV \_ put do MCI \_
</dt> <dd>

O retângulo definido para MCI \_ DGV \_ Rect aplica-se à posição da janela do cliente. O retângulo especificado é relativo à janela pai da janela de exibição. \_A janela do MCI DGV \_ Put \_ deve ser definida simultaneamente com esse sinalizador.

</dd> <dt>

<span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_destino de \_ Put \_ DGV do MCI
</dt> <dd>

O retângulo definido para \_ o MCI DGV \_ Rect especifica um retângulo de destino. O retângulo de destino especifica a parte da janela do cliente associada a essa instância de driver de dispositivo que mostra a imagem ou o vídeo.

</dd> <dt>

<span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>\_quadro de \_ Put \_ DGV do MCI
</dt> <dd>

O retângulo definido para \_ o MCI DGV \_ Rect aplica-se ao retângulo do quadro. O retângulo do quadro especifica a parte do buffer do quadro usado como o destino das imagens de vídeo obtidas do retângulo de vídeo. O vídeo deve ser dimensionado para caber no retângulo do buffer do quadro.

O retângulo é especificado em coordenadas de buffer de quadros. O retângulo padrão é o buffer de quadro completo. A especificação desse retângulo permite que o dispositivo dimensione a imagem à medida que digitaliza os dados. Os dispositivos que não podem dimensionar a imagem rejeitam esse comando com a \_ função sem suporte do MCIERR \_ . Você pode usar o \_ sinalizador MCI GETDEVCAPS \_ pode \_ ampliar com o [comando \_ GETDEVCAPS do MCI](mci-getdevcaps.md) para determinar se um dispositivo dimensiona a imagem. Um dispositivo retornará **falso** se não for possível dimensionar a imagem.

</dd> <dt>

<span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_fonte de \_ Put \_ DGV MCI
</dt> <dd>

O retângulo definido para \_ o MCI DGV \_ Rect especifica um retângulo de origem. O retângulo de origem especifica qual parte do buffer de quadro deve ser dimensionada para caber no retângulo de destino.

</dd> <dt>

<span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>vídeo do MCI \_ DGV \_ Put \_
</dt> <dd>

O retângulo definido para \_ o MCI DGV \_ Rect aplica-se ao retângulo de vídeo. O retângulo de vídeo especifica qual parte da fonte da apresentação atual é armazenada no buffer do quadro. O retângulo é especificado usando as coordenadas naturais da origem da apresentação. Ele permite a especificação de corte que ocorre antes de armazenar imagens e vídeo no buffer de quadros. O retângulo padrão é a área de verificação ativa completa ou imagens e vídeos totalmente descompactados.

</dd> <dt>

<span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_janela do DGV \_ Put \_ do MCI
</dt> <dd>

O retângulo definido para \_ o MCI DGV \_ Rect aplica-se à janela de exibição. Esse retângulo é relativo à janela pai da janela de exibição (geralmente a área de trabalho). Se a janela não for especificada, o padrão será o tamanho e a posição da janela inicial.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>\_DGV \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpDest* contém um retângulo válido.

</dd> </dl>

Para dispositivos de vídeo digital, *lpDest* aponta para uma estrutura [**MCI \_ DGV \_ colocar \_ parâmetros**](/previous-versions//dd743397(v=vs.85)) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_destino de \_ Put \_ OVLY do MCI
</dt> <dd>

O retângulo definido para \_ o MCI OVLY \_ Rect especifica a área da janela do cliente usada para exibir uma imagem. O retângulo contém o deslocamento e a extensão visível da imagem em relação à origem da janela. Se o quadro estiver sendo ampliado, a origem será ampliada para o retângulo de destino.

</dd> <dt>

<span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>\_quadro de \_ Put \_ OVLY do MCI
</dt> <dd>

O retângulo definido para o MCI \_ OVLY \_ Rect especifica a área do buffer de vídeo usado para receber a imagem de vídeo. O retângulo contém o deslocamento e a extensão da área do buffer em relação à origem do buffer de vídeo.

</dd> <dt>

<span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_fonte de \_ Put \_ OVLY MCI
</dt> <dd>

O retângulo definido para \_ o MCI OVLY \_ Rect especifica a área do buffer de vídeo usada como a origem da imagem digital. O retângulo contém o deslocamento e a extensão do retângulo de recorte para o buffer de vídeo em relação à sua origem.

</dd> <dt>

<span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>vídeo do MCI \_ OVLY \_ Put \_
</dt> <dd>

O retângulo definido para o MCI \_ OVLY \_ Rect especifica a área da captura de fonte de vídeo pelo buffer de vídeo. O retângulo contém o deslocamento e a extensão do retângulo de recorte da fonte de vídeo em relação à sua origem.

</dd> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpDest* contém um retângulo de exibição válido. Se esse sinalizador não for especificado, o retângulo padrão corresponderá às coordenadas do buffer de vídeo ou da janela que está sendo recortada.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, *lpDest* aponta para uma estrutura [**MCI \_ OVLY \_ Rect \_ parms**](mci-ovly-rect-parms.md) .

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

 

