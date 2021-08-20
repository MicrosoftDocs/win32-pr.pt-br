---
title: MCI_LIST comando (Mmsystem.h)
description: O comando MCI LIST obtém informações sobre o número e os tipos de entradas \_ disponíveis para o dispositivo. Os dispositivos de vídeo digital e VCR reconhecem esse comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- MCI_LIST comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_LIST
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9bd3aa35875791d6fa916d9d6831bdcb83a6db43be6e5859ce582243606f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138632"
---
# <a name="mci_list-command"></a>Comando MCI \_ LIST

O comando MCI LIST obtém informações sobre o número e os tipos de entradas \_ disponíveis para o dispositivo. Os dispositivos de vídeo digital e VCR reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LIST, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpList
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

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Ponteiro para uma [**estrutura \_ \_ PARMS GENÉRICA da MCI.**](mci-generic-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam ao **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>MCI \_ DGV \_ LIST \_ ALG
</dt> <dd>

O **membro lpstrAlgorithm** da estrutura identificada por *lpList* contém um endereço de um buffer que contém o nome de um algoritmo. O nome é usado para recuperar os tipos de descritores de qualidade associados a um algoritmo.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>CONTAGEM DE \_ LISTAS DE DGV \_ DA MCI \_
</dt> <dd>

Retorna o número de opções do tipo especificado.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>ITEM DE \_ LISTA DGV da MCI \_ \_
</dt> <dd>

Uma constante que indica que o tipo de lista está incluído no **membro dwItem** da estrutura identificada por *lpList*. Esse sinalizador é necessário. Use uma das seguintes constantes para indicar o tipo de lista:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>MCI \_ DGV \_ LIST \_ AUDIO \_ ALG
</dt> <dd>

O comando deve recuperar nomes de algoritmos de áudio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>QUALIDADE DE ÁUDIO \_ DA LISTA DE DGV da MCI \_ \_ \_
</dt> <dd>

O comando deve recuperar níveis de qualidade de áudio. Os níveis retornados são associados ao algoritmo referenciado pelo **membro lpstrAlgorithm** da estrutura identificada por *lpList*. Se esse membro for especificado usando a cadeia de caracteres "atual", as qualidades associadas ao algoritmo atual serão retornadas.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>FLUXO DE \_ ÁUDIO DA LISTA DGV \_ \_ da \_ MCI
</dt> <dd>

O comando deve recuperar nomes de fluxos de áudio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>MCI \_ DGV \_ LIST AINDA \_ \_ AL
</dt> <dd>

O comando deve recuperar nomes de algoritmos still.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>MCI \_ DGV \_ LIST \_ STILL \_ QUALITY
</dt> <dd>

O comando deve recuperar níveis de qualidade. Os níveis retornados são associados ao algoritmo referenciado pelo **membro lpstrAlgorithm** da estrutura identificada por *lpList*. Se esse membro for especificado usando a cadeia de caracteres "atual", as qualidades associadas ao algoritmo atual serão retornadas.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>ALG DE VÍDEO \_ DA LISTA DE DGV \_ \_ \_ DA MCI
</dt> <dd>

O comando deve recuperar nomes de algoritmos de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>QUALIDADE DO VÍDEO \_ DA LISTA DE DGV \_ \_ da \_ MCI
</dt> <dd>

O comando deve recuperar níveis de qualidade de vídeo. Os níveis retornados são associados ao algoritmo referenciado pelo **membro lpstrAlgorithm** da estrutura identificada por *lpList*. Se esse membro for especificado usando a cadeia de caracteres "atual", as qualidades associadas ao algoritmo atual serão retornadas.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>ORIGEM DO \_ VÍDEO DA LISTA DE DGV \_ \_ DA \_ MCI
</dt> <dd>

O comando deve retornar informações sobre as fontes de vídeo. Quando usado com MCI \_ DGV \_ LIST \_ COUNT, o comando retorna o número de fontes de vídeo. Quando usado com MCI \_ DGV \_ LIST \_ NUMBER, o comando retorna o tipo de uma fonte de vídeo. A MCI define os seguintes tipos:

-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ GENERIC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ NTSC
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ PAL
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ RGB
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SECAM
-   MCI \_ DGV \_ SETVIDEO \_ SRC \_ SVIDEO

Pode haver mais de uma fonte de cada tipo retornado. O tipo de origem genérico é usado quando mais de um tipo de sinal é permitido para esse conector.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>FLUXO DE VÍDEO \_ DA LISTA DE DGV \_ \_ da \_ MCI
</dt> <dd>

O comando deve recuperar nomes de fluxos de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>NÚMERO DA \_ LISTA DE DGV \_ DA MCI \_
</dt> <dd>

Um índice é especificado no **membro dwNumber** da estrutura identificada por *lpList*. O índice deve ser um inteiro entre 1 e o valor retornado para o sinalizador \_ LIST COUNT de DGV da MCI. \_ \_

</dd> </dl>

Para dispositivos de vídeo digital, *lpList* aponta para uma [**estrutura \_ MCI DGV \_ LIST \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa)

Os seguintes sinalizadores adicionais se aplicam ao **tipo de dispositivo vcr:**

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>FONTE DE ÁUDIO DA \_ LISTA DE VCR \_ \_ da \_ MCI
</dt> <dd>

Listar entradas ou tipos de áudio.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>CONTAGEM DE \_ LISTA DE VCR \_ DA MCI \_
</dt> <dd>

Define o **membro dwReturn** da estrutura identificada por *lpList* como o número total de entradas de áudio ou vídeo.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>NÚMERO DA LISTA \_ DE VCR \_ DA MCI \_
</dt> <dd>

Define o **membro dwReturn** da estrutura identificada por *lpList* para o tipo de entrada de áudio ou vídeo especificado pelo **membro dwNumber.**

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>ORIGEM DO VÍDEO \_ DA LISTA DE VCR \_ \_ DA \_ MCI
</dt> <dd>

Listar entradas ou tipos de vídeo.

</dd> </dl>

Para dispositivos VCR, *lpList* aponta para uma [**estrutura MCI \_ VCR \_ LIST \_ PARMS.**](mci-vcr-list-parms.md)

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

 

