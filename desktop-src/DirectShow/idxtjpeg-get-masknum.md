---
description: O \_ método Get MaskNum recupera o código de apagamento SMPTE do apagamento.
ms.assetid: 49710d40-acc0-453e-ac9c-882794a0b82d
title: 'Método IDxtJpeg:: get_MaskNum (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_MaskNum
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9265cac204609381e5d3d6d58d4fbd697f623913098e1f9ebe50d891db31b850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131036"
---
# <a name="idxtjpegget_masknum-method"></a>Método IDxtJpeg:: get \_ MaskNum

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_MaskNum` método recupera o código de apagamento SMPTE do apagamento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MaskNum(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe o código de apagamento SMPTE. Para obter uma lista de apagamentos SMPTE com suporte, consulte [transição de apagamento SMPTE](smpte-wipe-transition.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IDxtJpeg**](idxtjpeg.md)
</dt> </dl>

 

 




