---
title: Método ISoftKbd SetSoftKeyboardPosSize (Softkbdc. h)
description: O método ISoftKbd SetSoftKeyboardPosSize define a posição inicial e o tamanho de um teclado suave.
ms.assetid: bf827b07-0e8b-4d5a-8178-45d75af83551
keywords:
- Estrutura de serviços de texto do método SetSoftKeyboardPosSize
- Método SetSoftKeyboardPosSize de estrutura de serviços de texto, interface ISoftKbd
- Estrutura de serviços de texto da interface ISoftKbd, método SetSoftKeyboardPosSize
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardPosSize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7131d9c46c90917f2ebdf471916f872aedb2e33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455643"
---
# <a name="isoftkbdsetsoftkeyboardpossize-method"></a>Método ISoftKbd:: SetSoftKeyboardPosSize

O método **ISoftKbd:: SetSoftKeyboardPosSize** define a posição inicial e o tamanho de um teclado suave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSoftKeyboardPosSize(
  [in] POINT StartPoint,
  [in] WORD  width,
  [in] WORD  height
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StartPoint* \[ no\]
</dt> <dd>

Uma estrutura de [ponto](/previous-versions//dd162805(v=vs.85)) que indica as coordenadas da posição superior esquerda do teclado virtual.

</dd> <dt>

*largura* \[ no\]
</dt> <dd>

Largura do teclado virtual.

</dd> <dt>

*altura* \[ no\]
</dt> <dd>

Altura do teclado virtual.

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
</dt> </dl>

 

