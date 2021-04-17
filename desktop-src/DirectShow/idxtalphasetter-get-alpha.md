---
description: O \_ método Get Alpha recupera o valor alfa de toda a imagem.
ms.assetid: ce891149-e964-4239-aeef-c9f4a8354563
title: 'Método IDxtAlphaSetter:: get_Alpha (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_Alpha
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6182590d09df1c816a1a861df8be724798cc75da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782839"
---
# <a name="idxtalphasetterget_alpha-method"></a>Método IDxtAlphaSetter:: get \_ Alpha

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_Alpha` método recupera o valor alfa para a imagem inteira.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Alpha(
  [out, retval] long *pAlpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Recebe o valor alfa. Esse valor alfa será aplicado à imagem de destino inteira. Um valor negativo indica que nenhum valor alfa está definido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                               | Descrição                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo**<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Sucesso<br/>                   |



 

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

[**Interface IDxtAlphaSetter**](idxtalphasetter.md)
</dt> </dl>

 

 




