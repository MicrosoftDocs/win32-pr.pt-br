---
description: A função GetDialogSize recupera o tamanho de uma caixa de diálogo de recurso.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Função GetDialogSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7f1f2631e169549895a1f74ce571b2abfeeee8cd77ac7cb3c4dfc5aa6913a6d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564946"
---
# <a name="getdialogsize-function"></a>Função GetDialogSize

A função **GetDialogSize** recupera o tamanho de uma caixa de diálogo de recurso.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iResourceID* 
</dt> <dd>

Identificador de recurso da caixa de diálogo.

</dd> <dt>

*pDlgProc* 
</dt> <dd>

Ponteiro para o procedimento da caixa de diálogo.

</dd> <dt>

*lParam* 
</dt> <dd>

Valor passado na mensagem do WM \_ INITDIALOG enviada para a caixa de diálogo temporária logo após sua criação.

</dd> <dt>

*pResult* 
</dt> <dd>

Ponteiro para uma estrutura de **tamanho** que recebe as dimensões da caixa de diálogo, na tela pixels.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** se o recurso da caixa de diálogo foi encontrado ou **false** caso contrário.

## <a name="remarks"></a>Comentários

As páginas de propriedades podem usar essa função para retornar o tamanho de exibição real necessário. A maioria das páginas de propriedades são caixas de diálogo e, como tal, têm modelos de caixa de diálogo armazenados em arquivos de recursos. Os modelos usam unidades de caixa de diálogo que não são mapeadas diretamente na tela pixels. No entanto, a função [**GetPageInfo**](cbasepropertypage-getpageinfo.md) de uma página de propriedades deve retornar o tamanho de exibição real em pixels. A página de propriedades pode chamar `GetDialogSize` para calcular o tamanho de exibição.

Essa função cria uma instância temporária da caixa de diálogo. Para evitar que a caixa de diálogo apareça na tela, o modelo de caixa de diálogo no arquivo de recurso não deve ter uma \_ Propriedade WS visível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil. h (incluir Fluxos. h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções auxiliares de página de propriedades](property-page-helper-functions.md)
</dt> </dl>

 

 




