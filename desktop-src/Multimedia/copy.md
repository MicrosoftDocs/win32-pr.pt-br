---
title: comando de cópia
description: O comando de cópia copia dados para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- comando de cópia multimídia do Windows
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f08c764cb12b1cdca4c1876e6a22220a5c7522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644399"
---
# <a name="copy-command"></a>comando de cópia

O comando de cópia copia dados para a área de transferência. Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("copy %s %s %s"), 
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

Um dos sinalizadores a seguir que identificam o item a ser copiado.



| Valor                 | Significado                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| no *retângulo*        | Especifica a parte de cada quadro que será copiada. Se omitido, a configuração padrão será o quadro inteiro.                                                                                                                             |
| *fluxo* de fluxo de áudio | Especifica o fluxo de áudio no espaço de trabalho afetado pelo comando. Se você usar esse sinalizador e também quiser copiar o vídeo, também deverá usar o sinalizador "fluxo de vídeo". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão copiados.) |
| da *posição*       | Especifica o início do intervalo copiado. Se omitido, a configuração padrão será a posição atual.                                                                                                                                         |
| para a *posição*         | Especifica o fim do intervalo copiado. Os dados de áudio e vídeo copiados são exclusivos dessa posição. Se omitido, a configuração padrão será o final do espaço de trabalho.                                                                       |
| *fluxo* de fluxo de vídeo | Especifica o fluxo de vídeo no espaço de trabalho afetado pelo comando. Se você usar esse sinalizador e também quiser copiar áudio, também deverá usar o sinalizador "fluxo de áudio". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão copiados.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "Notify", "Test" ou uma combinação desses. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

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

 

