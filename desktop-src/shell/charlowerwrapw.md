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
ms.openlocfilehash: c9a02e89713dd82de63817c00d5402fabe991fed565ebe33fa40286ad30058d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710746"
---
# <a name="charlowerwrapw-function"></a>Função CharLowerWrapW

\[**CharLowerWrapW** está disponível para uso no Windows XP. Ele pode não estar disponível em versões subsequentes. Você deve usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) em seu lugar.\]

Converte uma cadeia de caracteres Unicode ou um único caractere em minúsculas. Se o operand for uma cadeia de caracteres, a função converterá os caracteres no local.

> [!Note]  
> **CharLowerWrapW** é um wrapper para a **função CharLowerW.** Consulte a [**página CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera) para ver mais observações de uso.

 

## <a name="syntax"></a>Sintaxe


```C++
LPWSTR CharLowerWrapW(
  _Inout_ LPWSTR pch
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pch* \[ in, out\]
</dt> <dd>

Tipo: **LPWSTR**

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo ou um único caractere. Se a palavra de ordem alta desse parâmetro for zero, a palavra de ordem baixa deverá conter apenas um único caractere a ser convertido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LPWSTR**

Se *pch for uma* cadeia de caracteres, a função retornará um ponteiro para a cadeia de caracteres convertida. Como a cadeia de caracteres é convertida no local, o valor de retorno é igual a *pch*.

Se *pch* for um único caractere, o valor de retorno será um valor de 32 bits cuja palavra de ordem alta é zero e a palavra de ordem baixa contém o caractere convertido.

Não há nenhuma indicação de êxito ou falha. A falha é rara. Não há informações de erro estendidas para essa função; não chame [**GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentários

O método preferencial é usar [**CharLowerW**](/windows/win32/api/winuser/nf-winuser-charlowera) em conjunto com o MSLU (Camada da Microsoft para Unicode).

**CharLowerWrapW** deve ser chamado diretamente do Shlwapi.dll, usando o ordinal 38.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CharLower**](/windows/win32/api/winuser/nf-winuser-charlowera)
</dt> </dl>

 

 
