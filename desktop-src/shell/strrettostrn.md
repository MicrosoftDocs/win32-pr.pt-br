---
description: 'Usa uma estrutura STRRET retornada por IShellFolder:: GetDisplayNameOf, converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.'
title: Função StrRetToStrN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989106"
---
# <a name="strrettostrn-function"></a>Função StrRetToStrN

Usa uma estrutura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) retornada por [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), converte-a em uma cadeia de caracteres e coloca o resultado em um buffer.

## <a name="syntax"></a>Sintaxe


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszOut* \[ fora\]
</dt> <dd>

Tipo: **LPTSTR**

Buffer para armazenar o nome de exibição. Ele será retornado como uma cadeia de caracteres terminada em nulo. Se *cchOut* for muito pequeno, o nome será truncado para se ajustar.

</dd> <dt>

*cchOut* \[ no\]
</dt> <dd>

Tipo: **uint**

Tamanho de *pszOut*, em caracteres. Se *cchOut* for muito pequeno, a cadeia de caracteres será truncada para caber.

</dd> <dt>

*pStrRet* \[ entrada, saída\]
</dt> <dd>

Tipo: **LPSTRRET**

Ponteiro para uma estrutura [**Strret**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Quando a função retornar, esse ponteiro não será mais válido.

</dd> <dt>

*PIDL* \[ no\]
</dt> <dd>

Tipo: **LPCITEMIDLIST**

Ponteiro para a estrutura [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **bool**

**Verdadeiro** para êxito, **falso** para falha.

## <a name="remarks"></a>Comentários

> [!Note]  
> A partir da versão Shell32.dll 5,0, chamar essa função é equivalente a chamar [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa).

 

**StrRetToStrN** não é exportado pelo nome. Para usá-lo, você deve usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) e solicitar o ordinal 96 de Shell32.dll para obter um ponteiro de função.

Se o membro **uType** da estrutura apontada por *pStrRet* for definido como **Strret \_ WSTR**, o membro **pOleStr** dessa estrutura será liberado no retorno.

Observe que essa função é exportada de Shell32.dll em vez de Shlwapi.dll. Ele também está incluído em shlobj. h em vez de shlwapi. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
