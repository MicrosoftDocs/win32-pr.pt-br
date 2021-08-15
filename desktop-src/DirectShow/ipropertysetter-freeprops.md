---
description: O método FreeProps libera recursos alocados pelo método IPropertySetter::GetProps. Chame esse método depois de chamar GetProps, passando-o para as estruturas retornadas por GetProps.
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: Método IPropertySetter::FreeProps (Qedit.h)
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
ms.openlocfilehash: 34529c7d78ad36a87eb441f624af8daf1167a77148758ff376feacc70250f18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397547"
---
# <a name="ipropertysetterfreeprops-method"></a>Método IPropertySetter::FreeProps

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `FreeProps` método libera recursos alocados pelo método [**IPropertySetter::GetProps.**](ipropertysetter-getprops.md) Chame esse método depois de chamar **GetProps,** passando-o para as estruturas retornadas **por GetProps.**

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

*cParams* \[ Em\]
</dt> <dd>

O número de elementos na matriz *paParam.*

</dd> <dt>

*paParam* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas DE PARAM DE \_ PARAM.**](dexter-param.md)

</dd> <dt>

*paValue* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas DE \_ VALOR DE VALOR.**](dexter-value.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

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

[**IPropertySetter Interface**](ipropertysetter.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




