---
description: Esses operadores de subscrito definem ou obtêm o elemento no índice especificado. Esses operadores são um substituto conveniente para os métodos SetAt e GetAt.
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'CHStringArray:: operator [] (ChStrArr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780423"
---
# <a name="chstringarrayoperator--"></a>Operador \[ CHStringArray:: \]

\[A classe [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

Esses operadores de subscrito definem ou obtêm o elemento no índice especificado. Esses operadores são um substituto conveniente para os métodos [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) e [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) .

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*
</dt> <dd>

Um índice inteiro que é maior ou igual a zero e menor ou igual ao valor retornado por [ **GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)

</dd> </dl>

## <a name="return-values"></a>Valores de retorno

Os operadores de subscrito retornam o elemento de ponteiro [**CHString**](chstring.md) atualmente neste índice.

## <a name="remarks"></a>Comentários

Você pode usar o primeiro operador, que chama matrizes que não são **const**, no lado direito (r-value) ou à esquerda (l-Value) de uma instrução de atribuição. O segundo, que chama matrizes **const** , pode ser usado somente à direita.

A versão de depuração da biblioteca é declarada se o subscrito (no lado esquerdo ou direito de uma instrução de atribuição) está fora dos limites.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra o uso de [**CHStringArray: \[ \] : Operator**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>ChStrArr. h (incluir FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CHStringArray:: Adicionar**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))
</dt> <dt>

[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))
</dt> </dl>

