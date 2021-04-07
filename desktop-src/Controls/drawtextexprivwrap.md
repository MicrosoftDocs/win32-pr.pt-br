---
title: Função DrawTextExPrivWrap
description: Desenha texto formatado no retângulo especificado. Essa função encapsula uma chamada para DrawTextEx.
ms.assetid: 3212282c-1adb-4f7e-b4d7-7d833b26ac60
keywords:
- Controles do Windows da função DrawTextExPrivWrap
topic_type:
- apiref
api_name:
- DrawTextExPrivWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba496a121af3ba88ed24ab6c9c7834c90153ec0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919170"
---
# <a name="drawtextexprivwrap-function"></a>Função DrawTextExPrivWrap

\[O **DrawTextExPrivWrap** está disponível por meio do Windows XP com Service Pack 2 (SP2). Ele pode ser alterado ou indisponível nas versões subsequentes. Em vez disso, é recomendável usar o [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) diretamente.\]

Desenha texto formatado no retângulo especificado. Essa função encapsula uma chamada para [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI DrawTextExPrivWrap(
  _In_    HDC              hdc,
  _Inout_ LPTSTR           lpchText,
  _In_    int              cchText,
  _Inout_ LPRECT           lprc,
  _In_    UINT             dwDTFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* \[ no\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Um identificador para o contexto do dispositivo no qual desenhar.

</dd> <dt>

*lpchText* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPTSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para um buffer que contém o texto a ser desenhado. Se o parâmetro *cchText* for-1, a cadeia de caracteres deverá ser terminada em nulo.

Se *dwDTFormat* incluir \_ o DT modifystring, a função poderá adicionar até quatro caracteres adicionais a essa cadeia de caracteres. O buffer que contém a cadeia de caracteres deve ser grande o suficiente para acomodar esses caracteres extras.

</dd> <dt>

*cchText* \[ no\]
</dt> <dd>

Tipo: **int**

O comprimento da cadeia de caracteres apontada por *lpchText*. Se *cchText* for-1, o parâmetro *lpchText* será considerado um ponteiro para uma cadeia de caracteres terminada em nulo e [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) calculará automaticamente a contagem de caracteres.

</dd> <dt>

*lprc* \[ entrada, saída\]
</dt> <dd>

Tipo: **lpRect**

Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado.

</dd> <dt>

*dwDTFormat* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

As opções de formatação. Consulte a documentação do [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa) para obter uma lista completa de opções.

</dd> <dt>

*lpDTParams* \[ no\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Um ponteiro para uma estrutura [**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opções de formatação adicionais. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Se a função for realizada com sucesso, o valor de retorno será a altura do texto em unidades lógicas. Se a **\_ parte inferior** de **dt \_ VCENTER** ou DT for especificada, o valor de retorno será o deslocamento do membro **superior** de *lprc* para a parte inferior do texto desenhado.

Se a função falhar, o valor retornado será zero.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

**DrawTextExPrivWrap** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público. Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 416 de ComCtl32.dll para obter um ponteiro de função.

Para comentários adicionais, consulte [**DrawTextEx**](/windows/desktop/api/winuser/nf-winuser-drawtextexa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 6,0 ou posterior)</dt> </dl> |



 

