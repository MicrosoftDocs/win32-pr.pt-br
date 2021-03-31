---
title: Função Str_GetPtr
description: Copia uma cadeia de caracteres de um buffer para outro.
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Controles do Windows da função Str_GetPtr
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fec99bb4d91bde86d901c0e7ed4761bafd15f3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644402"
---
# <a name="str_getptr-function"></a>\_Função GetPtr Str

\[Essa função está disponível por meio do Windows XP com Service Pack 2 (SP2) e Windows Server 2003. Ele pode ser alterado ou indisponível nas versões subsequentes do Windows.\]

Copia uma cadeia de caracteres de um buffer para outro.

## <a name="syntax"></a>Sintaxe


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszSource* \[ no\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para uma cadeia de caracteres de origem.

</dd> <dt>

*pszDest* \[ entrada, saída\]
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Um ponteiro para o buffer de destino. Esse valor pode ser **nulo**.

</dd> <dt>

*cchDest* \[ no\]
</dt> <dd>

Tipo: **int**

O tamanho de *pszDest*, em caracteres.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Se *pszDest* for **nulo** ou *cchDest* for zero, retornará o tamanho do buffer, em caracteres, necessário para conter uma cópia terminada em nulo da cadeia de caracteres apontada por *pszSource*.

Se *pszDest* for não **nulo**, retornará o número de caracteres copiados com êxito, incluindo o caractere nulo de terminação.

Se *pszDest* não puder conter a cadeia de caracteres inteira apontada por *pszSource*, os caracteres (*cchDest*-1) serão copiados, a cadeia de caracteres com terminação nula e *cchDest* retornado.

## <a name="remarks"></a>Comentários

**Str \_ GetPtr** está disponível como ANSI (**Str \_ GetPtrA**) e versões Unicode (**Str \_ GetPtrW**). Essas funções não são exportadas por nome ou declaradas em um arquivo de cabeçalho público. Para usá-los, você deve usar [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 233 (**Str \_ GetPtrA**) ou 235 (**Str \_ GetPtrW**) de ComCtl32.dll para obter um ponteiro de função.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **Str \_ GetPtrW** (Unicode) e **\_ GetPtrA de Str** (ANSI)<br/>                       |



 

