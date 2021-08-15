---
title: MCI_OPEN comando (Mmsystem.h)
description: O comando MCI \_ OPEN inicializa um dispositivo ou arquivo. Todos os dispositivos reconhecem esse comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- MCI_OPEN comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a84c95df35ecd602c207daa716b62d90f6bdc79b0ede7f937d3a38e6d6a9373b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689976"
---
# <a name="mci_open-command"></a>Comando MCI \_ OPEN

O comando MCI \_ OPEN inicializa um dispositivo ou arquivo. Todos os dispositivos reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_OPEN, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_OPEN_PARMS) lpOpen
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

MCI \_ NOTIFY ou MCI \_ WAIT. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Ponteiro para uma [**estrutura MCI \_ OPEN \_ PARMS.**](mci-open-parms.md) (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O sinalizador MCI \_ OPEN TYPE deve ser usado sempre que um dispositivo for especificado na função \_ [**mciSendCommand.**](/previous-versions//dd757160(v=vs.85)) Se você abrir um dispositivo especificando uma constante de tipo de dispositivo, deverá especificar o sinalizador \_ MCI OPEN \_ TYPE ID, além \_ de MCI OPEN \_ \_ TYPE. Para uma lista de constantes de tipo de dispositivo, consulte [Tipos de dispositivo MCI](mci-device-types.md).

Se o sinalizador MCI OPEN SHAREABLE não for especificado quando um dispositivo ou arquivo for aberto inicialmente, todos os comandos MCI OPEN subsequentes para o dispositivo ou arquivo \_ \_ \_ falharão. Se o dispositivo ou o arquivo já estiver aberto e esse sinalizador não for especificado, a chamada falhará mesmo que o primeiro comando aberto especifique MCI \_ OPEN \_ SHAREABLE. Arquivos abertos para o MCISEQ. DRV e MCIWAVE. Os dispositivos DRV não podem ser compartilhadas.

O caso é ignorado no nome do dispositivo, mas não pode haver espaços em branco à frente ou à parte final.

Para usar a seleção automática de tipo (por meio das entradas no Registro), atribua o nome do arquivo e a extensão de arquivo ao membro **lpstrElementName** da estrutura identificada por *lpOpen*, de definir o membro **lpstrDeviceType** como **NULL** e de definir o sinalizador MCI \_ OPEN \_ ELEMENT.

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que suportam MCI \_ OPEN:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>MCI \_ OPEN \_ ALIAS
</dt> <dd>

Um alias é incluído no **membro lpstrAlias** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ OPEN \_ SHAREABLE
</dt> <dd>

O dispositivo ou o arquivo deve ser aberto como compartilhável.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>MCI \_ OPEN \_ TYPE
</dt> <dd>

Um nome de tipo de dispositivo ou constante é incluído no **membro lpstrDeviceType** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ID DE TIPO \_ ABERTO da MCI \_
</dt> <dd>

A palavra de ordem baixa do membro **lpstrDeviceType** da estrutura identificada por *lpOpen* contém um identificador de tipo de dispositivo MCI padrão e a palavra de ordem alta opcionalmente contém o índice ordinal para o dispositivo. Use esse sinalizador com o sinalizador MCI \_ OPEN \_ TYPE.

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam a dispositivos compostos:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>ELEMENTO OPEN DA MCI \_ \_
</dt> <dd>

Um nome de arquivo é incluído no **membro lpstrElementName** da estrutura identificada por *lpOpen.*

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>ID DO ELEMENTO OPEN DA MCI \_ \_ \_
</dt> <dd>

O **membro lpstrElementName** da estrutura identificada por *lpOpen* é interpretado como um **valor DWORD** e tem significado interno para o dispositivo. Use esse sinalizador com o sinalizador MCI \_ OPEN \_ ELEMENT.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o **tipo de dispositivo digitalvideo:**

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>MCI \_ DGV \_ OPEN \_ NOSTATIC
</dt> <dd>

O dispositivo deve reduzir o número de cores estáticas (do sistema) na paleta. Isso aumenta o número de cores disponíveis para renderizar o fluxo de vídeo. Esse sinalizador se aplica somente a dispositivos que compartilham uma paleta com Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>MCI \_ DGV \_ OPEN \_ PARENT
</dt> <dd>

O identificador de janela pai é especificado no **membro hWndParent** da estrutura identificada por *lpOpen.*

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>MCI \_ DGV \_ OPEN \_ WS
</dt> <dd>

Um estilo de janela é especificado no **membro dwStyle** da estrutura identificada por *lpOpen.*

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ OPEN \_ 16BIT
</dt> <dd>

Indica uma preferência para suporte a dispositivos MCI de 16 bits.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ OPEN \_ 32BIT
</dt> <dd>

Indica uma preferência para suporte a dispositivos MCI de 32 bits.

</dd> </dl>

Para dispositivos de vídeo digital, *o parâmetro lpOpen* aponta para uma estrutura [**\_ MCI DGV \_ OPEN \_ PARMS.**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa)

Os seguintes sinalizadores adicionais são usados com o tipo **de dispositivo de sobreposição:**

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>MCI \_ OVLY \_ OPEN \_ PARENT
</dt> <dd>

O identificador de janela pai é especificado no **membro hWndParent** da estrutura identificada por *lpOpen.*

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>MCI \_ OVLY \_ OPEN \_ WS
</dt> <dd>

Um estilo de janela é especificado no **membro dwStyle** da estrutura identificada por *lpOpen.* O **valor dwStyle** especifica o estilo da janela que o driver criará e exibirá se o aplicativo não fornecer uma. O parâmetro style recebe um inteiro que define o estilo da janela. Essas constantes são iguais aos estilos de janela padrão (como WS \_ CHILD, WS \_ OVERLAPPEDWINDOW ou WS \_ POPUP).

</dd> </dl>

Para dispositivos de sobreposição de vídeo, *o parâmetro lpOpen* aponta para uma estrutura [**MCI \_ OVLY \_ OPEN \_ PARMS.**](mci-ovly-open-parms.md)

O sinalizador adicional a seguir é usado com o **tipo de dispositivo waveaudio:**

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>BUFFER ABERTO DO MCI \_ WAVE \_ \_
</dt> <dd>

Um comprimento de buffer é especificado no **membro dwBufferSeconds** da estrutura identificada por *lpOpen.*

</dd> </dl>

Para dispositivos waveform-audio, o *parâmetro lpOpen* aponta para uma [**estrutura MCI WAVE OPEN \_ \_ \_ PARMS.**](mci-wave-open-parms.md) O driver MCIWAVE requer um dispositivo assíncrono waveform-audio.

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

 

