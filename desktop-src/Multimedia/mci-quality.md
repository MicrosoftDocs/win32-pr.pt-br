---
title: MCI_QUALITY comando (Mmsystem.h)
description: O comando MCI QUALITY define um nível de qualidade personalizado para compactação de dados de \_ áudio, vídeo ou ainda imagem. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- MCI_QUALITY comando Windows Multimídia
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
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138217"
---
# <a name="mci_quality-command"></a>Comando MCI \_ QUALITY

O comando MCI QUALITY define um nível de qualidade personalizado para compactação de dados de \_ áudio, vídeo ou ainda imagem. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT ou MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*lpQuality*
</dt> <dd>

Ponteiro para uma [**estrutura \_ MCI DGV \_ QUALITY \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O nome definido para esse nível de qualidade pode ser usado ao definir o áudio, o vídeo ou ainda a qualidade com os comandos [MCI \_ SETAUDIO](mci-setaudio.md) e [MCI \_ SETVIDEO.](mci-setvideo.md)

Os seguintes sinalizadores adicionais se aplicam a dispositivos de vídeo digital:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>MCI \_ QUALITY \_ ALG
</dt> <dd>

O **membro lpstrAlgorithm** da estrutura identificada por *lpQuality* contém um endereço de um buffer que contém o nome do algoritmo. Esse algoritmo deve ter suporte do driver de dispositivo e deve ser compatível com o descritor de áudio, ainda ou vídeo usado. Se esse sinalizador for omitido, o algoritmo atual será usado.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>CAIXA DE DIÁLOGO QUALIDADE DA MCI \_ \_
</dt> <dd>

O driver de dispositivo deve exibir uma caixa de diálogo para especificar o nível de qualidade. A caixa de diálogo tem campos específicos do algoritmo usados internamente pelo driver de dispositivo para criar uma estrutura que descreve um nível de qualidade específico.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>MCI \_ QUALITY \_ HANDLE
</dt> <dd>

O **membro dwHandle** da estrutura identificada por *lpQuality* contém um identificador para uma estrutura. A estrutura contém dados específicos de algoritmo que descrevem o nível de qualidade específico. O formato das estruturas para os algoritmos depende do dispositivo.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>ITEM DE QUALIDADE da MCI \_ \_
</dt> <dd>

Uma constante que indica que o tipo de algoritmo está incluído no **membro dwItem** da estrutura identificada por *lpQuality*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>MCI \_ QUALITY \_ NAME
</dt> <dd>

O **membro lpstrName** da estrutura identificada por *lpQuality* contém um endereço de um buffer que contém o descritor de qualidade.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

