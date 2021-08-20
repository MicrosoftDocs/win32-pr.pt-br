---
title: Comando list
description: O comando list determina o número e os tipos de entradas de vídeo e áudio. Os dispositivos de vídeo digital e VCR reconhecem este comando.
ms.assetid: b3fe3819-0b8a-4de5-9c79-03e1e089436f
keywords:
- comando de lista Windows multimídia
topic_type:
- apiref
api_name:
- list
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8881c85d146ce869e41d234a72190901135d233f8e45d580d5f568c4ccc48da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139469"
---
# <a name="list-command"></a>Comando list

O comando list determina o número e os tipos de entradas de vídeo e áudio. Os dispositivos de vídeo digital e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("list %s %s %s"), 
  lpszDeviceID, 
  lpszList, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszList"></span><span id="lpszlist"></span><span id="LPSZLIST"></span>*lpszList*
</dt> <dd>

Sinalizador que identifica o número e os tipos de entradas de vídeo e áudio. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **lista** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                                           | Significado                                                                                                                      |
|--------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| digitalvideo | *algoritmo* de algoritmo de qualidade de áudio algorithmaudio áudio streamcountnumber *índice* | algoritmo de algoritmo de qualidade *algorithmstill vídeo algorithmvideo* *algoritmo* de algoritmo de qualidade de vídeo, monitor SourceVideo Stream |
| videocassete          | *índice* de número de origem de fonte de áudio countaudio                                     | *índice* de número de origem do countvideo de origem de vídeo                                                                                |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszList** e seus significados.



| Valor                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de áudio                     | Especifica que o comando deve recuperar os nomes de algoritmos de áudio.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* de algoritmo de qualidade de áudio | Especifica que o comando deve recuperar os níveis de qualidade associados ao *algoritmo* especificado. Se o *algoritmo* for "atual", o nível de qualidade do algoritmo atual será retornado.                                                                                                                                                                                                                                                                                                   |
| contagem de fontes de áudio                  | Retorna o número total de entradas de áudio.                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| *índice* de número de fonte de áudio         | Retorna o tipo de entrada de áudio do *índice* de origem.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| fluxo de áudio                        | Especifica que o comando deve recuperar os nomes dos fluxos de áudio associados ao espaço de trabalho. Essas cadeias de caracteres (como "inglês" ou "alemão") são inseridas no arquivo e identificam o fluxo.                                                                                                                                                                                                                                                                                    |
| count                               | Retorna o número de opções do tipo especificado.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| *índice* de número                      | Retorna uma cadeia de caracteres que descreve uma opção específica (conforme identificado pelo *índice*) do tipo de opção especificado. O *índice* deve ser um inteiro entre 1 e o valor retornado por "Count".                                                                                                                                                                                                                                                                                                         |
| algoritmo ainda                     | Especifica que o comando deve recuperar os nomes de algoritmos ainda.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* de algoritmo de qualidade ainda | Especifica que o comando deve recuperar os níveis de qualidade associados ao *algoritmo* ainda especificado. Se o *algoritmo* for "atual", o nível de qualidade do algoritmo atual será retornado.                                                                                                                                                                                                                                                                                             |
| algoritmo de vídeo                     | Especifica que o comando deve recuperar os nomes de algoritmos de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *algoritmo* de algoritmo de qualidade de vídeo | Especifica que o comando deve recuperar os níveis de qualidade associados ao *algoritmo* de vídeo especificado. Se o *algoritmo* for "atual", o nível de qualidade do algoritmo atual será retornado.                                                                                                                                                                                                                                                                                             |
| fonte de vídeo                        | Especifica que o comando deve retornar informações sobre as fontes de vídeo. Quando usado com o sinalizador "Count", ele retorna o número de fontes de vídeo. Quando usado com o sinalizador "Number", ele retorna o tipo de uma fonte de vídeo. O MCI define as seguintes constantes para o tipo: "NTSC", "RGB", "PAL", "secam", "SVIDEO" e "Generic". Pode haver mais de uma fonte de cada tipo retornada. O tipo de origem "genérico" é usado quando mais de um sinal é permitido para esse conector. |
| contagem de fontes de vídeo                  | Retorna o número total de entradas de vídeo.                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *índice* de número de origem do vídeo         | Retorna o tipo de entrada de vídeo do *índice* de origem.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| fluxo de vídeo                        | Especifica que o comando deve recuperar os nomes dos fluxos de vídeo associados ao espaço de trabalho. Essas cadeias de caracteres (como "fim de engraçado" ou "fim de triste") são inseridas no arquivo e identificam o fluxo.                                                                                                                                                                                                                                                                               |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify" ou "Test". Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Para dispositivos VCR, uma "fonte de vídeo" ou "fonte de áudio" deve ser especificada com os sinalizadores "Count" ou "Number". Se "Count" for especificado, o número total de entradas de vídeo ou áudio será retornado. Se "Number" for especificado, o driver retornará um tipo correspondente à entrada. O tipo pode ser qualquer um dos seguintes: "TUNER", "line", "SVIDEO", "AUX" ou "Generic". Normalmente, você deve primeiro consultar o VCR para a "contagem" e, em seguida, usar a contagem como o intervalo para o sinalizador "número". Os números de "origem" começam de 1.

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
</dt> </dl>

 

