---
title: comando update
description: O comando update reintsifique o quadro atual no DC (contexto de dispositivo) especificado. Os dispositivos de vídeo digital reconhecem esse comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- comando update Windows Multimídia
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1a5f4f185c16e0ba499e75ed9f445aaf87b9e346dbde9a7929035613f4744ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804696"
---
# <a name="update-command"></a>comando update

O comando update reintsifique o quadro atual no DC (contexto de dispositivo) especificado. Os dispositivos de vídeo digital reconhecem esse comando.

Para enviar esse comando, chame a [**função mciSendString**](/previous-versions//dd757161(v=vs.85)) com *o parâmetro lpszCommand* definido da seguinte forma.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("update %s %s %s"), 
  lpszDeviceID, 
  lpszHDC, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificador de um dispositivo MCI. Esse identificador ou alias é atribuído quando o dispositivo é aberto.

</dd> <dt>

<span id="lpszHDC"></span><span id="lpszhdc"></span><span id="LPSZHDC"></span>*lpszHDC*
</dt> <dd>

Lidar com um DC. A tabela a seguir lista os tipos de dispositivo que reconhecem o **comando update** e os sinalizadores usados por cada tipo.



| Valor        | Significado                       | Significado         |
|--------------|-------------------------------|-----------------|
| digitalvideo | hdc *hdc* hdc *hdc* *em rect* | paint hdc *hdc* |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no **parâmetro lpszHDC** e seus significados.



| Valor               | Significado                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| hdc *hdc*           | Especifica a alça do DC a ser pintado.                                                               |
| hdc *hdc* em *rect* | Especifica o retângulo de recorte relativo ao retângulo do cliente.                                     |
| paint hdc *hdc*     | Pinta o DC quando o aplicativo recebe uma mensagem [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint) destinada a um DC. |



 

Para especificar o handle do DC, use a cadeia de caracteres "hdc" seguida por uma representação ASCII do handle. O retângulo é especificado como **X1 Y1 X2 Y2**. As coordenadas **X1 Y1** especificam o canto superior esquerdo do retângulo e as coordenadas **X2 Y2** especificam a largura e a altura.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "wait", "notify" ou ambos. Para dispositivos de vídeo digital, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [Os sinalizadores de espera, notificação e teste.](the-wait-notify-and-test-flags.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="examples"></a>Exemplos

O comando a seguir atualiza toda a janela de exibição usada pelo dispositivo de "filme". O número 203 é um handle para um DC obtido da [**função BeginPaint.**](/windows/desktop/api/winuser/nf-winuser-beginpaint)

``` syntax
update movie hdc 203
```

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

 

