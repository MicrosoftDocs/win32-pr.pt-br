---
title: comando de indicação
description: O comando de indicação se prepara para reproduzir ou gravar. Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.
ms.assetid: 94fa0d0c-d5c9-4ef1-bb7d-22dfb09a7689
keywords:
- comando de indicação Windows multimídia
topic_type:
- apiref
api_name:
- cue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6398d4773b6c92332e8a95996e4d81941a073fe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467853"
---
# <a name="cue-command"></a>comando de indicação

O comando de indicação se prepara para reproduzir ou gravar. Digital-Video, VCR e Wave-Audio Devices reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cue %s %s %s"), 
  lpszDeviceID, 
  lpszInOutTo, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszInOutTo"></span><span id="lpszinoutto"></span><span id="LPSZINOUTTO"></span>*lpszInOutTo*
</dt> <dd>

Sinalizador que prepara um dispositivo para reprodução ou gravação. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **indicação** e os sinalizadores usados por cada tipo.




| Valor | Indicação | Indicação | 
|-------|-----|-----|
| digitalvideo | <ul><li>input</li><li>noshow</li></ul> | <ul><li>output</li><li>para a <em>posição</em></li></ul> | 
| videocassete | <ul><li>da <em>posição</em></li><li>input</li><li>output</li></ul> | <ul><li>prelance</li><li>reverse</li><li>para a <em>posição</em></li></ul> | 
| waveaudio | input | output | 




 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro *lpszInOutTo* e seus significados.



| Valor           | Significado                                                                                                                                                                                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| da *posição* | Indica onde começar.                                                                                                                                                                                                                                                                                      |
| input           | Prepara para gravação. Para dispositivos de vídeo digital, esse sinalizador poderá ser omitido se a fonte da apresentação atual já for a entrada externa.                                                                                                                                                                  |
| noshow          | Prepara para reproduzir um quadro sem exibi-lo. Quando esse sinalizador é especificado, a exibição continua a mostrar a imagem no buffer de quadro, embora seu quadro correspondente não seja a posição atual. Um comando de indicação subsequente sem esse sinalizador e sem o sinalizador "to" exibe o quadro atual. |
| output          | Prepara para jogar. Se nenhuma "entrada" nem "saída" for especificada, a configuração padrão será "saída".                                                                                                                                                                                                           |
| prelance         | Move a distância de preversão do *ponto em* diante. O ponto de entrada é a posição atual ou a posição especificada pelo sinalizador "de".                                                                                                                                                                            |
| reverse         | Indica que a direção da reprodução está em ordem inversa (retroativa).                                                                                                                                                                                                                                                             |
| para a *posição*   | Move o espaço de trabalho para a posição especificada. Para dispositivos VCR, esse sinalizador indica onde parar.                                                                                                                                                                                                             |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Embora não seja necessário, emitir o comando de indicação antes de reproduzir ou gravar em alguns dispositivos pode reduzir o atraso antes que o dispositivo inicie a ação.

Esse comando falhará se a reprodução ou a gravação estiver em andamento ou se o dispositivo estiver em pausa.

Quando advertência para reprodução (usando a indicação "saída"), emitir o comando [Play](play.md) com o sinalizador "from", "to" ou "Reverse" cancela o comando cue.

Quando advertência para gravação (usando a indicação de "entrada"), a emissão do comando de [registro](record.md) com o sinalizador "de", "para" ou "inicializar" cancela o comando de indicação.

## <a name="examples"></a>Exemplos

O comando a seguir prepara o dispositivo "mysound" para gravação.

``` syntax
cue mysound input
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

[reproduzir](play.md)
</dt> <dt>

[gravável](record.md)
</dt> </dl>

 

