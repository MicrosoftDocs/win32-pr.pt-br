---
description: O operador chString assignment (=) reinicializa um objeto CHString existente com novos dados.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: CHString::operator= (ChString.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dde67bbf0f1a7326074bc7638cdd6b256ad763e115ad12e2c193e6bcdc66605e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131778"
---
# <a name="chstringoperator"></a>CHString::operator=

\[A [**classe CHString**](chstring.md) faz parte do WMI Provider Framework, que agora é considerado no estado final e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estará disponível para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

O [**operador chString**](chstring.md) assignment (=) reinicializa um objeto CHString existente com novos dados.

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*
</dt> <dd>

Atribui uma cadeia [**de caracteres CHString**](chstring.md) a esse objeto.

</dd> <dt>

<span id="ch"></span><span id="CH"></span>*Ch*
</dt> <dd>

Atribui um caractere a este objeto .

</dd> <dt>

<span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*
</dt> <dd>

Atribui uma cadeia de caracteres terminada em **NULL** a esse objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a cadeia de caracteres de destino (ou seja, o lado esquerdo) já for grande o suficiente para armazenar os novos dados, nenhuma nova alocação de memória será executada. No entanto, exceções de memória podem ocorrer sempre que você usar o operador de atribuição porque o novo armazenamento geralmente é alocado para armazenar o objeto [**CHString**](chstring.md) resultante.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra o uso **de CHString::operator =**:


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| Cabeçalho<br/>                   | <dl> <dt>ChString.h (inclua FwCommon.h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CHString**](chstring.md)
</dt> </dl>

 

