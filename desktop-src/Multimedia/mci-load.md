---
title: MCI_LOAD comando (mmsystem. h)
description: O comando de carregamento do MCI \_ carrega um arquivo. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- Multimídia do Windows de comando MCI_LOAD
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb00ebe9dc9107c4673fc323fcb7719a89beffd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917974"
---
# <a name="mci_load-command"></a>Comando de carregamento do MCI \_

O comando de carregamento do MCI \_ carrega um arquivo. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
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

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Ponteiro para uma estrutura de [**\_ \_ parâmetros de carga MCI**](mci-load-parms.md) . (Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo. Para dispositivos de vídeo digital, o parâmetro **lpLoad** aponta para uma estrutura de [**\_ \_ \_ parâmetros de carga DGV MCI**](/previous-versions//dd743391(v=vs.85)) .)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O seguinte sinalizador adicional se aplica a todos os dispositivos que dão suporte à \_ carga MCI:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_arquivo de carregamento MCI \_
</dt> <dd>

O membro **lpFileName** da estrutura identificada por *lpLoad* contém um endereço de um buffer que contém o nome do arquivo.

</dd> </dl>

O seguinte sinalizador adicional é usado com o tipo de dispositivo de **sobreposição** :

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>\_OVLY \_ Rect MCI
</dt> <dd>

O membro **RC** da estrutura identificada por *lpLoad* contém um retângulo de exibição válido que identifica a área do buffer de vídeo a ser atualizada.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o parâmetro *lpLoad* aponta para uma estrutura de [**\_ \_ \_ parâmetros de carga OVLY MCI**](mci-ovly-load-parms.md) .

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

 

