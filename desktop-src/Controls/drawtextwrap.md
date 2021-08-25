---
title: Função DrawTextWrap
description: Desenha texto formatado no retângulo especificado. Ele formatará o texto de acordo com o método especificado (expandindo guias, justificando caracteres, quebrando linhas e assim por diante). Essa função envolve uma chamada para DrawText.
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- Função DrawTextWrap Windows Controles
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcbd504955b6ae772ffb3db7bc4cc0223215d6d9ecf880fe7d7e3aa359c992ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878286"
---
# <a name="drawtextwrap-function"></a>Função DrawTextWrap

\[**DrawTextWrap** está disponível por meio Windows XP com Service Pack 2 (SP2). Ele pode ser alterado ou não disponível nas versões subsequentes. Em vez disso, é recomendável [**usar DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) diretamente.\]

Desenha texto formatado no retângulo especificado. Ele formatará o texto de acordo com o método especificado (expandindo guias, justificando caracteres, quebrando linhas e assim por diante). Essa função envolve uma chamada para [**DrawText.**](/windows/desktop/api/winuser/nf-winuser-drawtext)

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hdc* \[ Em\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Um alça para o contexto do dispositivo.

</dd> <dt>

*lpString* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para um buffer que contém o texto a ser desenhar. Se o *parâmetro nCount* for -1, a cadeia de caracteres deverá ser terminada em nulo.

Se *uFormat incluir* DT MODIFYSTRING, a função poderá adicionar até quatro caracteres adicionais \_ a essa cadeia de caracteres. O buffer que contém a cadeia de caracteres deve ser grande o suficiente para acomodar esses caracteres extras.

</dd> <dt>

*nCount* \[ Em\]
</dt> <dd>

Tipo: **int**

O comprimento da cadeia de caracteres apontada por *lpString.* Se *nCount* for -1, o parâmetro *lpString* será presumido como um ponteiro para uma cadeia de caracteres terminada em nulo e [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) calculará a contagem de caracteres automaticamente.

</dd> <dt>

*lpRect* \[ in, out\]
</dt> <dd>

Tipo: **LPRECT**

Um ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que contém o retângulo, em coordenadas lógicas, em que o texto deve ser formatado.

</dd> <dt>

*uFormat* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

As opções de formatação. Consulte a documentação [**de DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) para ver uma lista completa de opções.

</dd> <dt>

*lpDTParams* \[ Em\]
</dt> <dd>

Tipo: **LPDRAWTEXTPARAMS**

Um ponteiro para uma [**estrutura DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams) que especifica opções de formatação adicionais. Este parâmetro pode ser **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **int**

Se a função for bem-sucedida, o valor de retorno será a altura do texto em unidades lógicas. Se **DT \_ VCENTER** ou **DT \_ BOTTOM** for especificado, o  valor de retorno será o deslocamento do membro superior de *lprc* para a parte inferior do texto desenhado Se a função falhar, o valor de retorno será zero.

Se a função falhar, o valor retornado será zero.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

**DrawTextWrap** não é exportado por nome nem declarado em um header público. Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar ordinal 415 do ComCtl32.dll para obter um ponteiro de função.

Para comentários adicionais, consulte [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 6.0 ou posterior)</dt> </dl> |



 

