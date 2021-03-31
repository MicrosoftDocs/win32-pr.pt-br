---
title: MCI_OPEN comando (mmsystem. h)
description: O \_ comando MCI abrir Inicializa um dispositivo ou arquivo. Todos os dispositivos reconhecem este comando.
ms.assetid: e2ee92b5-b10b-4408-950e-3002fe775b25
keywords:
- Multimídia do Windows de comando MCI_OPEN
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
ms.openlocfilehash: 14d8b33e70a2e061b54260aeffc6e69432c469f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824144"
---
# <a name="mci_open-command"></a>Comando de abertura do MCI \_

O \_ comando MCI abrir Inicializa um dispositivo ou arquivo. Todos os dispositivos reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Notificação MCI ou \_ espera MCI. Para obter informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpOpen"></span><span id="lpopen"></span><span id="LPOPEN"></span>*lpOpen*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros abertos do MCI**](mci-open-parms.md) . (Dispositivos com conjuntos de comandos estendidos podem substituir essa estrutura por uma estrutura específica do dispositivo.)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O \_ sinalizador de tipo Open do MCI \_ deve ser usado sempre que um dispositivo é especificado na função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Se você abrir um dispositivo especificando uma constante do tipo de dispositivo, deverá especificar o sinalizador de \_ ID de tipo aberto MCI, \_ além do \_ tipo de abertura de MCI \_ \_ . Para obter uma lista de constantes de tipo de dispositivo, consulte [tipos de dispositivo MCI](mci-device-types.md).

Se o \_ sinalizador de compartilhamento aberto do MCI \_ não for especificado quando um dispositivo ou arquivo for aberto inicialmente, todos os \_ comandos de abertura do MCI subsequentes para o dispositivo ou arquivo falharão. Se o dispositivo ou arquivo já estiver aberto e esse sinalizador não for especificado, a chamada falhará mesmo que o primeiro comando aberto especificado por MCI seja \_ \_ compartilhável. Arquivos abertos para o MCISEQ. DRV e MCIWAVE. Os dispositivos DRV não são compartilháveis.

O caso é ignorado no nome do dispositivo, mas não pode haver espaços em branco à esquerda ou à direita.

Para usar a seleção automática de tipo (por meio das entradas no registro), atribua o nome de arquivo e a extensão de arquivos ao membro **lpstrElementName** da estrutura identificada por *lpOpen*, defina o membro **lpstrDeviceType** como **nulo** e defina o \_ sinalizador de elemento abrir do MCI \_ .

Os seguintes sinalizadores adicionais se aplicam a todos os dispositivos que oferecem suporte a MCI \_ Open:

<dl> <dt>

<span id="MCI_OPEN_ALIAS"></span><span id="mci_open_alias"></span>\_alias de abrir MCI \_
</dt> <dd>

Um alias é incluído no membro **lpstrAlias** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_SHAREABLE"></span><span id="mci_open_shareable"></span>MCI \_ aberto \_ compartilhável
</dt> <dd>

O dispositivo ou arquivo deve ser aberto como compartilhável.

</dd> <dt>

<span id="MCI_OPEN_TYPE"></span><span id="mci_open_type"></span>tipo de MCI \_ aberto \_
</dt> <dd>

Um nome de tipo de dispositivo ou constante está incluído no membro **lpstrDeviceType** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_TYPE_ID"></span><span id="mci_open_type_id"></span>\_ID do \_ tipo \_ Open do MCI
</dt> <dd>

A palavra de ordem inferior do membro **lpstrDeviceType** da estrutura identificada por *lpOpen* contém um identificador de tipo de dispositivo MCI padrão e a palavra de ordem superior, opcionalmente, contém o índice ordinal para o dispositivo. Use esse sinalizador com o \_ sinalizador de tipo aberto do MCI \_ .

</dd> </dl>

Os seguintes sinalizadores adicionais se aplicam a dispositivos compostos:

<dl> <dt>

<span id="MCI_OPEN_ELEMENT"></span><span id="mci_open_element"></span>\_elemento MCI Open \_
</dt> <dd>

