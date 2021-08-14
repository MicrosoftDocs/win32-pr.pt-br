---
title: Comando unfreeze
description: O comando unfreeze reaables video acquisition to the frame buffer after it's been disabled by the freeze command. Os dispositivos de vídeo digital, VCR e sobreposição de vídeo reconhecem esse comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- Unfreeze command Windows Multimídia
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fe45b1346872483a4012c5f5d161dcd61020c64349fee254ae4bf337b4be8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370806"
---
# <a name="unfreeze-command"></a>Comando unfreeze

O comando unfreeze reaables video acquisition to the frame buffer after it's been disabled by the [freeze](freeze.md) command. Os dispositivos de vídeo digital, VCR e sobreposição de vídeo reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*
</dt> <dd>

Sinalizador para reablucar a aquisição de vídeo para o buffer de quadro. A tabela a seguir lista os tipos de dispositivo que reconhecem o **comando unfreeze** e os sinalizadores usados por cada tipo.



| Valor        | Significado        |
|--------------|----------------|
| digitalvideo | retângulo *em* |
| overlay      | retângulo *em* |
| Videocassete          | saída de entrada   |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no **parâmetro lpszUnfreeze** e seus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| retângulo *em* | Especifica a região que terá a aquisição de vídeo reaabled. O retângulo é relativo à origem do buffer de vídeo e é especificado como *X1 Y1 X2 Y2*. As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo e as coordenadas *X2 Y2* especificam a largura e a altura. |
| input          | Desaconselhe a imagem de entrada.                                                                                                                                                                                                                                                                  |
| output         | Desaconselhe a imagem de saída. Se nem "entrada" nem "saída" for dado, "saída" será assumida.                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="examples"></a>Exemplos

O comando a seguir desconsincha uma região do buffer de vídeo.

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[Congelar](freeze.md)
</dt> </dl>

 

