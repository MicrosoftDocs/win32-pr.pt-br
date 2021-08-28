---
description: O \_ método Get Invert recupera um valor booliano que indica se a operação de chave está invertida. Essa propriedade se aplica a todos os tipos de chave, exceto DXTKEY \_ alfa.
ms.assetid: 2ccf2066-3d9c-493b-bc54-a03e7d075531
title: 'Método IDxtKey:: get_Invert (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c5a862e062175d3c052a5003a2ced60fe5d3cc439bff76315e046fc2153f73af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083846"
---
# <a name="idxtkeyget_invert-method"></a>\_Método inverter IDxtKey:: Get

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Invert` método recupera um valor booliano que indica se a operação de chave é invertida. Essa propriedade se aplica a todos os tipos de chave, exceto DXTKEY \_ alfa.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Invert(
  [out, retval] BOOL *pVal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PVal* \[ out, retval\]
</dt> <dd>

Recebe um dos valores a seguir.



| Valor     | Descrição                                                                       |
|-----------|-----------------------------------------------------------------------------------|
| **TRUE**  | Os pixels na imagem subjacente são invertidos em relação à operação padrão. |
| **FALSE** | Os pixels na imagem subjacente são tornados transparentes da maneira padrão.         |



 

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
</dt> <dt>

[**IDxtKey:: obter \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




