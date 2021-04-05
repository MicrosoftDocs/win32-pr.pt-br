---
title: comando put
description: O comando put define a área da imagem de origem e a janela de destino usadas para exibição. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- comando put multimídia do Windows
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086231"
---
# <a name="put-command"></a>comando put

O comando put define a área da imagem de origem e a janela de destino usadas para exibição. Dispositivos de vídeo digital e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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
| digitalvideo | destino de destino no quadro de quadro do *retângulo* na fonte de origem do *retângulo* no *retângulo* | vídeo em vídeo na janela de janela do *retângulo* na janela do *retângulo* cliente da janela do cliente no *retângulo* |
| overlay      | destino de destino no quadro de quadro do *retângulo* no *retângulo*                             | fonte de origem no vídeo de vídeo de *retângulo* no *retângulo*                                           |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszRegions** e seus significados.



| Valor                        | Significado                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destino                  | Seleciona toda a área do cliente da janela de destino para exibir os dados.                                                                                                                                                                                                                                                                         |
| destino no *retângulo*   | Seleciona uma parte da área do cliente da janela de destino usada para exibir a imagem. Quando uma área da janela de exibição é especificada e o dispositivo dá suporte à ampliação, a imagem de origem é esticada para o deslocamento e a extensão de destino.                                                                                                     |
| frame                        | Seleciona o buffer de quadro inteiro para receber as imagens de vídeo de entrada.                                                                                                                                                                                                                                                                                 |
| quadro no *retângulo*         | Seleciona uma parte do buffer de quadro para receber as imagens de vídeo de entrada.                                                                                                                                                                                                                                                                           |
| source                       | Seleciona a imagem inteira para exibição na janela de destino.                                                                                                                                                                                                                                                                                       |
| fonte no *retângulo*        | Seleciona uma parte da imagem a ser exibida na janela de destino. Quando uma área da imagem de origem é especificada e o dispositivo dá suporte à ampliação, a imagem de origem é esticada para o deslocamento e a extensão de destino.                                                                                                                           |
| video                        | Seleciona a imagem de vídeo de entrada inteira a ser capturada no buffer de quadro.                                                                                                                                                                                                                                                                               |
| vídeo no *retângulo*         | Seleciona uma parte da imagem de vídeo de entrada a ser capturada no buffer de quadro.                                                                                                                                                                                                                                                                         |
| janela                       | Restaura o tamanho inicial da janela na exibição. Esse comando também exibe a janela.                                                                                                                                                                                                                                                               |
| janela no *retângulo*        | Altera o tamanho e o local da janela de exibição. O retângulo especificado é relativo à janela pai da janela de exibição (normalmente a área de trabalho) se o sinalizador "estilo filho" tiver sido usado para o comando [abrir](open.md) . Para alterar o local da janela sem alterar sua altura ou largura, especifique zero para a altura e a largura. |
| cliente do Windows                | Restaura a área do cliente da janela.                                                                                                                                                                                                                                                                                                               |
| cliente de janela no *retângulo* | Altera o tamanho e o local da área do cliente da janela. O retângulo especificado é relativo à janela pai da janela do cliente. Para alterar o local da janela sem alterar sua altura ou largura, especifique zero para a altura e a largura.                                                                                      |



 

Quando um sinalizador inclui um retângulo, as coordenadas do retângulo são relativas à origem da janela ou à origem da imagem, conforme apropriado, e são especificadas como **X1 Y1 x2 y2**. As coordenadas **X1Y1** especificam o canto superior esquerdo e as coordenadas **X2Y2** especificam a largura e a altura do retângulo.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O comando put define um ou mais dos seguintes retângulos ao trabalhar com dispositivos de sobreposição de vídeo:

-   O retângulo de vídeo define a região da imagem de vídeo de entrada a ser capturada.
-   O retângulo do quadro define a região do buffer de quadro que recebe a imagem de vídeo de entrada.
-   O retângulo de origem define qual região do buffer de quadro é copiada para o retângulo de destino.
-   O retângulo de destino define a região da área do cliente da janela de exibição que recebe a imagem de vídeo.

O retângulo de vídeo está relacionado ao retângulo do quadro da mesma maneira que o retângulo de origem está relacionado ao retângulo de destino. O alongamento pode ocorrer do retângulo de vídeo para o retângulo de quadro e do retângulo de origem para o retângulo de destino. Nem todos os dispositivos dão suporte ao alongamento, e o alongamento deve ser habilitado (usando o comando [set](set.md) ).

O comando a seguir define três regiões para o vídeo, o quadro e a fonte.

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

As regiões neste exemplo são definidas da seguinte maneira:

-   Uma região de 200 a 200 pixels dos dados de vídeo de entrada, começando com uma origem 120 pixels no canto superior esquerdo, será capturada para o buffer de quadro.
-   Os dados de vídeo serão colocados em uma região de 200 por 200 pixels no canto superior esquerdo do buffer de quadros.
-   São feitas transferências da região 200-por 200 pixels no canto superior esquerdo do buffer de quadro para a janela de destino.

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

[open](open.md)
</dt> <dt>

[set](set.md)
</dt> </dl>

 

