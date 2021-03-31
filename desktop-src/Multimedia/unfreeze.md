---
title: descongelar comando
description: O comando descongelar reabilita a aquisição de vídeo para o buffer de quadro após ele ter sido desabilitado pelo comando Freeze. Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- descongelar multimídia do Windows de comando
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645164"
---
# <a name="unfreeze-command"></a>descongelar comando

O comando descongelar reabilita a aquisição de vídeo para o buffer de quadro após ele ter sido desabilitado pelo comando [Freeze](freeze.md) . Dispositivos digitais de vídeo, VCR e de sobreposição de vídeo reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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

Sinalizador para reabilitar a aquisição de vídeo para o buffer de quadros. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **descongelar** e os sinalizadores usados por cada tipo.



| Valor        | Significado        |
|--------------|----------------|
| digitalvideo | no *retângulo* |
| overlay      | no *retângulo* |
| videocassete          | saída de entrada   |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszUnfreeze** e seus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo* | Especifica a região que terá a aquisição de vídeo reativada. O retângulo é relativo à origem do buffer de vídeo e é especificado como *X1 Y1 x2 y2*. As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *x2 y2* especificam a largura e a altura. |
| input          | Descongele a imagem de entrada.                                                                                                                                                                                                                                                                  |
| output         | Descongele a imagem de saída. Se nem "Input" nem "output" for fornecido, "output" será assumido.                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="examples"></a>Exemplos

O comando a seguir destrava uma região do buffer de vídeo.

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[Trave](freeze.md)
</dt> </dl>

 

