---
description: O método SetPalette instala uma paleta para a janela. Esse método não tem parâmetros.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Método CBaseWindow.SetPalette (Winutil.h) – Sem parâmetros
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
ms.openlocfilehash: f15df65f6e427e467c14654a0e2745b84d774a5226b9a526193fc546261c5a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052146"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Método CBaseWindow.SetPalette (Winutil.h) – Sem parâmetros

O `SetPalette` método instala uma paleta para a janela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Uma chamada interna para **GdiFlush retornou** um erro.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                            |



 

## <a name="remarks"></a>Comentários

A paleta dada pela variável de [**membro CBaseWindow::m \_ hPalette**](cbasewindow-m-hpalette.md) está selecionada. O chamador deve garantir a validade de **m \_ hPalette.**

Se o valor da variável de membro [**CBaseWindow::m \_ bNoRealize**](cbasewindow-m-bnorealize.md) for **FALSE** (o padrão), esse método selecionará a paleta e a perceberá. Caso contrário, ele selecionará a paleta, mas não a perceberá. O objeto não exclui nenhuma paleta anterior que estava usando. O chamador é responsável por excluir paletas.

Qualquer thread pode chamar com segurança esse método, não apenas o thread que possui a janela. A janela envia uma mensagem privada para si mesma, que dispara uma chamada para o [**método CBaseWindow::OnPaletteChange.**](cbasewindow-onpalettechange.md)

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | Winutil.h (incluir Fluxos.h) |
| Biblioteca| Strmbase.lib (builds de varejo); Strmbasd.lib (builds de depuração) |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




