---
title: comando capability
description: O comando de funcionalidade solicita informações sobre uma funcionalidade específica de um dispositivo. Todos os dispositivos MCI reconhecem esse comando.
ms.assetid: 1b470473-0de6-41ba-9f6e-41f0b13ceaeb
keywords:
- comando capability Windows Multimídia
topic_type:
- apiref
api_name:
- capability
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44e57a793f799214753f50504d80bce7051fba14
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469153"
---
# <a name="capability-command"></a>comando capability

O comando de funcionalidade solicita informações sobre uma funcionalidade específica de um dispositivo. Todos os dispositivos MCI reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

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

Sinalizador que identifica uma funcionalidade do dispositivo. A tabela a seguir lista os tipos de dispositivo que reconhecem **o comando de funcionalidade** e os sinalizadores usados por cada tipo:




| Valor | Tipo | Tipo | 
|-------|------|------|
| cdaudio | <ul><li>pode ejetar</li><li>pode reproduzir</li><li>pode registrar</li><li>pode salvar</li><li>dispositivo composto</li></ul> | <ul><li>tipo de dispositivo</li><li>tem áudio</li><li>tem vídeo</li><li>usa arquivos</li></ul> | 
| digitalvideo | <ul><li>pode ejetar</li><li>pode congelar</li><li>pode bloquear</li><li>pode reproduzir</li><li>pode registrar</li><li>pode reverter</li><li>pode salvar</li><li>pode alongar</li><li>pode alongar a entrada</li><li>pode testar</li></ul> | <ul><li>dispositivo composto</li><li>tipo de dispositivo</li><li>tem áudio</li><li>ainda tem</li><li>tem vídeo</li><li>taxa de reprodução máxima</li><li>taxa de reprodução mínima</li><li>usa arquivos</li><li>usa paletas</li><li>windows</li></ul> | 
| overlay | <ul><li>pode ejetar</li><li>pode congelar</li><li>pode reproduzir</li><li>pode registrar</li><li>pode salvar</li><li>pode alongar</li></ul> | <ul><li>dispositivo composto</li><li>tipo de dispositivo</li><li>tem áudio</li><li>tem vídeo</li><li>usa arquivos</li><li>windows</li></ul> | 
| sequenciador | <ul><li>pode ejetar</li><li>pode reproduzir</li><li>pode registrar</li><li>pode salvar</li><li>dispositivo composto</li></ul> | <ul><li>tipo de dispositivo</li><li>tem áudio</li><li>tem vídeo</li><li>usa arquivos</li></ul> | 
| Videocassete | <ul><li>pode detectar comprimento</li><li>pode ejetar</li><li>pode congelar</li><li>pode monitorar fontes</li><li>pode reproduzir</li><li>pode pré-fazer o pré-roll</li><li>pode visualizar</li><li>pode registrar</li><li>pode reverter</li><li>pode salvar</li><li>pode testar</li></ul> | <ul><li>taxa de incremento do relógio</li><li>dispositivo composto</li><li>tipo de dispositivo</li><li>tem áudio</li><li>tem relógio</li><li>tem código de hora</li><li>tem vídeo</li><li>número de marcas</li><li>precisão de busca</li><li>usa arquivos</li></ul> | 
| videodisc | <ul><li>pode ejetar</li><li>pode reproduzir</li><li>pode registrar</li><li>pode reverter</li><li>pode salvar</li><li>CAV</li><li>CLV</li><li>dispositivo composto</li></ul> | <ul><li>tipo de dispositivo</li><li>taxa de reprodução rápida</li><li>tem áudio</li><li>tem vídeo</li><li>taxa de reprodução normal</li><li>taxa de reprodução lenta</li><li>usa arquivos</li></ul> | 
| Waveaudio | <ul><li>pode ejetar</li><li>pode reproduzir</li><li>pode registrar</li><li>pode salvar</li><li>dispositivo composto</li><li>tipo de dispositivo</li></ul> | <ul><li>tem áudio</li><li>tem vídeo</li><li>entradas</li><li>outputs</li><li>usa arquivos</li></ul> | 




 

A tabela a seguir lista os sinalizadores que podem ser especificados no *parâmetro lpszRequest* e seus significados:




