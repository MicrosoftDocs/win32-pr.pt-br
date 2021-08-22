---
title: comando cut
description: O comando cut remove dados do workspace e os copia para a área de transferência. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: f42c7364-49cb-41be-b601-bda6e97d1e76
keywords:
- comando cut Windows Multimídia
topic_type:
- apiref
api_name:
- cut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a39010ad7dd07ccff38291441bb0aa05a54ee65da1b865d7ac82ed77fbfdd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144559"
---
# <a name="cut-command"></a>comando cut

O comando cut remove dados do workspace e os copia para a área de transferência. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

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

<span id="lpszItem"></span><span id="lpszitem"></span><span id="LPSZITEM"></span>*Lpszitem*
</dt> <dd>

Um dos sinalizadores a seguir identificando o item a ser cortado.



| Valor                 | Significado                                                                                                                                                                                                                               |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| retângulo *em*        | Especifica a parte de cada corte de quadro. Se omitido, ele assume como padrão todo o quadro. Quando esse item é especificado, os quadros não são excluídos. Em vez disso, a área dentro do retângulo se torna preta.                                       |
| fluxo de fluxo de *áudio* | Especifica o fluxo de áudio no workspace afetado pelo comando. Se você usar esse sinalizador e também quiser recortar vídeo, também deverá usar o sinalizador "fluxo de vídeo". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão cortados.) |
| da *posição*       | Especifica o início do corte de intervalo. Se omitido, ele assume como padrão a posição atual.                                                                                                                                                |
| para *posicionar*         | Especifica o final do corte de intervalo. O corte de dados de áudio e vídeo é exclusivo dessa posição. Se omitido, o padrão será o final do workspace.                                                                                  |
| fluxo de fluxo de *vídeo* | Especifica o fluxo de vídeo no workspace afetado pelo comando. Se você usar esse sinalizador e também quiser cortar áudio, também deverá usar o sinalizador "fluxo de áudio". (Se nenhum sinalizador for especificado, todos os fluxos de áudio e vídeo serão cortados.) |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify", "test" ou uma combinação deles. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

A alteração se torna permanente somente quando os dados são salvos explicitamente; no entanto, a reprodução age como se os dados tivesse sido removidos.

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

 

