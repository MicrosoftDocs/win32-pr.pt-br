---
description: O método \_ get SrcWidth recupera a largura do retângulo de origem.
ms.assetid: 373bb108-5f0b-47f3-a39a-ed43b536e612
title: Método IDxtCompositor::get_SrcWidth (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor.get_SrcWidth
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dfac81b82a59883d4ce382ea81efd42fa64076fecc81069787edeb1778066f1b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042906"
---
# <a name="idxtcompositorget_srcwidth-method"></a>Método IDxtCompositor::get \_ SrcWidth

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_SrcWidth` método recupera a largura do retângulo de origem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_SrcWidth(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recebe a largura do retângulo de origem, em pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDxtCompositor Interface**](idxtcompositor.md)
</dt> </dl>

 

 




