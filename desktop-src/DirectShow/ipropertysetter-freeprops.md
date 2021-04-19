---
description: 'O método FreeProps libera recursos alocados pelo método IPropertySetter:: GetProps. Chame esse método depois de chamar GetProps, passando-o para as estruturas retornadas por GetProps.'
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Método IPropertySetter:: FreeProps (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766990"
---
# <a name="ipropertysetterfreeprops-method"></a>Método IPropertySetter:: FreeProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `FreeProps` método libera recursos alocados pelo método [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) . Chame esse método depois de chamar **GetProps**, passando-o para as estruturas retornadas por **GetProps**.

## <a name="syntax"></a>Sintaxe


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cParams* \[ no\]
</dt> <dd>

O número de elementos na matriz *paParam* .

</dd> <dt>

*paParam* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas \_ param Dexter**](dexter-param.md) .

</dd> <dt>

*paValue* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de estruturas de [**\_ valor Dexter**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




