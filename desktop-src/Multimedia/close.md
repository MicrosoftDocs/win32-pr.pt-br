---
title: Comando close (Corecrt \_ io.h)
description: O comando close fecha o dispositivo ou o arquivo e todos os recursos associados. A MCI descarrega um dispositivo quando todas as instâncias do dispositivo ou todos os arquivos são fechados. Todos os dispositivos MCI reconhecem esse comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- Fechar comando Windows Multimídia
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02acd3ebe3d45a402ae565c6fcac121f712df4374924bcb0e02c3dcadf9ceeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807955"
---
# <a name="close-command"></a>Comando close

O comando close fecha o dispositivo ou o arquivo e todos os recursos associados. A MCI descarrega um dispositivo quando todas as instâncias do dispositivo ou todos os arquivos são fechados. Todos os dispositivos MCI reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Para fechar todos os dispositivos abertos pelo seu aplicativo, especifique o identificador de dispositivo "all" para *o parâmetro lpszDeviceID.*

Fechar o **dispositivo cdaudio** interrompe a reprodução de áudio.

**Windows 2000/XP:** Se o **dispositivo cdaudio** estiver sendo acionado, fechar o **dispositivo cdaudio** não faz com que o áudio pare de tocar. Envie o [comando stop](stop.md) primeiro.

## <a name="examples"></a>Exemplos

O comando a seguir fecha o dispositivo "mysound".

``` syntax
close mysound
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Corecrt \_ io.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

