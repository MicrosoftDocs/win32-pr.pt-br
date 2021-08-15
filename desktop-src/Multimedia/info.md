---
title: comando info
description: O comando info recupera uma descrição de hardware de um dispositivo. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: cdd6628b-bff8-4a0d-9dad-a63321f584ea
keywords:
- comando de informações Windows multimídia
topic_type:
- apiref
api_name:
- info
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f15675923f37a80ce694a400f18113f5178a54a3f75664008644919c6d9fc128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690466"
---
# <a name="info-command"></a>comando info

O comando info recupera uma descrição de hardware de um dispositivo. Todos os dispositivos MCI reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("info %s %s %s"), 
  lpszDeviceID, 
  lpszInfoType, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszInfoType"></span><span id="lpszinfotype"></span><span id="LPSZINFOTYPE"></span>*lpszInfoType*
</dt> <dd>

Sinalizador que identifica o tipo de informação necessário. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **info** e os sinalizadores usados por cada tipo.



| Valor        | Significado                                                             | Significado                                             |
|--------------|---------------------------------------------------------------------|-----------------------------------------------------|
| cdaudio      | informações identityinfo UPC                                               | product                                             |
| digitalvideo | áudio algorithmaudio qualityfileproductstill algorithmstill Quality | usageversionvideo algorithmvideo qualitywindow Text |
| overlay      | produto                                                         | texto da janela                                         |
| sequenciador    | copyrightfile                                                       | nameproduct                                         |
| videocassete          | product                                                             | version                                             |
| videodisk    | product                                                             |                                                     |
| waveaudio    | entrada de dados                                                           | outputproduct                                       |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszInfoType** e seus significados.



| Valor           | Significado                                                                                                                                                                                            |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algoritmo de áudio | Retorna o nome do algoritmo de compactação de áudio atual.                                                                                                                                       |
| qualidade de áudio   | Retorna o nome do descritor de qualidade de áudio atual. Isso pode retornar "desconhecido" se o aplicativo tiver definido parâmetros para valores específicos que não correspondam a qualidades definidas.       |
| direitos autorais       | Recupera o aviso de direitos autorais do arquivo MIDI do evento meta de direitos autorais.                                                                                                                            |
| file            | Recupera o nome do arquivo usado pelo dispositivo composto. Se o dispositivo for aberto sem um arquivo e o comando de [carregamento](load.md) não tiver sido usado, uma cadeia de caracteres nula será retornada.                  |
| identidade de informações   | Produz um identificador exclusivo para o CD de áudio atualmente carregado no Player que está sendo consultado.                                                                                                        |
| UPC de informações        | Produz o código do produto universal (UPC) que é codificado em um CD de áudio. O UPC é uma cadeia de caracteres de dígitos. Ele pode não estar disponível para todos os CDs.                                                    |
| input           | Recupera a descrição do dispositivo de entrada atual. Retorna "None" se um dispositivo de entrada não estiver definido.                                                                                               |
| name            | Recupera o nome da sequência do evento meta de nome de sequência/faixa.                                                                                                                               |
| output          | Recupera a descrição do dispositivo de saída atual. Retorna "None" se um dispositivo de saída não estiver definido.                                                                                             |
| product         | Recupera uma descrição do dispositivo. Essas informações geralmente incluem o nome do produto e o modelo. O comprimento da cadeia de caracteres será de 31 caracteres ou menos.                                               |
| algoritmo ainda | Retorna o nome do algoritmo de compactação de imagem ainda atual.                                                                                                                                 |
| qualidade ainda   | Retorna o nome do descritor de qualidade da imagem atual ainda. Isso pode retornar "desconhecido" se o aplicativo tiver definido parâmetros para valores específicos que não correspondam a qualidades definidas. |
| uso           | Retorna uma cadeia de caracteres que descreve as restrições de uso que podem ser impostas pelo proprietário dos dados visuais ou de áudio no espaço de trabalho.                                                                    |
| version         | Retorna o nível de versão do driver de dispositivo e do hardware.                                                                                                                                       |
| algoritmo de vídeo | Retorna o nome do algoritmo de compactação de vídeo atual.                                                                                                                                       |
| qualidade de vídeo   | Retorna o nome do descritor de qualidade de vídeo atual. Isso pode retornar "desconhecido" se o aplicativo tiver definido parâmetros para valores específicos que não correspondam a qualidades definidas.       |
| texto da janela     | Recupera a legenda da janela usada pelo dispositivo.                                                                                                                                            |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="examples"></a>Exemplos

O comando a seguir recupera uma descrição do hardware associado ao dispositivo "mysound".

``` syntax
info mysound product
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

[carga](load.md)
</dt> </dl>

 