| Flags | Significado | 
|-------|---------|
| pode detectar comprimento | Retornará <strong>TRUE</strong> se o dispositivo puder detectar o comprimento da mídia. | 
| pode ejetar | Retornará <strong>TRUE</strong> se o dispositivo puder ejetar a mídia. | 
| pode congelar | Retornará <strong>TRUE</strong> se o dispositivo puder congelar dados no buffer de quadro. | 
| pode bloquear | Retornará <strong>TRUE</strong> se o dispositivo puder bloquear dados. | 
| pode monitorar fontes | Retornará <strong>TRUE</strong> se o dispositivo puder passar uma entrada (origem) para a saída monitorada, independentemente da seleção de entrada atual. | 
| pode reproduzir | Retornará <strong>TRUE</strong> se o dispositivo puder reproduzir. | 
| pode pré-fazer o pré-roll | Retornará <strong>TRUE</strong> se o dispositivo for compatível com o sinalizador "preroll" com o <a href="cue.md">comando de indicação.</a> | 
| pode visualizar | Retornará <strong>TRUE</strong> se o dispositivo for compatível com visualizações. | 
| pode registrar | Retornará <strong>TRUE</strong> se o dispositivo for compatível com a gravação. | 
| pode reverter | Retornará <strong>TRUE</strong> se o dispositivo puder reproduzir em ordem inversa. | 
| pode salvar | Retornará <strong>TRUE</strong> se o dispositivo puder salvar dados. | 
| pode alongar | Retornará <strong>TRUE</strong> se o dispositivo puder alongar quadros para preencher um retângulo de exibição específico. | 
| pode alongar a entrada | Retornará <strong>TRUE</strong> se o dispositivo puder ressarcimento de uma imagem no processo de digitá-la no buffer de quadro. | 
| pode testar | Retornará <strong>TRUE</strong> se o dispositivo reconhecer a palavra-chave test. | 
| Cav | Quando combinado com outros itens, esse sinalizador especifica que as informações de retorno se aplica a videodiscs de formato DECOD. Esse será o padrão se nenhum videodisc for inserido. | 
| taxa de incremento do relógio | Retorna o número de subdivisões que o relógio externo dá suporte por segundo. Se o relógio externo for um relógio de milissegundos, o valor de retorno será 1000. Se o valor de retorno for 0, nenhum relógio será suportado. | 
| clv | Quando combinado com outros itens, esse sinalizador especifica que as informações de retorno se aplica a videodiscs de formato CLV. | 
| dispositivo composto | Retornará <strong>TRUE</strong> se o dispositivo for compatível com um nome de elemento (nome do arquivo). | 
| tipo de dispositivo | Retorna um nome de tipo de dispositivo, que pode ser um dos seguintes:<ul><li>cdaudio</li><li>Dat</li><li>digitalvideo</li><li>other</li><li>overlay</li><li>verificador</li><li>sequenciador</li><li>Videocassete</li><li>videodisc</li><li>Waveaudio</li></ul> | 
| taxa de reprodução rápida | Retorna a taxa de reprodução rápida em quadros por segundo ou zero se o dispositivo não puder reproduzir rapidamente. | 
| tem áudio | Retornará <strong>TRUE</strong> se o dispositivo for compatível com reprodução de áudio. | 
| tem relógio | Retornará <strong>TRUE</strong> se o dispositivo tiver um relógio. | 
| ainda tem | Retornará <strong>TRUE</strong> se o dispositivo tratar arquivos com uma única imagem com mais eficiência do que arquivos de vídeo de movimento. | 
| tem código de hora | Retornará <strong>TRUE</strong> se o dispositivo for capaz de dar suporte ao código de tempo ou se for desconhecido. | 
| tem vídeo | Retornará <strong>TRUE</strong> se o dispositivo for compatível com vídeo. | 
| entradas | Retorna o número total de dispositivos de entrada. | 
| taxa de reprodução máxima | Retorna a taxa de reprodução máxima, em quadros por segundo, para o dispositivo. | 
| taxa de reprodução mínima | Retorna a taxa de reprodução mínima, em quadros por segundo, para o dispositivo. | 
| taxa de reprodução normal | Retorna a taxa de reprodução normal, em quadros por segundo, para o dispositivo. | 
| número de marcas | Retorna o número máximo de marcas que podem ser usadas; zero indica que não há suporte para marcas. | 
| outputs | Retorna o número total de dispositivos de saída. | 
| precisão de busca | Retorna a precisão esperada de uma pesquisa em quadros; 0 indica que o dispositivo tem um quadro preciso, 1 indica que o dispositivo espera estar dentro de um quadro da posição de busca indicada e assim por diante. | 
| taxa de reprodução lenta | Retorna a taxa de reprodução lenta em quadros por segundo ou zero se o dispositivo não puder reproduzir lentamente. | 
| usa arquivos | Retornará <strong>TRUE</strong> se o armazenamento de dados usado por um dispositivo composto for um arquivo. | 
| usa paletas | Retornará <strong>TRUE</strong> se o dispositivo usar paletas. | 
| windows | Retorna o número de janelas de exibição simultâneas que o dispositivo pode dar suporte. | 




 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital e VCR, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna informações no *parâmetro lpszReturnString* da [**função mciSendString.**](/previous-versions//dd757161(v=vs.85)) As informações dependem do tipo de solicitação.

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

[Cue](cue.md)
</dt> </dl>

 

