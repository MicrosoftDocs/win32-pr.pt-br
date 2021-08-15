---
title: comando put
description: O comando put define a área da imagem de origem e da janela de destino usada para exibição. Os dispositivos de vídeo digital e sobreposição de vídeo reconhecem esse comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- comando put Windows Multimídia
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08732b0ed55464fa1a288cc13a9ac19609b480644ffa4c9dfbeb140cedbbd3c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372375"
---
# <a name="put-command"></a>comando put

O comando put define a área da imagem de origem e da janela de destino usada para exibição. Os dispositivos de vídeo digital e sobreposição de vídeo reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*
</dt> <dd>

Sinalizador para definir a área. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando put e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                                                      | Significado                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| digitalvideo | destino de destino no *quadro do retângulo* na fonte de origem do *retângulo* no *retângulo* | vídeo vídeo na janela *do retângulo* no cliente da janela *do* cliente da janela retângulo no *retângulo* |
| overlay      | destino de destino no *quadro do* retângulo no *retângulo*                             | fonte de origem no *vídeo* de retângulo no *retângulo*                                           |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no **parâmetro lpszRegions** e seus significados.



| Valor                        | Significado                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destino                  | Seleciona toda a área de cliente da janela de destino para exibir os dados.                                                                                                                                                                                                                                                                         |
| destino no *retângulo*   | Seleciona uma parte da área do cliente da janela de destino usada para exibir a imagem. Quando uma área da janela de exibição é especificada e o dispositivo dá suporte a alongamento, a imagem de origem é alongada até o deslocamento e a extensão de destino.                                                                                                     |
| frame                        | Seleciona todo o buffer de quadro para receber as imagens de vídeo de entrada.                                                                                                                                                                                                                                                                                 |
| quadro no *retângulo*         | Seleciona uma parte do buffer de quadro para receber as imagens de vídeo de entrada.                                                                                                                                                                                                                                                                           |
| source                       | Seleciona a imagem inteira para exibição na janela de destino.                                                                                                                                                                                                                                                                                       |
| origem no *retângulo*        | Seleciona uma parte da imagem a ser exibida na janela de destino. Quando uma área da imagem de origem é especificada e o dispositivo dá suporte ao alongamento, a imagem de origem é alongada até o deslocamento e a extensão de destino.                                                                                                                           |
| video                        | Seleciona toda a imagem de vídeo de entrada a ser capturada no buffer de quadro.                                                                                                                                                                                                                                                                               |
| vídeo no *retângulo*         | Seleciona uma parte da imagem de vídeo de entrada a ser capturada no buffer de quadro.                                                                                                                                                                                                                                                                         |
| janela                       | Restaura o tamanho inicial da janela na exibição. Esse comando também exibe a janela.                                                                                                                                                                                                                                                               |
| janela no *retângulo*        | Altera o tamanho e o local da janela de exibição. O retângulo especificado será relativo à janela pai da janela de exibição (geralmente a área de trabalho) se o sinalizador "filho de estilo" tiver sido usado para o [comando](open.md) open. Para alterar o local da janela sem alterar sua altura ou largura, especifique zero para a altura e a largura. |
| cliente de janela                | Restaura a área do cliente da janela.                                                                                                                                                                                                                                                                                                               |
| cliente de janela no *retângulo* | Altera o tamanho e o local da área do cliente da janela. O retângulo especificado é relativo à janela pai da janela do cliente. Para alterar o local da janela sem alterar sua altura ou largura, especifique zero para a altura e a largura.                                                                                      |



 

Quando um sinalizador inclui um retângulo, as coordenadas do retângulo são relativas à origem da janela ou à origem da imagem, conforme apropriado, e são especificadas como **X1 Y1 X2 Y2**. As coordenadas **X1Y1 especificam** o canto superior esquerdo e as coordenadas **X2Y2** especificam a largura e a altura do retângulo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O comando put define um ou mais dos retângulos a seguir ao trabalhar com dispositivos de sobreposição de vídeo:

-   O retângulo de vídeo define a região da imagem de vídeo de entrada a ser capturada.
-   O retângulo de quadro define a região do buffer de quadro que recebe a imagem de vídeo de entrada.
-   O retângulo de origem define qual região do buffer de quadro é copiada para o retângulo de destino.
-   O retângulo de destino define a região da área de cliente da janela de exibição que recebe a imagem de vídeo.

O retângulo de vídeo está relacionado ao retângulo de quadro da mesma maneira que o retângulo de origem está relacionado ao retângulo de destino. O alongamento pode ocorrer do retângulo de vídeo para o retângulo do quadro e do retângulo de origem para o retângulo de destino. Nem todos os dispositivos são compatíveis com alongamento e o alongamento deve ser habilitado (usando o [comando set).](set.md)

O comando a seguir define três regiões para o vídeo, o quadro e a origem.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

As regiões neste exemplo são definidas da seguinte forma:

-   Uma região de 200 por 200 pixels dos dados de vídeo de entrada, começando em uma origem de 120 pixels do canto superior esquerdo, será capturada no buffer de quadros.
-   Os dados de vídeo serão colocados em uma região de 200 por 200 pixels no canto superior esquerdo do buffer de quadros.
-   As transferências são feitas da região de 200 por 200 pixels no canto superior esquerdo do buffer de quadros para a janela de destino.

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

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

