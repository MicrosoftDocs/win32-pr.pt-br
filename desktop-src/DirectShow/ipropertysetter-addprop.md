---
description: O método AddProp adiciona uma propriedade ao setter de propriedade, com uma matriz de pares time-value definindo o valor da propriedade em um intervalo de tempo.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: Método IPropertySetter::AddProp (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b2a4cf2f730d177b4eb9323e882d5030c6fc1d658ede574e74d9d222e81d677f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818605"
---
# <a name="ipropertysetteraddprop-method"></a>Método IPropertySetter::AddProp

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método adiciona uma propriedade ao setter de propriedade, com uma matriz de pares time-value definindo o valor da propriedade em `AddProp` um intervalo de tempo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param* \[ Em\]
</dt> <dd>

[**SÃO PAULO \_ Estrutura PARAM**](dexter-param.md) que especifica a propriedade . O **membro nValues** da estrutura deve ser igual ao tamanho da matriz dado no *parâmetro paValue.*

</dd> <dt>

*paValue* \[ Em\]
</dt> <dd>

Ponteiro para uma matriz de [**estruturas DE VALOR DE VALOR QUE \_**](dexter-value.md) contêm pares de valor de tempo. A matriz deve estar em ordem de tempo crescente. Os horários são relativos à hora de início do efeito ou da transição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

A primeira [**estrutura DE VALOR DE VALOR DEVE \_**](dexter-value.md) especificar um tempo de referência de zero e um sinalizador de interpolação (**dwInterp**) de **JUMP de INTERPOLF \_** ou o método retorna um erro.

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

 

 




