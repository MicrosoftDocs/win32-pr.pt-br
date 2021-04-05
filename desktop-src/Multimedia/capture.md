---
title: comando de captura
description: O comando Capture copia o conteúdo do buffer de quadro e o armazena no arquivo especificado. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- Multimídia do Windows de comando de captura
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086302"
---
# <a name="capture-command"></a>comando de captura

O comando Capture copia o conteúdo do buffer de quadro e o armazena no arquivo especificado. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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
| como *nome do caminho*  | Especifica o caminho de destino e o nome do arquivo para a imagem capturada. Esse sinalizador é necessário.                                                                                                                                                                |
| no *retângulo* | Especifica a região retangular dentro do buffer de quadro que o dispositivo corta e salva em disco. Se omitido, a região cortada usa como padrão o retângulo especificado ou padronizado em um comando "Source" de [Put](put.md) anterior para essa instância de dispositivo. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Esse comando poderá falhar se o dispositivo estiver executando o vídeo de movimento no momento ou executando alguma outra operação de uso intensivo de recursos. Se o buffer de quadros estiver sendo atualizado em tempo real, a atualização pausará momentaneamente para que uma imagem completa seja capturada. Se o dispositivo pausar a atualização, poderá haver um efeito visual ou audível. Se o formato de arquivo, o algoritmo de compactação e os níveis de qualidade não tiverem sido definidos, seus padrões serão usados.

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

[Posicione](put.md)
</dt> </dl>

 

