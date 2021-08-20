---
title: MCI_LOAD comando (Mmsystem.h)
description: O comando MCI \_ LOAD carrega um arquivo. Os dispositivos de vídeo digital e sobreposição de vídeo reconhecem esse comando.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- MCI_LOAD comando Windows Multimídia
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
ms.openlocfilehash: e318e79bf24e51fec69f97a0dcb56395cb1a8917a31105deae062a865169b778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138534"
---
# <a name="mci_load-command"></a>Comando MCI \_ LOAD

O comando MCI \_ LOAD carrega um arquivo. Os dispositivos de vídeo digital e sobreposição de vídeo reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

MCI \_ NOTIFY, MCI \_ WAIT ou, para dispositivos de vídeo digital, MCI \_ TEST. Para obter informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*lpLoad*
</dt> <dd>

Ponteiro para uma [**estrutura MCI \_ LOAD \_ PARMS.**](mci-load-parms.md) (Dispositivos com parâmetros adicionais podem substituir essa estrutura por uma estrutura específica do dispositivo. Para dispositivos de vídeo digital, o **parâmetro lpLoad** aponta para uma [**estrutura MCI \_ DGV \_ LOAD \_ PARMS.)**](/previous-versions//dd743391(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O sinalizador adicional a seguir se aplica a todos os dispositivos que suportam mci \_ load:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>ARQUIVO DE \_ CARREGAMENTO MCI \_
</dt> <dd>

O **membro lpfilename** da estrutura identificada por *lpLoad* contém um endereço de um buffer que contém o nome do arquivo.

</dd> </dl>

O sinalizador adicional a seguir é usado com o **tipo de dispositivo de sobreposição:**

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ OVLY \_ RECT
</dt> <dd>

O **membro rc** da estrutura identificada por *lpLoad* contém um retângulo de exibição válido que identifica a área do buffer de vídeo a ser atualizada.

</dd> </dl>

Para dispositivos de sobreposição de vídeo, o *parâmetro lpLoad* aponta para uma estrutura [**MCI \_ OVLY \_ LOAD \_ PARMS.**](mci-ovly-load-parms.md)

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

 

