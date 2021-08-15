---
description: Determina se um caractere é um caractere alfabético ou numérico.
ms.assetid: d4b01ba5-e42a-4040-a763-ecef0c73977f
title: Função IsCharAlphaNumericWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCharAlphaNumericWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: bf0a9752162c1593928e1bed270859ec4166230fe1f7e2d46d979c5c989ca237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452991"
---
# <a name="ischaralphanumericwrapw-function"></a>Função IsCharAlphaNumericWrapW

\[o **IsCharAlphaNumericWrapW** está disponível para uso no Windows XP. Ele não estará disponível nas versões subsequentes. Você deve usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) em seu lugar.\]

Determina se um caractere é um caractere alfabético ou numérico. Essa determinação se baseia na semântica do idioma selecionado pelo usuário durante a instalação ou por meio do painel de controle.

> [!Note]  
> **IsCharAlphaNumericWrapW** é um wrapper para a função **IsCharAlphaNumericW** . Consulte a página [**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsCharAlphaNumericWrapW(
  _In_ WCHAR ch
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ch* \[ no\]
</dt> <dd>

Tipo: **WCHAR**

O caractere Unicode a ser testado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **bool**

Se o caractere for alfanumérico, o valor de retorno será diferente de zero.

Se o caractere não for alfanumérico, o valor de retorno será zero. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

o **IsCharAlphaNumericWrapW** fornece a capacidade de usar cadeias de caracteres Unicode em sistemas operacionais anteriores ao Windows XP. O método preferencial é usar [**IsCharAlphaNumericW**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica) em conjunto com a camada Microsoft para Unicode (MSLU).

**IsCharAlphaNumericWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 28.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IsCharAlphaNumeric**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)
</dt> </dl>

 

 
