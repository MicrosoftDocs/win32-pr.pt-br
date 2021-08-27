---
description: O operador + concatenation une duas cadeias de caracteres e retorna um objeto CHString.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'CHString:: Operator + (ChString. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ce52e8740fcd420600aaebb192c23ab7269c4ddf14c068a4980c59df3e7773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097346"
---
# <a name="chstringoperator"></a>CHString:: Operator +

\[A classe [**CHString**](chstring.md) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O operador + concatenation une duas cadeias de caracteres e retorna um objeto [**CHString**](chstring.md) .

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*
</dt> <dd>

[**CHString**](chstring.md) cadeias de caracteres que são concatenadas.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*CH*
</dt> <dd>

Um caractere que concatena a uma cadeia de caracteres ou uma cadeia de caracteres que se concatena a um caractere.

</dd> <dt>

<span id="lpsz"></span><span id="LPSZ"></span>*lpsz*
</dt> <dd>

Ponteiro para uma cadeia de caracteres terminada em **nulo**.

</dd> </dl>

## <a name="return-values"></a>Valores de retorno

Esse operador de concatenação retorna um objeto [**CHString**](chstring.md) que é o resultado temporário da concatenação. Esse valor de retorno torna possível combinar várias concatenações na mesma expressão.

## <a name="remarks"></a>Comentários

Uma das duas cadeias de caracteres de argumento deve ser um objeto [**CHString**](chstring.md) ; o outro pode ser um ponteiro de caractere ou um caractere. Lembre-se de que as exceções de memória podem ocorrer sempre que você usar o operador de concatenação porque um novo armazenamento pode ser alocado para manter dados temporários.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra o uso de **CHString:: Operator +**:


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
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

 

