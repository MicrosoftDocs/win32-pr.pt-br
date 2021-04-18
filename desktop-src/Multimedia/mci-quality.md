---
title: MCI_QUALITY comando (mmsystem. h)
description: O comando de qualidade do MCI \_ define um nível de qualidade personalizado para compactação de dados de áudio, vídeo ou ainda imagem. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- Multimídia do Windows de comando MCI_QUALITY
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996703c1a5b7d3adec1a001af58ebc8d916301a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369214"
---
# <a name="mci_quality-command"></a>\_Comando de qualidade MCI

O comando de qualidade do MCI \_ define um nível de qualidade personalizado para compactação de dados de áudio, vídeo ou ainda imagem. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
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

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ \_ parâmetros de qualidade DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O nome definido para esse nível de qualidade pode ser usado ao definir o áudio, o vídeo ou ainda a qualidade com os comandos [MCI \_ SetAudio](mci-setaudio.md) e [MCI \_ setvideo](mci-setvideo.md) .

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_alg qualidade do MCI \_
</dt> <dd>

O membro **lpstrAlgorithm** da estrutura identificada por *lpQuality* contém um endereço de um buffer que contém o nome do algoritmo. Esse algoritmo deve ser suportado pelo driver de dispositivo e deve ser compatível com o descritor de áudio, ainda ou vídeo que é usado. Se esse sinalizador for omitido, o algoritmo atual será usado.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_caixa de diálogo qualidade do MCI \_
</dt> <dd>

O driver de dispositivo deve exibir uma caixa de diálogo para especificar o nível de qualidade. A caixa de diálogo tem campos específicos de algoritmo usados internamente pelo driver de dispositivo para criar uma estrutura que descreve um nível de qualidade específico.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_alça de qualidade do MCI \_
</dt> <dd>

O membro **dwHandle** da estrutura identificada por *lpQuality* contém um identificador para uma estrutura. A estrutura contém dados específicos de algoritmos que descrevem o nível de qualidade específico. O formato das estruturas para os algoritmos depende do dispositivo.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_item de qualidade MCI \_
</dt> <dd>

Uma constante indicando que o tipo de algoritmo está incluído no membro **dwItem** da estrutura identificada por *lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_nome da qualidade do MCI \_
</dt> <dd>

O membro **lpstrname** da estrutura identificada por *lpQuality* contém um endereço de um buffer que contém o descritor de qualidade.

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

 

