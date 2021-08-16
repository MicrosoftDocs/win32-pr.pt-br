---
description: O \_ método obter KeyType recupera o tipo de chave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Método IDxtKey:: get_KeyType (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cfb8930df859771f61406ebab9a1e7f60cfdf149eaf66eae23120bb7292ebf74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819470"
---
# <a name="idxtkeyget_keytype-method"></a>Método IDxtKey:: get \_ KeyType

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_KeyType` método recupera o tipo de chave.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe um dos seguintes valores de enumeração.



| Valor             | Descrição                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Chave croma. (Chave no valor RGB.)                       |
| DXTKEY \_ NONRED    | Chave Nonred. (Torna as áreas azul e verde transparentes.) |
| luminância de DXTKEY \_ | Chave de luminância.                                        |
| DXTKEY \_ alfa     | Chave por valor alfa.                                   |
| \_matiz DXTKEY       | Chave por matiz.                                           |



 

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

[**Interface IDxtKey**](idxtkey.md)
</dt> </dl>

 

 




