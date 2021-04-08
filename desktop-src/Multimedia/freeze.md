---
title: congelar comando
description: O comando Freeze congela a entrada de vídeo ou a saída de vídeo em um videocassete ou desabilita a aquisição de vídeo para o buffer de quadros. Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.
ms.assetid: 49f3ab98-e893-402a-be78-6140af3b81df
keywords:
- congelar multimídia do Windows de comando
topic_type:
- apiref
api_name:
- freeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b63fbb2d888fc1ca315c0b511bcb18224c8168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008840"
---
# <a name="freeze-command"></a>congelar comando

O comando Freeze congela a entrada de vídeo ou a saída de vídeo em um videocassete ou desabilita a aquisição de vídeo para o buffer de quadros. Dispositivos de vídeo digital, de sobreposição de vídeo e VCR reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("freeze %s %s %s"), 
  lpszDeviceID, 
  lpszFreezeFlags, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszFreezeFlags"></span><span id="lpszfreezeflags"></span><span id="LPSZFREEZEFLAGS"></span>*lpszFreezeFlags*
</dt> <dd>

Sinalizador que identifica o que congelar. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando **Freeze** e os sinalizadores usados por cada tipo.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>digitalvideo</td>
<td>no <em>retângulo</em></td>
<td>exterior</td>
</tr>
<tr class="even">
<td>overlay</td>
<td>no <em>retângulo</em></td>

</tr>
<tr class="odd">
<td>videocassete</td>
<td><ul>
<li>field</li>
<li>frame</li>
</ul></td>
<td><ul>
<li>input</li>
<li>output</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszFreezeFlags* e seus significados.



| Valor          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo* | Especifica a região que será congelada. Para dispositivos de sobreposição de vídeo, essa região terá a aquisição de vídeo desabilitada. Para dispositivos de vídeo digital, os pixels dentro do retângulo terão seu bit de máscara de bloqueio ativado (a menos que o sinalizador "externo" seja especificado). O retângulo é relativo à origem do buffer de vídeo e é especificado como *X1 Y1 x2 y2*. As coordenadas *X1 Y1* especificam o canto superior esquerdo do retângulo, e as coordenadas *x2 y2* especificam a largura e a altura. |
| field          | Congela o primeiro campo. O campo é assumido por padrão (se nenhum quadro nem campo for especificado).                                                                                                                                                                                                                                                                                                                                                                                               |
| frame          | Congela o quadro inteiro, exibindo os dois campos.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| input          | Congela o quadro atual da imagem de entrada, se está em pausa ou em execução.                                                                                                                                                                                                                                                                                                                                                                                                                |
| output         | Congela o quadro atual da saída do VCR. Se o VCR estiver sendo executado quando congelar for emitido, o quadro atual será congelado e o VCR será pausado. Se o VCR estiver em pausa quando esse comando for emitido, o quadro atual será congelado. A imagem congelada permanece no dispositivo de saída até que um comando de [descongelamento](unfreeze.md) seja emitido. Se nem "Input" nem "output" for especificado, "output" será assumido.                                                                                    |
| exterior        | Indica que a área fora da região especificada usando o sinalizador "at" está congelada.                                                                                                                                                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Quando usado com dispositivos VCR, esse comando destina-se a cartões de captura de quadros.

Para especificar regiões de aquisição irregular com o sinalizador "at", use uma série de comandos congelar e [descongelar](unfreeze.md) . Alguns dispositivos de sobreposição de vídeo limitam a complexidade da região de aquisição.

Esse comando só terá suporte se uma chamada para o comando [Capability](capability.md) com o sinalizador "pode congelar" retornar **true**.

## <a name="examples"></a>Exemplos

O comando a seguir desabilita a aquisição de vídeo em um quadrado de 100 pixels no canto superior esquerdo do buffer de vídeo.

``` syntax
freeze vboard at 0 0 100 100
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

[capability](capability.md)
</dt> <dt>

[descongelar](unfreeze.md)
</dt> </dl>

 

