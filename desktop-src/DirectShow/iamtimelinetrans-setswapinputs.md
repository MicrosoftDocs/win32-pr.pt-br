---
description: O método SetSwapInputs especifica se as entradas de transição são trocadas.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: 'Método IAMTimelineTrans:: SetSwapInputs (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3da350c6fe34f671d7af53ca67c404b4e327690918434b5e2fb1426e4a0953ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052076"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>Método IAMTimelineTrans:: SetSwapInputs

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetSwapInputs` método especifica se as entradas de transição são trocadas.

Por padrão, uma transição é proveniente da composição de todas as camadas de prioridade inferior para a camada em que reside a transição. Você pode reverter essa progressão, de modo que a transição vai da camada onde ela reside de volta para a composição de camadas de prioridade inferior. Para obter mais informações, consulte [direção da transição](transition-direction.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Val* 
</dt> <dd>

Especifica se as entradas são trocadas. Se **for false**, a transição passará da composição de todas as camadas de prioridade inferior para a camada de transição. Se **for true**, a transição vai para a direção oposta.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método não altera a direção do efeito visual. Por exemplo, um apagamento da esquerda para a direita ainda passará da esquerda para a direita. Para alterar a direção, defina a propriedade **Progress** usando a interface [**IPropertySetter**](ipropertysetter.md) .

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

[**Interface IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




