---
title: comando Where
description: O comando Where recupera o retângulo especificando a área de origem ou de destino. Esse retângulo foi especificado usando o comando put. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- como multimídia do Windows de comando
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919007"
---
# <a name="where-command"></a>comando Where

O comando Where recupera o retângulo especificando a área de origem ou de destino. Esse retângulo foi especificado usando o comando [Put](put.md) . Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*
</dt> <dd>

Sinalizador que identifica o retângulo cujas dimensões são recuperadas. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Where** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                       | Significado                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| digitalvideo | destinationdestination [**Max**](max.md)frameFrame maxsource | maxvideovideo de origem maxwindowwindow Max |
| overlay      | destinationframe                                              | sourcevideo                              |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRequestRect** e seus significados.



| Valor                          | Significado                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destino                    | Recupera a extensão e o deslocamento de destino. Para dispositivos de sobreposição de vídeo, o retângulo de destino define a área da área do cliente da janela de exibição que exibe os dados da imagem do buffer de quadro.                                                                                             |
| [ **máximo** de destino](max.md) | Recupera o tamanho atual do retângulo do cliente.                                                                                                                                                                                                                                                  |
| frame                          | Recupera o deslocamento e a extensão do retângulo do buffer do quadro. O retângulo do buffer de quadro define a área do buffer de quadro que recebe dados de vídeo recebidos. As imagens do retângulo "vídeo" são dimensionadas para essa região.                                                                     |
| [ **máximo** do quadro](max.md)       | Retorna o tamanho máximo do buffer de quadro.                                                                                                                                                                                                                                                        |
| source                         | Recupera o deslocamento e a extensão da origem. Para dispositivos de sobreposição de vídeo, o retângulo de origem define a região do buffer de quadro que é exibido na janela de destino. O dispositivo usa esse retângulo para cortar a imagem antes que ela seja ampliada para se ajustar ao retângulo de destino na exibição. |
| fonte [ **máxima**](max.md)      | Recupera o tamanho máximo do buffer de quadro.                                                                                                                                                                                                                                                      |
| video                          | Recupera o deslocamento e a extensão do retângulo de vídeo. O retângulo de vídeo define a região dos dados de vídeo de entrada que são transferidos para o buffer de quadros.                                                                                                                                   |
| [ **máximo** de vídeo](max.md)       | Retorna o tamanho máximo da entrada.                                                                                                                                                                                                                                                               |
| janela                         | Recupera o tamanho atual e a posição do quadro da janela de exibição.                                                                                                                                                                                                                                 |
| janela [ **máxima**](max.md)      | Recupera o tamanho da tela inteira.                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um retângulo no parâmetro *lpszReturnString* da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . O retângulo descreve a área especificada no parâmetro *lpszRequestRect* deste comando. O retângulo é especificado como *X1 Y1 x2 y2*. As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *x2 y2* especificam a largura e a altura.

## <a name="examples"></a>Exemplos

O comando a seguir retorna o retângulo de exibição do dispositivo de "filme".

``` syntax
where movie destination
```

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

 

