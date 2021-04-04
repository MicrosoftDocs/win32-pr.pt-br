---
title: comando colar
description: O comando Paste copia o conteúdo da área de transferência no espaço de trabalho. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: c09418e1-2535-40d1-8912-e5ece91ee673
keywords:
- comando colar multimídia do Windows
topic_type:
- apiref
api_name:
- paste
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482fd744d7e6e163059330148b6e3f081d435880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009054"
---
# <a name="paste-command"></a>comando colar

O comando Paste copia o conteúdo da área de transferência no espaço de trabalho. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("paste %s %s %s"), 
  lpszDeviceID, 
  lpszItem, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*lpszItem*
</dt> <dd>

Um ou mais dos sinalizadores a seguir.



| Valor                 | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo*        | Especifica o local dentro do quadro onde os dados são colados. O canto superior esquerdo do *retângulo* corresponde ao canto superior esquerdo dos dados adicionados. Se o retângulo tiver um tamanho diferente de zero em X ou Y, o conteúdo da área de transferência será dimensionado nessas dimensões quando eles forem colados no quadro. Se omitido, o *retângulo* assume como padrão o quadro inteiro. Se esse sinalizador for especificado no modo de "inserção" (o padrão), qualquer região fora do retângulo será pintada como uma cor sólida.                       |
| *fluxo* de fluxo de áudio | Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando. Se houver apenas um fluxo de áudio na área de transferência, os dados de áudio serão colados no *fluxo* designado. Se houver mais de um fluxo de áudio na área de transferência, o *fluxo* indicará o número inicial para as sequências de fluxo. Se você usar esse sinalizador e também quiser colar o vídeo, também deverá usar o sinalizador "fluxo de vídeo". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados e manterão seus números de fluxo originais.) |
| insert                | Especifica que os dados são inseridos no espaço de trabalho. Todos os dados após o ponto de inserção são movidos para frente no espaço de trabalho para liberar espaço. Esse é o valor padrão.                                                                                                                                                                                                                                                                                                                                                    |
| overwrite             | Especifica que os dados são copiados no espaço de trabalho por meio da gravação de todos os dados existentes após o ponto de inserção. Os sinalizadores "Inserir" e "substituir" afetam se os quadros são destruídos ou movidos durante a operação de colagem, e não como os dados são colados dentro de cada quadro.                                                                                                                                                                                                                                              |
| para a *posição*         | Especifica a posição no espaço de trabalho em que os dados são colados. Se for omitido, o padrão será a posição atual.                                                                                                                                                                                                                                                                                                                                                                                                    |
| *fluxo* de fluxo de vídeo | Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando. Se houver apenas um fluxo de vídeo na área de transferência, os dados de vídeo serão colados no *fluxo* designado. Se houver mais de um fluxo de vídeo na área de transferência, o *fluxo* indicará o número inicial para as sequências de fluxo. Se você usar esse sinalizador e também quiser colar o áudio, também deverá usar o sinalizador "fluxo de áudio". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão colados e manterão seus números de fluxo originais.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Não há sinais presentes nos dados copiados da área de transferência. A alteração se torna permanente somente quando os dados são explicitamente salvos; no entanto, a reprodução age como se os dados tiverem sido adicionados.

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

 

