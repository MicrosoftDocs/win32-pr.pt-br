---
title: Função de retorno de chamada ReaderScroll
description: Uma função de retorno de chamada definida pelo aplicativo usada quando o ponteiro do mouse é movido dentro da parte da janela de modo de leitor que foi declarada como a área de rolagem ativa.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Função readerScroll de retorno de chamada Windows Controles
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 554530e556161b4128199cda0a1a9d791f4f0ed75e8915c311d8945445486ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169106"
---
# <a name="readerscroll-callback-function"></a>Função de retorno de chamada ReaderScroll

\[*ReaderScroll* está disponível para uso nos sistemas operacionais especificados na seção Requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Uma função de retorno de chamada definida pelo aplicativo usada quando o ponteiro do mouse é movido dentro da parte da janela de modo de leitor que foi declarada como a área de rolagem ativa.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*prmi* \[ Em\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Um ponteiro para a [**estrutura READERMODEINFO**](readermodeinfo.md) que foi passada para a [**função DoReaderMode.**](doreadermode.md) Essa estrutura define a janela de modo de leitor e a área de rolagem ativa.

</dd> <dt>

*dx* \[ em\]
</dt> <dd>

Tipo: **int**

A distância a ser rolada horizontalmente. Se o sinalizador RMF \_ VERTICALONLY for definido na estrutura [**READERMODEINFO,**](readermodeinfo.md) esse valor será sempre 0.

</dd> <dt>

*dy* \[ Em\]
</dt> <dd>

Tipo: **int**

A distância a ser rolada verticalmente. Se o sinalizador RMF \_ HORIZONTALONLY for definido na estrutura [**READERMODEINFO,**](readermodeinfo.md) esse valor será sempre 0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Essa função sempre deve retornar **TRUE.**

## <a name="remarks"></a>Comentários

Quando o aplicativo recebe notificação dessa função, o aplicativo é responsável por rolar a janela do modo de leitor na direção especificada pelos parâmetros *dx* e *dy.*

## <a name="examples"></a>Exemplos

O exemplo a seguir descreve uma implementação dessa função usando uma função personalizada para realizar a rolagem.


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista, Windows aplicativos \[ da área de trabalho do Vista\]<br/> |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>          |



 

