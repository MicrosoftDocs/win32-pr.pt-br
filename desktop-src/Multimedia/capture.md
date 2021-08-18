---
title: Comando capture
description: O comando capture copia o conteúdo do buffer de quadro e o armazena no arquivo especificado. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- comando capture Windows Multimídia
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68bc32fd247cbe3519fbffad778b33679e3b71c652b476f557db5a910e87721c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941514"
---
# <a name="capture-command"></a>Comando capture

O comando capture copia o conteúdo do buffer de quadro e o armazena no arquivo especificado. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*
</dt> <dd>

Um ou mais dos seguintes sinalizadores:



| Valor          | Significado                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| como *pathname*  | Especifica o caminho de destino e o nome do arquivo para a imagem capturada. Esse sinalizador é necessário.                                                                                                                                                                |
| retângulo *em* | Especifica a região retangular dentro do buffer de quadro que o dispositivo cortará e salvará em disco. Se omitido, a região cortada assume como padrão o retângulo especificado ou padrão em um comando [put](put.md) "source" anterior para esta instância do dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify", "test" ou uma combinação deles. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

Esse comando poderá falhar se o dispositivo estiver executando vídeo de movimento no momento ou executando outra operação com uso intensivo de recursos. Se o buffer de quadro estiver sendo atualizado em tempo real, a atualização pausa momentaneamente para que uma imagem completa seja capturada. Se o dispositivo pausar a atualização, poderá haver um efeito visual ou audível. Se o formato de arquivo, o algoritmo de compactação e os níveis de qualidade não foram definidos, seus padrões serão usados.

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

[Colocar](put.md)
</dt> </dl>

 

