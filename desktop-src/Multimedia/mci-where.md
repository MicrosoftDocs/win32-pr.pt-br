---
title: MCI_WHERE comando (mmsystem. h)
description: O MCI \_ em que o comando obtém o retângulo de recorte para o dispositivo de vídeo.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- Multimídia do Windows de comando MCI_WHERE
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918507"
---
# <a name="mci_where-command"></a>MCI, \_ em que comando

O MCI \_ em que o comando obtém o retângulo de recorte para o dispositivo de vídeo. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando. Os membros **superior** e **esquerdo** do [Rect](/previous-versions//ms536136(v=vs.85)) retornado contêm a origem do retângulo de recorte e os membros **direito** e **inferior** contêm a largura e a altura do retângulo de recorte. (Esse não é o uso padrão dos membros **direito** e **inferior** .)

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
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

<span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ DGV \_ em que \_ destino
</dt> <dd>

Obtém uma descrição da região retangular usada para exibir vídeo e imagens na área do cliente da janela atual.

</dd> <dt>

<span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>DGV MCI, \_ \_ em que \_ frame
</dt> <dd>

Obtém uma descrição da região retangular do buffer de quadro no qual as imagens do retângulo de vídeo são dimensionadas. As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ DGV \_ em que \_ Max
</dt> <dd>

Quando usado com o MCI \_ DGV \_ onde \_ o destino ou o MCI \_ DGV \_ em que \_ a origem, o retângulo retornado indica a largura máxima e a altura da região especificada. Quando usado com o MCI \_ DGV \_ em que \_ Window, o retângulo retornado indica o tamanho da tela inteira.

</dd> <dt>

<span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ DGV \_ onde a \_ origem
</dt> <dd>

Obtém uma descrição da região retangular (cortada do buffer de quadro) que é ampliada para se ajustar ao retângulo de destino na exibição.

</dd> <dt>

<span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>\_DGV MCI \_ em que \_ vídeo
</dt> <dd>

Obtém uma descrição da região retangular recortada da fonte da apresentação para preencher o retângulo do quadro no buffer do quadro. As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>DGV MCI, \_ \_ em que \_ janela
</dt> <dd>

Obtém uma descrição do quadro da janela de exibição.

</dd> <dt>


</dt> <dd></dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpQuery* aponta para um **\_ DGV MCI \_ em \_ que** a estrutura de parâmetros. O **DGV MCI em que a estrutura de \_ \_ \_ parms** é idêntica à estrutura de [**parâmetros do MCI \_ DGV \_ Rect \_**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ OVLY \_ em que \_ destino
</dt> <dd>

Obtém o retângulo de exibição de destino. As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>OVLY MCI, \_ \_ em que \_ frame
</dt> <dd>

Obtém o retângulo de quadro sobreposto. As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ OVLY \_ onde a \_ origem
</dt> <dd>

Obtém o retângulo de origem. As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.

</dd> <dt>

<span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>\_OVLY MCI \_ em que \_ vídeo
</dt> <dd>

Obtém o retângulo de vídeo. As coordenadas de retângulo são colocadas no membro **RC** da estrutura identificada por *lpQuery*.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpQuery* aponta para uma estrutura de [**parâmetros MCI do \_ OVLY \_ Rect \_**](mci-ovly-rect-parms.md) .

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

 

