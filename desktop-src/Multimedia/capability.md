---
title: comando de funcionalidade
description: O comando Capability solicita informações sobre um recurso específico de um dispositivo. Todos os dispositivos MCI reconhecem este comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- Multimídia do Windows de comando de funcionalidade
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a6ac87b98fb8d748a5baf2665cc5a63230b6a98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454810"
---
# <a name="capability-command"></a>comando de funcionalidade

O comando Capability solicita informações sobre um recurso específico de um dispositivo. Todos os dispositivos MCI reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capability %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszRequest"></span><span id="lpszrequest"></span><span id="LPSZREQUEST"></span>*lpszRequest*
</dt> <dd>

Sinalizador que identifica uma funcionalidade de dispositivo. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **capacidade** e os sinalizadores usados por cada tipo:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Tipo</th>
<th>Tipo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>cdaudio</td>
<td><ul>
<li>pode ejetar</li>
<li>pode reproduzir</li>
<li>pode registrar</li>
<li>pode salvar</li>
<li>dispositivo composto</li>
</ul></td>
<td><ul>
<li>tipo de dispositivo</li>
<li>com áudio</li>
<li>tem vídeo</li>
<li>usa arquivos</li>
</ul></td>
</tr>
<tr class="even">
<td>digitalvideo</td>
<td><ul>
<li>pode ejetar</li>
<li>pode congelar</li>
<li>pode bloquear</li>
<li>pode reproduzir</li>
<li>pode registrar</li>
<li>pode reverter</li>
<li>pode salvar</li>
<li>pode ampliar</li>
<li>pode ampliar a entrada</li>
<li>pode testar</li>
</ul></td>
<td><ul>
<li>dispositivo composto</li>
<li>tipo de dispositivo</li>
<li>com áudio</li>
<li>ainda</li>
<li>tem vídeo</li>
<li>taxa de execução máxima</li>
<li>taxa mínima de execução</li>
<li>usa arquivos</li>
<li>usa paletas</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="odd">
<td>overlay</td>
<td><ul>
<li>pode ejetar</li>
<li>pode congelar</li>
<li>pode reproduzir</li>
<li>pode registrar</li>
<li>pode salvar</li>
<li>pode ampliar</li>
</ul></td>
<td><ul>
<li>dispositivo composto</li>
<li>tipo de dispositivo</li>
<li>com áudio</li>
<li>tem vídeo</li>
<li>usa arquivos</li>
<li>windows</li>
</ul></td>
</tr>
<tr class="even">
<td>sequenciador</td>
<td><ul>
<li>pode ejetar</li>
<li>pode reproduzir</li>
<li>pode registrar</li>
<li>pode salvar</li>
<li>dispositivo composto</li>
</ul></td>
<td><ul>
<li>tipo de dispositivo</li>
<li>com áudio</li>
<li>tem vídeo</li>
<li>usa arquivos</li>
</ul></td>
</tr>
<tr class="odd">
<td>videocassete</td>
<td><ul>
<li>pode detectar comprimento</li>
<li>pode ejetar</li>
<li>pode congelar</li>
<li>pode monitorar fontes</li>
<li>pode reproduzir</li>
<li>pode ser prevertido</li>
<li>pode Visualizar</li>
<li>pode registrar</li>
<li>pode reverter</li>
<li>pode salvar</li>
<li>pode testar</li>
</ul></td>
<td><ul>
<li>taxa de incremento de relógio</li>
<li>dispositivo composto</li>
<li>tipo de dispositivo</li>
<li>com áudio</li>
<li>tem relógio</li>
<li>tem código de paficação</li>
<li>tem vídeo</li>
<li>número de marcas</li>
<li>precisão da busca</li>
<li>usa arquivos</li>
</ul></td>
</tr>
<tr class="even">
<td>videodisc</td>
<td><ul>
<li>pode ejetar</li>
<li>pode reproduzir</li>
<li>pode registrar</li>
<li>pode reverter</li>
<li>pode salvar</li>
<li>CAV</li>
<li>CLV</li>
<li>dispositivo composto</li>
</ul></td>
<td><ul>
<li>tipo de dispositivo</li>
<li>taxa de reprodução rápida</li>
<li>com áudio</li>
<li>tem vídeo</li>
<li>taxa de reprodução normal</li>
<li>taxa de reprodução lenta</li>
<li>usa arquivos</li>
</ul></td>
</tr>
<tr class="odd">
<td>waveaudio</td>
<td><ul>
<li>pode ejetar</li>
<li>pode reproduzir</li>
<li>pode registrar</li>
<li>pode salvar</li>
<li>dispositivo composto</li>
<li>tipo de dispositivo</li>
</ul></td>
<td><ul>
<li>com áudio</li>
<li>tem vídeo</li>
<li>entradas</li>
<li>outputs</li>
<li>usa arquivos</li>
</ul></td>
</tr>
</tbody>
</table>



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszRequest* e seus significados:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>pode detectar comprimento</td>
<td>Retornará <strong>true</strong> se o dispositivo puder detectar o comprimento da mídia.</td>
</tr>
<tr class="even">
<td>pode ejetar</td>
<td>Retornará <strong>true</strong> se o dispositivo puder ejetar a mídia.</td>
</tr>
<tr class="odd">
<td>pode congelar</td>
<td>Retornará <strong>true</strong> se o dispositivo puder congelar dados no buffer de quadros.</td>
</tr>
<tr class="even">
<td>pode bloquear</td>
<td>Retornará <strong>true</strong> se o dispositivo puder bloquear dados.</td>
</tr>
<tr class="odd">
<td>pode monitorar fontes</td>
<td>Retornará <strong>true</strong> se o dispositivo puder passar uma entrada (origem) para a saída monitorada, independentemente da seleção de entrada atual.</td>
</tr>
<tr class="even">
<td>pode reproduzir</td>
<td>Retornará <strong>true</strong> se o dispositivo puder ser executado.</td>
</tr>
<tr class="odd">
<td>pode ser prevertido</td>
<td>Retornará <strong>true</strong> se o dispositivo der suporte ao &quot; sinalizador preroll &quot; com o comando <a href="cue.md">Cue</a> .</td>
</tr>
<tr class="even">
<td>pode Visualizar</td>
<td>Retornará <strong>true</strong> se o dispositivo oferecer suporte a visualizações.</td>
</tr>
<tr class="odd">
<td>pode registrar</td>
<td>Retornará <strong>true</strong> se o dispositivo der suporte à gravação.</td>
</tr>
<tr class="even">
<td>pode reverter</td>
<td>Retornará <strong>true</strong> se o dispositivo puder reproduzir em ordem inversa.</td>
</tr>
<tr class="odd">
<td>pode salvar</td>
<td>Retornará <strong>true</strong> se o dispositivo puder salvar dados.</td>
</tr>
<tr class="even">
<td>pode ampliar</td>
<td>Retornará <strong>true</strong> se o dispositivo puder alongar quadros para preencher um determinado retângulo de exibição.</td>
</tr>
<tr class="odd">
<td>pode ampliar a entrada</td>
<td>Retornará <strong>true</strong> se o dispositivo puder redimensionar uma imagem no processo de digitalização no buffer de quadros.</td>
</tr>
<tr class="even">
<td>pode testar</td>
<td>Retornará <strong>true</strong> se o dispositivo reconhecer a palavra-chave test.</td>
</tr>
<tr class="odd">
<td>cav</td>
<td>Quando combinado com outros itens, esse sinalizador especifica que as informações de retorno se aplicam ao formato CAV videodiscs. Esse será o padrão se nenhum VIDEODISC for inserido.</td>
</tr>
<tr class="even">
<td>taxa de incremento de relógio</td>
<td>Retorna o número de subdivisãos com suporte do relógio externo por segundo. Se o relógio externo for um relógio de milissegundo, o valor de retorno será 1000. Se o valor de retorno for 0, não haverá suporte para nenhum relógio.</td>
</tr>
<tr class="odd">
<td>clv</td>
<td>Quando combinado com outros itens, esse sinalizador especifica que as informações de retorno se aplicam ao formato CLV videodiscs.</td>
</tr>
<tr class="even">
<td>dispositivo composto</td>
<td>Retornará <strong>true</strong> se o dispositivo der suporte a um nome de elemento (filename).</td>
</tr>
<tr class="odd">
<td>tipo de dispositivo</td>
<td>Retorna um nome de tipo de dispositivo, que pode ser um dos seguintes:
<ul>
<li>cdaudio</li>
<li>DATs</li>
<li>digitalvideo</li>
<li>outros</li>
<li>overlay</li>
<li>verificador</li>
<li>sequenciador</li>
<li>videocassete</li>
<li>videodisc</li>
<li>waveaudio</li>
</ul></td>
</tr>
<tr class="even">
<td>taxa de reprodução rápida</td>
<td>Retorna a taxa de reprodução rápida em quadros por segundo ou zero se o dispositivo não puder ser executado rapidamente.</td>
</tr>
<tr class="odd">
<td>com áudio</td>
<td>Retornará <strong>true</strong> se o dispositivo der suporte à reprodução de áudio.</td>
</tr>
<tr class="even">
<td>tem relógio</td>
<td>Retornará <strong>true</strong> se o dispositivo tiver um relógio.</td>
</tr>
<tr class="odd">
<td>ainda</td>
<td>Retornará <strong>true</strong> se o dispositivo tratar arquivos com uma única imagem com mais eficiência do que arquivos de vídeo de movimento.</td>
</tr>
<tr class="even">
<td>tem código de paficação</td>
<td>Retornará <strong>true</strong> se o dispositivo for capaz de dar suporte ao código de Code ou se for desconhecido.</td>
</tr>
<tr class="odd">
<td>tem vídeo</td>
<td>Retornará <strong>true</strong> se o dispositivo der suporte a vídeo.</td>
</tr>
<tr class="even">
<td>entradas</td>
<td>Retorna o número total de dispositivos de entrada.</td>
</tr>
<tr class="odd">
<td>taxa de execução máxima</td>
<td>Retorna a taxa de execução máxima, em quadros por segundo, para o dispositivo.</td>
</tr>
<tr class="even">
<td>taxa mínima de execução</td>
<td>Retorna a taxa mínima de reprodução, em quadros por segundo, para o dispositivo.</td>
</tr>
<tr class="odd">
<td>taxa de reprodução normal</td>
<td>Retorna a taxa de reprodução normal, em quadros por segundo, para o dispositivo.</td>
</tr>
<tr class="even">
<td>número de marcas</td>
<td>Retorna o número máximo de marcas que podem ser usadas; zero indica que não há suporte para marcas.</td>
</tr>
<tr class="odd">
<td>outputs</td>
<td>Retorna o número total de dispositivos de saída.</td>
</tr>
<tr class="even">
<td>precisão da busca</td>
<td>Retorna a precisão esperada de uma pesquisa em quadros; 0 indica que o dispositivo é preciso de quadro, 1 indica que o dispositivo espera estar dentro de um quadro da posição de busca indicada e assim por diante.</td>
</tr>
<tr class="odd">
<td>taxa de reprodução lenta</td>
<td>Retorna a taxa de reprodução lenta em quadros por segundo ou zero se o dispositivo não puder ser executado lentamente.</td>
</tr>
<tr class="even">
<td>usa arquivos</td>
<td>Retornará <strong>true</strong> se o armazenamento de dados usado por um dispositivo composto for um arquivo.</td>
</tr>
<tr class="odd">
<td>usa paletas</td>
<td>Retornará <strong>true</strong> se o dispositivo usar paletas.</td>
</tr>
<tr class="even">
<td>windows</td>
<td>Retorna o número de janelas de exibição simultâneas às quais o dispositivo pode dar suporte.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna informações no parâmetro *lpszReturnString* da função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) . As informações dependem do tipo de solicitação.

## <a name="examples"></a>Exemplos

O comando a seguir retorna o tipo de dispositivo do dispositivo "mysound".

``` syntax
capability mysound device type
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

[advertência](cue.md)
</dt> </dl>

 

