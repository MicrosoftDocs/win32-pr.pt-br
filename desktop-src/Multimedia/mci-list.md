---
title: MCI_LIST comando (mmsystem. h)
description: O \_ comando lista de MCI Obtém informações sobre o número e os tipos de entradas disponíveis para o dispositivo. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: 1977fbfa-cae4-4afe-9fc5-ac68177574ca
keywords:
- Multimídia do Windows de comando MCI_LIST
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
ms.openlocfilehash: 15d5a616085028132c83fd71c46f7d409bf48a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499794"
---
# <a name="mci_list-command"></a>Comando de lista de MCI \_

O \_ comando lista de MCI Obtém informações sobre o número e os tipos de entradas disponíveis para o dispositivo. Os dispositivos de vídeo digital e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação MCI, \_ espera MCI ou teste MCI \_ . Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpList"></span><span id="lplist"></span><span id="LPLIST"></span>*lpList*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros genéricos do MCI**](mci-generic-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_LIST_ALG"></span><span id="mci_dgv_list_alg"></span>DGV do MCI \_ \_ lista \_ alg
</dt> <dd>

O membro **lpstrAlgorithm** da estrutura identificada por *lpList* contém um endereço de um buffer que contém o nome de um algoritmo. O nome é usado para recuperar os tipos de descritores de qualidade associados a um algoritmo.

</dd> <dt>

<span id="MCI_DGV_LIST_COUNT"></span><span id="mci_dgv_list_count"></span>\_contagem de \_ lista de DGV MCI \_
</dt> <dd>

Retorna o número de opções do tipo especificado.

</dd> <dt>

<span id="MCI_DGV_LIST_ITEM"></span><span id="mci_dgv_list_item"></span>\_item de \_ lista de DGV MCI \_
</dt> <dd>

Uma constante indicando que o tipo de lista está incluído no membro **dwItem** da estrutura identificada por *lpList*. Esse sinalizador é necessário. Use uma das seguintes constantes para indicar o tipo de lista:

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_ALG"></span><span id="mci_dgv_list_audio_alg"></span>DGV do MCI da \_ \_ lista de \_ áudio \_
</dt> <dd>

O comando deve recuperar os nomes dos algoritmos de áudio.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_QUALITY"></span><span id="mci_dgv_list_audio_quality"></span>\_qualidade de \_ áudio da lista de DGV MCI \_ \_
</dt> <dd>

O comando deve recuperar os níveis de qualidade de áudio. Os níveis retornados são associados ao algoritmo referenciado pelo membro **lpstrAlgorithm** da estrutura identificada por *lpList*. Se esse membro for especificado usando a cadeia de caracteres "Current", as qualidades associadas ao algoritmo atual serão retornadas.

</dd> <dt>

<span id="MCI_DGV_LIST_AUDIO_STREAM"></span><span id="mci_dgv_list_audio_stream"></span>\_fluxo de \_ áudio da lista de DGV MCI \_ \_
</dt> <dd>

O comando deve recuperar os nomes dos fluxos de áudio.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_AL"></span><span id="mci_dgv_list_still_al"></span>\_lista de DGV MCI \_ \_ ainda \_ Al
</dt> <dd>

O comando deve recuperar os nomes dos algoritmos ainda.

</dd> <dt>

<span id="MCI_DGV_LIST_STILL_QUALITY"></span><span id="mci_dgv_list_still_quality"></span>a \_ qualidade da lista de DGV MCI é \_ \_ ainda \_
</dt> <dd>

O comando deve recuperar os níveis de qualidade. Os níveis retornados são associados ao algoritmo referenciado pelo membro **lpstrAlgorithm** da estrutura identificada por *lpList*. Se esse membro for especificado usando a cadeia de caracteres "Current", as qualidades associadas ao algoritmo atual serão retornadas.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_ALG"></span><span id="mci_dgv_list_video_alg"></span>\_ \_ \_ vídeo alg da lista de DGV MCI \_
</dt> <dd>

O comando deve recuperar os nomes dos algoritmos de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_QUALITY"></span><span id="mci_dgv_list_video_quality"></span>\_qualidade de \_ vídeo da lista de DGV MCI \_ \_
</dt> <dd>

