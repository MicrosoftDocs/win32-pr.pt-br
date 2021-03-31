---
title: Função GetTextExtentPoint32Wrap
description: Computa a largura e a altura da cadeia de caracteres especificada de texto. Essa função encapsula uma chamada para GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Controles do Windows da função GetTextExtentPoint32Wrap
topic_type:
- apiref
api_name:
- GetTextExtentPoint32Wrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6a0db92ad019950cf8be0a72260da75acc06779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644302"
---
# <a name="gettextextentpoint32wrap-function"></a>Função GetTextExtentPoint32Wrap

\[O **GetTextExtentPoint32Wrap** está disponível por meio do Windows XP com Service Pack 2 (SP2). Ele pode ser alterado ou indisponível nas versões subsequentes. Em vez disso, é recomendável usar o [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) diretamente.\]

Computa a largura e a altura da cadeia de caracteres especificada de texto. Essa função encapsula uma chamada para [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="syntax"></a>Sintaxe


```C++
BOOL GetTextExtentPoint32Wrap(
  _In_  HDC     hdc,
  _In_  LPCTSTR lpString,
  _In_  UINT    cbCount,
  _Out_ LPSIZE  lpSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HDC* \[ no\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Um identificador para o contexto do dispositivo.

</dd> <dt>

*LPSTR* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para um buffer que contém o texto a ser desenhado. A cadeia de caracteres não precisa terminar com zero, pois *cbCount* especifica o comprimento da cadeia de caracteres.

</dd> <dt>

*cbCount* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

O comprimento, em bytes, da cadeia de caracteres apontada por *lpString*.

</dd> <dt>

*lpSize* \[ fora\]
</dt> <dd>

Tipo: **LPSIZE**

Quando esse método retorna, contém um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que contém as dimensões da cadeia de caracteres, em unidades lógicas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

Retorna um valor diferente de zero se for bem-sucedido; caso contrário, 0.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

**GetTextExtentPoint32Wrap** não é exportado pelo nome ou declarado em um arquivo de cabeçalho público. Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 420 de ComCtl32.dll para obter um ponteiro de função.

Para comentários adicionais, consulte [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5,81 ou posterior)</dt> </dl> |



 

