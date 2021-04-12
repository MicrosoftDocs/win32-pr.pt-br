---
title: Método ISoftKbd GetSoftKeyboardPosSize (Softkbdc. h)
description: O método ISoftKbd GetSoftKeyboardPosSize recupera a posição inicial e o tamanho de um teclado suave.
ms.assetid: d4482e34-1723-4fe2-a488-e7c18eb3f68e
keywords:
- Estrutura de serviços de texto do método GetSoftKeyboardPosSize
- Método GetSoftKeyboardPosSize de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método GetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9af445efd3e1b510280d20667862f2d95404597f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295830"
---
# <a name="isoftkbdgetsoftkeyboardpossize-method"></a>Método ISoftKbd:: GetSoftKeyboardPosSize

O método **ISoftKbd:: GetSoftKeyboardPosSize** recupera a posição inicial e o tamanho de um teclado suave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetSoftKeyboardPosSize(
  [out] POINT *lpStartPoint,
  [out] WORD  *lpwidth,
  [out] WORD  *lpheight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpStartPoint* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera uma estrutura de [ponto](/previous-versions//dd162805(v=vs.85)) que indica as coordenadas da posição superior esquerda do teclado suave.

</dd> <dt>

*lpwidth* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera a largura do teclado virtual.

</dd> <dt>

*lpheight* \[ fora\]
</dt> <dd>

Ponteiro para um buffer no qual esse método recupera a altura do teclado virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Valor                                                                                        | Descrição                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um dos parâmetros é inválido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                        |
| parâmetro<br/>                   | <dl> <dt>Softkbdc. h</dt> </dl>  |
| INSERI<br/>                      | <dl> <dt>Softkbd. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Softkbd.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISoftKbd**](isoftkbd.md)
</dt> <dt>

[**ISoftKbd::SetSoftKeyboardPosSize**](isoftkbd-setsoftkeyboardpossize.md)
</dt> </dl>

 

