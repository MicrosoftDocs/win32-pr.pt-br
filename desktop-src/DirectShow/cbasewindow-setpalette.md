---
description: O método SetPalette instala uma paleta para a janela.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Método CBaseWindow. SetPalette (Winutil. h)
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
ms.openlocfilehash: 0c04d4e24c621dd704b8aeba91646016e334a6f6bface4769578a710322a7cff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074550"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>Método CBaseWindow. SetPalette (Winutil. h)

O `SetPalette` método instala uma paleta para a janela.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPalette* 
</dt> <dd>

Identificador para a nova paleta. Não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Uma chamada interna para **GdiFlush** retornou um erro.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                            |



 

## <a name="remarks"></a>Comentários

Se o valor da variável de membro [**CBaseWindow:: m \_ BNoRealize**](cbasewindow-m-bnorealize.md) for **false** (o padrão), esse método selecionará a paleta e a perceberá. Caso contrário, ele seleciona a paleta, mas não a percebe. O objeto não exclui nenhuma paleta anterior que estava sendo usada. O chamador é responsável por excluir paletas.

Qualquer thread pode chamar esse método com segurança, não apenas o thread que possui a janela. A janela envia uma mensagem particular para si mesma, que dispara uma chamada para o método [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Winutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




