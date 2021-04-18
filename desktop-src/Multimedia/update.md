---
title: Atualizar comando
description: O comando Update redesenha o quadro atual no contexto de dispositivo especificado (DC). Dispositivos de vídeo digital reconhecem este comando.
ms.assetid: 51a83262-91d5-4852-ad17-bd62c14417b1
keywords:
- atualizar o comando multimídia do Windows
topic_type:
- apiref
api_name:
- update
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb0fc96d404efd8e2f657985ffa5a8861d3b4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499769"
---
# <a name="update-command"></a>Atualizar comando

O comando Update redesenha o quadro atual no contexto de dispositivo especificado (DC). Dispositivos de vídeo digital reconhecem este comando.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

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

Identificador de um controlador de domínio. A tabela a seguir lista os tipos de dispositivo que reconhecem o comando de **atualização** e os sinalizadores usados por cada tipo.



| Valor        | Significado                       | Significado         |
|--------------|-------------------------------|-----------------|
| digitalvideo | HDC *HDC* HDC *HDC* em *Rect* | pintar HDC *HDC* |



 

A tabela a seguir lista os sinalizadores que podem ser especificados no parâmetro **lpszHDC** e seus significados.



| Valor               | Significado                                                                                                |
|---------------------|--------------------------------------------------------------------------------------------------------|
| HDC *HDC*           | Especifica o identificador do DC a ser pintado.                                                               |
| HDC *HDC* at *Rect* | Especifica o retângulo de recorte relativo ao retângulo do cliente.                                     |
| pintar HDC *HDC*     | Pinta o controlador de domínio quando o aplicativo recebe uma mensagem de [**\_ pintura do WM**](/windows/desktop/gdi/wm-paint) destinada a um DC. |



 

Para especificar o identificador do controlador de domínio, use a cadeia de caracteres "hdc" seguida de uma representação ASCII do identificador. O retângulo é especificado como **X1 Y1 x2 y2**. As coordenadas **X1 Y1** especificam o canto superior esquerdo do retângulo, e as coordenadas **x2 y2** especificam a largura e a altura.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital, "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="examples"></a>Exemplos

O comando a seguir atualiza toda a janela de exibição usada pelo dispositivo "filme". O número 203 é um identificador para um controlador de domínio obtido da função [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) .

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

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> </dl>

 

