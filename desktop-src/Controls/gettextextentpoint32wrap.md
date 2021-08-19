---
title: Função GetTextExtentPoint32Wrap
description: Calcula a largura e a altura da cadeia de caracteres de texto especificada. Essa função envolve uma chamada para GetTextExtentPoint.
ms.assetid: 156f9344-6071-451c-94c7-63f369a5573a
keywords:
- Função GetTextExtentPoint32Wrap Windows Controles
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
ms.openlocfilehash: 0217d1708764ec33dd76ea35ff330f0d411697b5e9be3a6bd148377002a1f127
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047206"
---
# <a name="gettextextentpoint32wrap-function"></a>Função GetTextExtentPoint32Wrap

\[**GetTextExtentPoint32Wrap** está disponível por meio do Windows XP com o Service Pack 2 (SP2). Ele pode ser alterado ou não disponível nas versões subsequentes. É recomendável usar [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa) diretamente.\]

Calcula a largura e a altura da cadeia de caracteres de texto especificada. Essa função envolve uma chamada para [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

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

*hdc* \[ Em\]
</dt> <dd>

Tipo: **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

Um alça para o contexto do dispositivo.

</dd> <dt>

*lpString* \[ Em\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para um buffer que contém o texto a ser desenhado. A cadeia de caracteres não precisa ser terminada em zero, pois *cbCount* especifica o comprimento da cadeia de caracteres.

</dd> <dt>

*cbCount* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

O comprimento, em bytes, da cadeia de caracteres apontada por *lpString*.

</dd> <dt>

*lpSize* \[ out\]
</dt> <dd>

Tipo: **LPSIZE**

Quando este método retorna, contém um ponteiro para uma estrutura [**SIZE**](/previous-versions//dd145106(v=vs.85)) que contém as dimensões da cadeia de caracteres, em unidades lógicas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

Retornará um valor não zero se for bem-sucedido; caso contrário, 0.

Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

**GetTextExtentPoint32Wrap** não é exportado por nome nem declarado em um arquivo de header público. Para usá-lo, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar ordinal 420 do ComCtl32.dll para obter um ponteiro de função.

Para comentários adicionais, consulte [**GetTextExtentPoint**](/windows/desktop/api/wingdi/nf-wingdi-gettextextentpointa).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5.81 ou posterior)</dt> </dl> |



 

