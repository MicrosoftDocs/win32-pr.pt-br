---
title: Função ExtTextOutWrap
description: Desenha o texto usando a fonte, a cor do plano de fundo e a cor do texto selecionados no momento. Opcionalmente, você pode fornecer dimensões a serem usadas para recorte, opacidade ou ambos. Essa função encapsula uma chamada para ExtTextOut.
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- Controles do Windows da função ExtTextOutWrap
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a173fedb7d8534dbd926a8a147e833435a7710b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085212"
---
# <a name="exttextoutwrap-function"></a>Função ExtTextOutWrap

\[O **ExtTextOutWrap** está disponível por meio do Windows XP com Service Pack 2 (SP2). Ele pode ser alterado ou indisponível nas versões subsequentes. Em vez disso, é recomendável usar o [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) diretamente.\]

Desenha o texto usando a fonte, a cor do plano de fundo e a cor do texto selecionados no momento. Opcionalmente, você pode fornecer dimensões a serem usadas para recorte, opacidade ou ambos. Essa função encapsula uma chamada para [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="syntax"></a>Sintaxe


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* \[ no\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Um identificador para o contexto do dispositivo.

</dd> <dt>

*X* \[ em\]
</dt> <dd>

Tipo: **int**

A coordenada x, em coordenadas lógicas, do ponto de referência usado para posicionar a cadeia de caracteres.

</dd> <dt>

*Y* \[ em\]
</dt> <dd>

Tipo: **int**

A coordenada y, em coordenadas lógicas, do ponto de referência usado para posicionar a cadeia de caracteres.

</dd> <dt>

*uOptions* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Valores que especificam como usar o retângulo definido pelo aplicativo. Consulte [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) para obter uma lista completa de opções.

</dd> <dt>

*lprc* \[ no\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \** _

Um ponteiro para uma estrutura opcional [_ *Rect* *](/previous-versions//dd162897(v=vs.85)) que especifica as dimensões, em coordenadas lógicas, de um retângulo usado para recorte, opacidade ou ambos.

</dd> <dt>

*LPSTR* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para um buffer que contém o texto a ser desenhado. A cadeia de caracteres não precisa terminar com zero, pois *cbCount* especifica o comprimento da cadeia de caracteres.

</dd> <dt>

*cbCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O comprimento da cadeia de caracteres, em bytes, apontado por *LPSTR*.

</dd> <dt>

*lpDx* \[ no\]
</dt> <dd>

Tipo: **const [**int**](/windows/desktop/WinProg/windows-data-types) \** _

Um ponteiro para uma matriz opcional de valores que indicam a distância entre as origens das células de caracteres adjacentes. Por exemplo, _lpDx \[ unidades lógicas * x separam \] as origens da célula de caractere x e da célula de caractere (x + 1).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Retorna um valor diferente de zero se a cadeia de caracteres é desenhada com êxito. No entanto, se a versão ANSI de [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) for chamada com o \_ índice de glifo Eto \_ , a função retornará **true** mesmo que a função não faça nada.

Se a função falhar, o valor retornado será zero.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

**ExtTextOutWrap** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público. Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 417 de ComCtl32.dll para obter um ponteiro de função.

Para comentários adicionais, consulte [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                 |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 6,0 ou posterior)</dt> </dl> |



 

