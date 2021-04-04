---
title: comando fechar (Corecrt \_ Io. h)
description: O comando fechar fecha o dispositivo ou arquivo e todos os recursos associados. O MCI descarrega um dispositivo quando todas as instâncias do dispositivo ou todos os arquivos são fechados. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- fechar o comando multimídia do Windows
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
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918329"
---
# <a name="close-command"></a>comando fechar

O comando fechar fecha o dispositivo ou arquivo e todos os recursos associados. O MCI descarrega um dispositivo quando todas as instâncias do dispositivo ou todos os arquivos são fechados. Todos os dispositivos MCI reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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

Pode ser "Wait", "notificar" ou ambos. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Para fechar todos os dispositivos abertos pelo seu aplicativo, especifique o identificador de dispositivo "todos" para o parâmetro *lpszDeviceID* .

Fechar o dispositivo **cdaudio** para a reprodução de áudio.

**Windows 2000/XP:** Se o dispositivo **cdaudio** estiver em execução, fechar o dispositivo **cdaudio** não fará com que o áudio pare de ser executado. Envie o comando [Stop](stop.md) primeiro.

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
| Cabeçalho<br/>                   | <dl> <dt>Corecrt \_ Io. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

