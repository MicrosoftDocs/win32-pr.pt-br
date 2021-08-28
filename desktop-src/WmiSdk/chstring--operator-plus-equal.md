---
description: O operador de concatenação + = une caracteres ao final desta cadeia de caracteres. O operador aceita outro objeto CHString, um ponteiro de caractere ou um único caractere.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'CHString:: Operator + = (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 316f5272c7b5a4ef5b59e93dd480ade215e3279ea754f1da5432448d46fcce17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679872"
---
# <a name="chstringoperator"></a>CHString:: Operator + =

\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O operador de concatenação + = une caracteres ao final desta cadeia de caracteres. O operador aceita outro objeto [**CHString**](chstring.md) , um ponteiro de caractere ou um único caractere.

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="string"></span><span id="STRING"></span>*Strings*
</dt> <dd>

Uma cadeia de caracteres [**CHString**](chstring.md) que concatena a esta cadeia de caracteres.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*CH*
</dt> <dd>

Um caractere para concatenar a esta cadeia de caracteres.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em **nulo** para concatenar a esta cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

Lembre-se de que as exceções de memória podem ocorrer sempre que você usar esse operador de concatenação porque um novo armazenamento pode ser alocado para caracteres adicionados a esse objeto [**CHString**](chstring.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso de **CHString:: Operator + =**:


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>ChString. h (incluir FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

