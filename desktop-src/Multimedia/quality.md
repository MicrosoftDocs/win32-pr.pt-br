---
title: comando de qualidade
description: O comando de qualidade define um nível de qualidade personalizado para a compactação de dados de áudio, vídeo ou ainda de imagem. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cc920ec9-362c-43db-808e-b9fb59d1df6d
keywords:
- comando de qualidade Windows multimídia
topic_type:
- apiref
api_name:
- quality
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50f019b0e89f21d792f75c13e6c8e755486009d38d242878fec3121333fb9af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372321"
---
# <a name="quality-command"></a>comando de qualidade

O comando de qualidade define um nível de qualidade personalizado para a compactação de dados de áudio, vídeo ou ainda de imagem. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("quality %s %s %s"), 
  lpszDeviceID, 
  lpszQuality, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszQuality"></span><span id="lpszquality"></span><span id="LPSZQUALITY"></span>*lpszQuality*
</dt> <dd>

Um ou mais dos sinalizadores a seguir. (Um dos três sinalizadores "áudio", "ainda" e "vídeo" deve estar presente.)



| Valor                 | Significado                                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *algoritmo* de algoritmo | Associa o nível de qualidade ao *algoritmo* especificado. Esse *algoritmo* deve ser suportado pelo dispositivo e ser compatível com o sinalizador "áudio", "ainda" ou "vídeo" que é usado. Se omitido, o algoritmo atual será usado. |
| *nome* do áudio          | Indica que este comando especifica um nível de qualidade de "áudio" identificado com o *nome*.                                                                                                                                                   |
| diálogo                | Solicita que o dispositivo exiba uma caixa de diálogo. Essa caixa de diálogo tem campos específicos de algoritmo que são usados internamente pelo dispositivo para criar a estrutura que descreve um nível de qualidade específico.                                    |
| *identificador* de identificador       | Especifica um *identificador* para uma estrutura que contém dados específicos de algoritmos que descrevem um nível de qualidade específico. As estruturas para os dados referenciados por esse identificador são específicas do dispositivo.                                         |
| *nome* ainda          | Indica que o comando especifica um nível de qualidade "ainda" identificado com o *nome.*                                                                                                                                                     |
| *nome* do vídeo          | Indica que o comando especifica um nível de qualidade de "vídeo" identificado com o *nome*.                                                                                                                                                     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Este comando define um nome de cadeia de caracteres para o nível de qualidade, que pode ser usado em um comando [setvideo](setvideo.md) "qualidade", setvideo "qualidade [" ou "](setaudio.md) qualidade" para estabelecer o nível de qualidade do vídeo atual, ainda ou de compactação de áudio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[SetAudio](setaudio.md)
</dt> <dt>

[setvideo](setvideo.md)
</dt> </dl>

 

