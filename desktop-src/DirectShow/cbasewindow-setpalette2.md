---
description: O método SetPalette instala uma paleta para a janela. Esse método não tem parâmetros.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Método CBaseWindow. SetPalette (Winutil. h)-sem parâmetros
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104173218"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Método CBaseWindow. SetPalette (Winutil. h)-sem parâmetros

O `SetPalette` método instala uma paleta para a janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Uma chamada interna para **GdiFlush** retornou um erro.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A paleta fornecida pela variável de membro [**CBaseWindow:: m \_ hPalette**](cbasewindow-m-hpalette.md) é selecionada. O chamador deve garantir a validade de **m \_ hPalette**.

Se o valor da variável de membro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) for **false** (o padrão), esse método selecionará a paleta e a perceberá. Caso contrário, ele seleciona a paleta, mas não a percebe. O objeto não exclui nenhuma paleta anterior que estava sendo usada. O chamador é responsável por excluir paletas.

Qualquer thread pode chamar esse método com segurança, não apenas o thread que possui a janela. A janela envia uma mensagem particular para si mesma, que dispara uma chamada para o método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Winutil. h (incluir fluxos. h) |
| Biblioteca| Strmbase. lib (compilações de varejo); Strmbasd. lib (compilações de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




