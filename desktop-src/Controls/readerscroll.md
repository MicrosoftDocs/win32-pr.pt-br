---
title: Função de retorno de chamada ReaderScroll
description: Uma função de retorno de chamada definida pelo aplicativo usada quando o ponteiro do mouse é movido dentro da parte da janela do modo de leitor que foi declarada como a área de rolagem ativa.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Controles do Windows da função de retorno de chamada ReaderScroll
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
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918386"
---
# <a name="readerscroll-callback-function"></a>Função de retorno de chamada ReaderScroll

\[O *ReaderScroll* está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

Uma função de retorno de chamada definida pelo aplicativo usada quando o ponteiro do mouse é movido dentro da parte da janela do modo de leitor que foi declarada como a área de rolagem ativa.

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

*prmi* \[ no\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Um ponteiro para a estrutura [**READERMODEINFO**](readermodeinfo.md) que foi passada para a função [**doreadermode**](doreadermode.md) . Essa estrutura define a janela modo de leitura e a área de rolagem ativa.

</dd> <dt>

*DX* \[ em\]
</dt> <dd>

Tipo: **int**

A distância para rolar horizontalmente. Se o \_ sinalizador RMF VERTICALONLY for definido na estrutura [**READERMODEINFO**](readermodeinfo.md) , esse valor será sempre 0.

</dd> <dt>

*DY* \[ no\]
</dt> <dd>

Tipo: **int**

A distância para rolar verticalmente. Se o \_ sinalizador RMF HORIZONTALONLY for definido na estrutura [**READERMODEINFO**](readermodeinfo.md) , esse valor será sempre 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Essa função sempre deve retornar **true**.

## <a name="remarks"></a>Comentários

Quando o aplicativo recebe uma notificação dessa função, o aplicativo é responsável por rolar a janela do modo de leitura na direção especificada pelos parâmetros *DX* e *DY* .

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
| Cliente mínimo com suporte<br/> | Windows Vista, \[ somente aplicativos da área de trabalho do Windows Vista\]<br/> |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>          |



 

