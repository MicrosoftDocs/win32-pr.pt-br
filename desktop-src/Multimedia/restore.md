---
title: Comando restore
description: O comando restore copia uma imagem still de um arquivo para o buffer de quadro. Esse é o inverso do comando de captura. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- comando restore Windows Multimídia
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e82fdec2480cfe2fc1b41901872aef7e41ee468d1adc3924df17a27e40031e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689186"
---
# <a name="restore-command"></a>Comando restore

O comando restore copia uma imagem still de um arquivo para o buffer de quadro. Esse é o inverso do comando [de](capture.md) captura. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*
</dt> <dd>

Um ou mais dos sinalizadores a seguir.



| Valor           | Significado                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| retângulo *em*  | Especifica um retângulo relativo à origem do buffer de quadro. O *retângulo* é especificado como *X1 Y1 X2 Y2*. As coordenadas *X1 Y1 especificam* o canto superior esquerdo e as coordenadas *X2 Y2* especificam a largura e a altura. Se esse sinalizador não for usado, a imagem será copiada para o canto superior esquerdo do buffer de quadros.<br/> |
| de *nome de arquivo* | Especifica o nome do arquivo de imagem a ser lembrado. Esse sinalizador é necessário.                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify", "test" ou uma combinação deles. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Os dispositivos podem reconhecer uma variedade de formatos de imagem; um Windows bitmap independente de dispositivo sempre é reconhecido.

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

[Capturar](capture.md)
</dt> </dl>

 

