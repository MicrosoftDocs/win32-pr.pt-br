---
description: O método \_ get RGB recupera a cor RGB na qual a chave deve ser obtida. Essa propriedade se aplica somente quando o tipo de chave é DXTKEY \_ RGB.
ms.assetid: 7b1b22ff-457a-48c8-9221-ca38601874a9
title: Método IDxtKey::get_RGB (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 596595e38ce57b026631d1ba7bd88d501bc50661ea3034fecd9ad4fbd9615428
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652405"
---
# <a name="idxtkeyget_rgb-method"></a>Método IDxtKey::get \_ RGB

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_RGB` método recupera a cor RGB na qual a chave deve ser obtida. Essa propriedade se aplica somente quando o tipo de chave é DXTKEY \_ RGB.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_RGB(
  [out, retval] DWORD *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recebe a cor. O valor retornado é um número hexadecimal com o formato 0xRRGGBB, em que RR é o valor vermelho, GG é o valor verde e BB é o valor azul.

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

[**IDxtKey Interface**](idxtkey.md)
</dt> <dt>

[**IDxtKey::get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




