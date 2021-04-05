---
title: comando Recortar
description: O comando Recortar remove dados do espaço de trabalho e os copia para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- comando Recortar multimídia do Windows
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33571309e1dd249f20e577c97b8c6e1b950eda09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918956"
---
# <a name="cut-command"></a>comando Recortar

O comando Recortar remove dados do espaço de trabalho e os copia para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("cut %s %s %s"), 
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

Um dos sinalizadores a seguir que identificam o item a ser recortado.



| Valor                 | Significado                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo*        | Especifica a parte de cada corte de quadro. Se for omitido, o padrão será o quadro inteiro. Quando esse item é especificado, os quadros não são excluídos. Em vez disso, a área dentro do retângulo se torna preta.                                       |
| *fluxo* de fluxo de áudio | Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando. Se você usar esse sinalizador e também quiser recortar o vídeo, também deverá usar o sinalizador "fluxo de vídeo". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão recortados.) |
| da *posição*       | Especifica o início do intervalo de recorte. Se for omitido, o padrão será a posição atual.                                                                                                                                                |
| para a *posição*         | Especifica o fim do intervalo de recorte. Os dados de áudio e vídeo recortados são exclusivos dessa posição. Se omitido, o padrão será o final do espaço de trabalho.                                                                                  |
| *fluxo* de fluxo de vídeo | Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando. Se você usar esse sinalizador e também quiser cortar o áudio, também deverá usar o sinalizador "fluxo de áudio". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão recortados.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

A alteração se torna permanente somente quando os dados são explicitamente salvos; no entanto, a reprodução funciona como se os dados tiverem sido removidos.

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

 

