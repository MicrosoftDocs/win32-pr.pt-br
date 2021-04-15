---
description: O \_ método Get AlphaRamp recupera a propriedade de rampa alfa. A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados. Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.
ms.assetid: e142a562-2e78-4418-94e9-b41320d4af57
title: 'Método IDxtAlphaSetter:: get_AlphaRamp (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter.get_AlphaRamp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 335c227b0ac35ccd730d8ce7014b9a5c7ebc3213
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760878"
---
# <a name="idxtalphasetterget_alpharamp-method"></a>Método IDxtAlphaSetter:: get \_ AlphaRamp

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `get_AlphaRamp` método recupera a propriedade de rampa alfa. A rampa alfa é a porcentagem pela qual os valores Alfa na imagem original são ajustados. Por exemplo, se a rampa alfa for 0,5, os valores Alfa na imagem serão reduzidos em 50%.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_AlphaRamp(
  [out, retval] double *pAlpha
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAlpha* \[ out, retval\]
</dt> <dd>

Recebe a rampa de alfa. Um valor negativo indica que nenhuma rampa de alfa está definida.

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

 

 