Um nome de arquivo é incluído no membro **lpstrElementName** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OPEN_ELEMENT_ID"></span><span id="mci_open_element_id"></span>\_ID do \_ elemento de abertura do MCI \_
</dt> <dd>

O membro **lpstrElementName** da estrutura identificada por *lpOpen* é interpretado como um valor **DWORD** e tem significado interno para o dispositivo. Use esse sinalizador com o \_ sinalizador de \_ elemento MCI Open.

</dd> </dl>

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo **DigitalVideo** :

<dl> <dt>

<span id="MCI_DGV_OPEN_NOSTATIC"></span><span id="mci_dgv_open_nostatic"></span>\_DGV MCI \_ abrir \_ noestático
</dt> <dd>

O dispositivo deve reduzir o número de cores estáticas (do sistema) na paleta. Isso aumenta o número de cores disponíveis para renderizar o fluxo de vídeo. Esse sinalizador se aplica somente a dispositivos que compartilham uma paleta com o Windows.

</dd> <dt>

<span id="MCI_DGV_OPEN_PARENT"></span><span id="mci_dgv_open_parent"></span>DGV do MCI \_ \_ abrir \_ pai
</dt> <dd>

O identificador de janela pai é especificado no membro **hwndParent** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_WS"></span><span id="mci_dgv_open_ws"></span>\_DGV MCI \_ abrir \_ WS
</dt> <dd>

Um estilo de janela é especificado no membro **dwStyle** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_DGV_OPEN_16BIT"></span><span id="mci_dgv_open_16bit"></span>MCI \_ DGV \_ abrir \_ 16 bits
</dt> <dd>

Indica uma preferência para o suporte a dispositivos MCI de 16 bits.

</dd> <dt>

<span id="MCI_DGV_OPEN_32BIT"></span><span id="mci_dgv_open_32bit"></span>MCI \_ DGV \_ abrir \_ 32 bits
</dt> <dd>

Indica uma preferência para o suporte a dispositivos MCI de 32 bits.

</dd> </dl>

Para dispositivos de vídeo digital, o parâmetro *lpOpen* aponta para uma estrutura de [**\_ \_ \_ parâmetros Open parms DGV MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_open_parmsa) .

Os seguintes sinalizadores adicionais são usados com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_OPEN_PARENT"></span><span id="mci_ovly_open_parent"></span>OVLY do MCI \_ \_ abrir \_ pai
</dt> <dd>

O identificador de janela pai é especificado no membro **hwndParent** da estrutura identificada por *lpOpen*.

</dd> <dt>

<span id="MCI_OVLY_OPEN_WS"></span><span id="mci_ovly_open_ws"></span>\_OVLY MCI \_ abrir \_ WS
</dt> <dd>

Um estilo de janela é especificado no membro **dwStyle** da estrutura identificada por *lpOpen*. O valor **dwStyle** especifica o estilo da janela que o driver criará e exibirá se o aplicativo não fornecer um. O parâmetro Style usa um inteiro que define o estilo da janela. Essas constantes são as mesmas que os estilos de janela padrão (como WS \_ -Child, WS \_ OVERLAPPEDWINDOW ou WS \_ popup).

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpOpen* aponta para uma estrutura de [**\_ \_ \_ parâmetros Open parms OVLY MCI**](mci-ovly-open-parms.md) .

O seguinte sinalizador adicional é usado com o tipo de dispositivo **WaveAudio** :

<dl> <dt>

<span id="MCI_WAVE_OPEN_BUFFER"></span><span id="mci_wave_open_buffer"></span>\_ \_ buffer aberto do MCI Wave \_
</dt> <dd>

Um comprimento de buffer é especificado no membro **dwBufferSeconds** da estrutura identificada por *lpOpen*.

</dd> </dl>

Para dispositivos de formato de onda-áudio, o parâmetro *lpOpen* aponta para uma estrutura [**MCI de \_ \_ Open \_ parms de Wave**](mci-wave-open-parms.md) . O driver MCIWAVE requer um dispositivo de áudio de onda assíncrono.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

