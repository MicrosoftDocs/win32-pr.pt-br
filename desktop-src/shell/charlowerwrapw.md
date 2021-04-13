---
description: Converte uma cadeia de caracteres Unicode ou um único caractere em minúsculas.
ms.assetid: 09b7cf8e-6aed-40f4-9dfa-29be3559ae89
title: Função CharLowerWrapW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CharLowerWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 3911e0366d30f3eb9420391f9d06867ded73530e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501438"
---
# <a name="charlowerwrapw-function"></a>Função CharLowerWrapW

\[O **CharLowerWrapW** está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Você deve usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) em seu lugar.\]

Converte uma cadeia de caracteres Unicode ou um único caractere em minúsculas. Se o operando for uma cadeia de caracteres, a função converterá os caracteres em vigor.

> [!Note]  
> **CharLowerWrapW** é um wrapper para a função **CharLowerW** . Consulte a página [**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PCH* \[ entrada, saída\]
</dt> <dd>

Tipo: **LPWSTR**

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo ou um único caractere. Se a palavra de ordem superior desse parâmetro for zero, a palavra de ordem inferior deverá conter apenas um único caractere a ser convertido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LPWSTR**

Se *PCH* for uma cadeia de caracteres, a função retornará um ponteiro para a cadeia de caracteres convertida. Como a cadeia de caracteres é convertida em vigor, o valor de retorno é igual a *PCH*.

Se *PCH* for um único caractere, o valor de retorno será um valor de 32 bits cuja palavra de ordem superior é zero e a palavra de ordem inferior conterá o caractere convertido.

Não há nenhuma indicação de êxito ou falha. A falha é rara. Não há informações de erro estendidas para esta função; Não chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Comentários

O método preferencial é usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) em conjunto com a camada Microsoft para Unicode (MSLU).

**CharLowerWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 38.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
