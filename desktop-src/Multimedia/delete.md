---
title: Excluir comando
description: O comando Excluir exclui um segmento de dados de um arquivo. Os dispositivos digital-video e Wave-Audio reconhecem este comando.
ms.assetid: 9cf084f6-d64e-4487-9407-b68502b7cec9
keywords:
- excluir o comando multimídia do Windows
topic_type:
- apiref
api_name:
- delete
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e356d4972384e676f2e521bd2ca102bb21d7ef2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824737"
---
# <a name="delete-command"></a>Excluir comando

O comando Excluir exclui um segmento de dados de um arquivo. Os dispositivos digital-video e Wave-Audio reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("delete %s %s %s"), 
  lpszDeviceID, 
  lpszPosition, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszPosition"></span><span id="lpszposition"></span><span id="LPSZPOSITION"></span>*lpszPosition*
</dt> <dd>

Sinalizador que identifica um segmento de dados a ser excluído. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **exclusão** e os sinalizadores usados por cada tipo.



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
<td><ul>
<li>no <em>retângulo</em></li>
<li><em>fluxo</em> de fluxo de áudio</li>
<li>da <em>posição</em></li>
</ul></td>
<td><ul>
<li>para a <em>posição</em></li>
<li><em>fluxo</em> de fluxo de vídeo</li>
</ul></td>
</tr>
<tr class="even">
<td>waveaudio</td>
<td>da <em>posição</em></td>
<td>para a <em>posição</em></td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszPosition* e seus significados.



| Valor                 | Significado                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo*        | Especifica a parte de cada quadro excluída. Se for omitido, o padrão será o quadro inteiro. Quando esse item é especificado, os quadros não são excluídos. Em vez disso, a área dentro do retângulo se torna preta.                                          |
| *fluxo* de fluxo de áudio | Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando. Se você usar esse sinalizador e também quiser excluir o vídeo, também deverá usar o sinalizador "fluxo de vídeo". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão excluídos.) |
| da *posição*       | Especifica a posição na qual começa a exclusão. Se esse sinalizador for omitido, a exclusão começará na posição atual.                                                                                                                       |
| para a *posição*         | Especifica a posição na qual termina a exclusão. Se esse sinalizador for omitido, a exclusão continuará no final do conteúdo ou espaço de trabalho.                                                                                                       |
| *fluxo* de fluxo de vídeo | Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando. Se você usar esse sinalizador e também quiser excluir áudio, também deverá usar o sinalizador "fluxo de áudio". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão excluídos.)     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Antes de emitir comandos que usam valores de posição, você deve definir o formato de hora desejado usando o comando [set](set.md) .

## <a name="examples"></a>Exemplos

O comando a seguir exclui os dados de forma de onda-áudio de 1 milissegundo a 900 milissegundos (supondo que o formato de hora seja definido como milissegundos).

``` syntax
delete mysound from 1 to 900
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

[set](set.md)
</dt> </dl>

 