O comando deve recuperar os níveis de qualidade do vídeo. Os níveis retornados são associados ao algoritmo referenciado pelo membro **lpstrAlgorithm** da estrutura identificada por *lpList*. Se esse membro for especificado usando a cadeia de caracteres "Current", as qualidades associadas ao algoritmo atual serão retornadas.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_SOURCE"></span><span id="mci_dgv_list_video_source"></span>\_fonte de \_ vídeo da lista de DGV MCI \_ \_
</dt> <dd>

O comando deve retornar informações sobre as fontes de vídeo. Quando usado com \_ \_ a contagem de lista de DGV MCI \_ , o comando retorna o número de fontes de vídeo. Quando usado com \_ \_ \_ o número da lista MCI DGV, o comando retorna o tipo de uma fonte de vídeo. O MCI define os seguintes tipos:

-   \_src DGV de vídeo de MCI \_ \_ \_ genérico
-   NTSC DGV do MCI de \_ \_ vídeo \_ \_
-   \_PAL DGV de \_ vídeo \_ do \_ MCI
-   \_DGV de \_ vídeo MCI \_ \_ RGB
-   SECAM de DGV do MCI de \_ \_ vídeo \_ \_
-   SVIDEO de DGV do MCI de \_ \_ vídeo \_ \_

Pode haver mais de uma fonte de cada tipo retornada. O tipo de origem genérico é usado quando mais de um tipo de sinal é permitido para esse conector.

</dd> <dt>

<span id="MCI_DGV_LIST_VIDEO_STREAM"></span><span id="mci_dgv_list_video_stream"></span>\_fluxo de \_ vídeo da lista de DGV MCI \_ \_
</dt> <dd>

O comando deve recuperar os nomes dos fluxos de vídeo.

</dd> <dt>

<span id="MCI_DGV_LIST_NUMBER"></span><span id="mci_dgv_list_number"></span>\_número da \_ lista de DGV MCI \_
</dt> <dd>

Um índice é especificado no membro **dwNumber** da estrutura identificada por *lpList*. O índice deve ser um inteiro entre 1 e o valor retornado para o \_ sinalizador de contagem de lista de DGV MCI \_ \_ .

</dd> </dl>

Para dispositivos de vídeo digital, o *lpList* aponta para uma estrutura de parâmetros de [**lista de \_ DGV \_ \_ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_list_parmsa) .

Os seguintes sinalizadores adicionais se aplicam ao tipo de dispositivo **VCR** :

<dl> <dt>

<span id="MCI_VCR_LIST_AUDIO_SOURCE"></span><span id="mci_vcr_list_audio_source"></span>\_fonte de \_ áudio da lista de VIDEOCASSETEs MCI \_ \_
</dt> <dd>

Listar entradas de áudio ou tipos.

</dd> <dt>

<span id="MCI_VCR_LIST_COUNT"></span><span id="mci_vcr_list_count"></span>\_contagem de lista de videocassetes MCI \_ \_
</dt> <dd>

Define o membro **dwReturn** da estrutura identificada por *lpList* para o número total de entradas de vídeo ou áudio.

</dd> <dt>

<span id="MCI_VCR_LIST_NUMBER"></span><span id="mci_vcr_list_number"></span>\_número da lista de videocassetes MCI \_ \_
</dt> <dd>

Define o membro **dwReturn** da estrutura identificada por *lpList* para o tipo da entrada de vídeo ou áudio especificada pelo membro **dwNumber** .

</dd> <dt>

<span id="MCI_VCR_LIST_VIDEO_SOURCE"></span><span id="mci_vcr_list_video_source"></span>\_fonte de \_ vídeo da lista de VIDEOCASSETEs MCI \_ \_
</dt> <dd>

Listar entradas ou tipos de vídeo.

</dd> </dl>

Para dispositivos VCR, o *lpList* aponta para uma estrutura de parâmetros de [**\_ \_ lista \_ de videocassetes MCI**](mci-vcr-list-parms.md) .

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

 

