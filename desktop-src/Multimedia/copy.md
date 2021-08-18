---
title: comando copy
description: O comando copy copia dados para a área de transferência. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: 4f7b5be6-12c3-43a0-bac9-19eb49384330
keywords:
- comando copy Windows Multimídia
topic_type:
- apiref
api_name:
- copy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3d103aae14b9dc13bb0d7d210d0412db993210bc788fa7fedd1a48a7216d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144779"
---
# <a name="copy-command"></a>comando copy

O comando copy copia dados para a área de transferência. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

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

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*Lpszitem*
</dt> <dd>

Um dos sinalizadores a seguir identificando o item a ser copiado.



| Valor                 | Significado                                                                                                                                                                                                                                   |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| retângulo *em*        | Especifica a parte de cada quadro que será copiada. Se omitido, a configuração padrão será o quadro inteiro.                                                                                                                             |
| fluxo de fluxo de *áudio* | Especifica o fluxo de áudio no workspace afetado pelo comando. Se você usar esse sinalizador e também quiser copiar vídeo, também deverá usar o sinalizador "fluxo de vídeo". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão copiados.) |
| da *posição*       | Especifica o início do intervalo copiado. Se omitido, a configuração padrão será a posição atual.                                                                                                                                         |
| para *posicionar*         | Especifica o final do intervalo copiado. Os dados de áudio e vídeo copiados são exclusivos dessa posição. Se omitido, a configuração padrão será o final do workspace.                                                                       |
| fluxo de fluxo de *vídeo* | Especifica o fluxo de vídeo no workspace afetado pelo comando. Se você usar esse sinalizador e também quiser copiar áudio, também deverá usar o sinalizador "fluxo de áudio". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão copiados.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify", "test" ou uma combinação deles. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

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
</dt> </dl>

 

