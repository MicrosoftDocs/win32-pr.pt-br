---
description: A tabela a seguir lista os métodos CHString.
ms.assetid: e2e4378f-d842-4bca-bffc-a60e718caed3
ms.tgt_platform: multiple
title: Classe CHString (ChString. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CHString
- ??1CHString@@QAE@XZ
- ??1CHString@@QEAA@XZ
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 0c94fcd89a41e610d039afe17f4b56e58cb117bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763519"
---
# <a name="chstring-class"></a>Classe CHString

\[A classe **CHString** faz parte da estrutura do provedor de WMI, que agora é considerada no estado final, e nenhum outro desenvolvimento, melhoria ou atualização estará disponível para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

A tabela a seguir lista os métodos **CHString** .

## <a name="members"></a>Membros

A classe **CHString** tem estes tipos de membros:

-   [Construtores](#constructors)
-   [Métodos](#methods)
-   [Operadores](#operators)

### <a name="constructors"></a>Construtores

A classe **CHString** tem esses construtores.



| Construtor                           | Descrição                                                 |
|:--------------------------------------|:------------------------------------------------------------|
| [**CHString**](/windows/desktop/api/ChString/nf-chstring-chstring-chstring(constchstring_)) | Constrói cadeias de caracteres **CHString** de várias maneiras.<br/> |



 

### <a name="methods"></a>Métodos

A classe **CHString** tem esses métodos.



| Método                                                    | Descrição                                                                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [**AllocSysString**](/windows/desktop/api/ChString/nf-chstring-chstring-allocsysstring)         | Aloca um BSTR a partir de dados **CHString** .<br/>                                                            |
| [**COLLATE**](/windows/desktop/api/ChString/nf-chstring-chstring-collate)                       | Compara duas cadeias de caracteres (diferencia maiúsculas de minúsculas; usa informações específicas de localidade).<br/>                            |
| [**Comparar**](/windows/desktop/api/ChString/nf-chstring-chstring-compare)                       | Compara duas cadeias de caracteres (diferencia maiúsculas de minúsculas).<br/>                                                              |
| [**CompareNoCase**](/windows/desktop/api/ChString/nf-chstring-chstring-comparenocase)           | Compara duas cadeias de caracteres (não diferencia maiúsculas de minúsculas).<br/>                                                            |
| [**Esvaziá**](/windows/desktop/api/ChString/nf-chstring-chstring-empty)                           | Força uma cadeia de caracteres a ter um comprimento de 0 (zero).<br/>                                                            |
| [**Localizar**](/windows/win32/api/chstring/nf-chstring-chstring-find(wchar))                        | Sobrecarregado. Localiza um caractere ou uma subcadeia de caracteres dentro de uma cadeia de caracteres maior.<br/>                                  |
| [**FindOneOf**](/windows/desktop/api/ChString/nf-chstring-chstring-findoneof)                   | Localiza o primeiro caractere correspondente de um conjunto.<br/>                                                      |
| [**Ao**](/windows/desktop/api/ChString/nf-chstring-chstring-format(uint_---))                         | Sobrecarregado. Formata a cadeia de caracteres como **sprintf** .<br/>                                                 |
| [**FormatMessageW**](/windows/desktop/api/ChString/nf-chstring-chstring-formatmessagew(uint_---))         | Sobrecarregado. Formata uma cadeia de caracteres de mensagem.<br/>                                                               |
| [**FormatV**](/windows/desktop/api/ChString/nf-chstring-chstring-formatv)                       | Formata a cadeia de caracteres como **vsprintf** .<br/>                                                            |
| [**FreeExtra**](/windows/desktop/api/ChString/nf-chstring-chstring-freeextra)                   | Remove qualquer sobrecarga dessa cadeia de caracteres liberando qualquer memória extra alocada anteriormente para a cadeia de caracteres.<br/> |
| [**GetAllocLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getalloclength)         | Retorna o tamanho do buffer de cadeia de caracteres.<br/>                                                              |
| [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int))                           | Sobrecarregado. Retorna o caractere em uma determinada posição.<br/>                                              |
| [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer)                   | Retorna um ponteiro para os caracteres na cadeia de caracteres **CHString** .<br/>                                     |
| [**GetBufferSetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffersetlength) | Retorna um ponteiro para os caracteres na cadeia de caracteres **CHString** , truncando para o comprimento especificado.<br/> |
| [**GetData**](/windows/desktop/api/ChString/nf-chstring-chstring-getdata)                       | Retorna um ponteiro para os dados na cadeia de caracteres **CHString** .<br/>                                           |
| [**GetLength**](/windows/desktop/api/ChString/nf-chstring-chstring-getlength)                   | Retorna o número de caracteres Unicode em uma cadeia de caracteres **CHString** .<br/>                                  |
| [**IsEmpty**](/windows/desktop/api/ChString/nf-chstring-chstring-isempty)                       | Testa se uma cadeia de caracteres **CHString** não contém caracteres.<br/>                                         |
| [**Mantida**](/windows/desktop/api/ChString/nf-chstring-chstring-left)                             | Extrai a parte esquerda de uma cadeia de caracteres (como a função básica **$ Left** ).<br/>                             |
| [**LoadStringW**](/windows/desktop/api/ChString/nf-chstring-chstring-loadstringw(uint))               | Carrega uma cadeia de caracteres **CHString** existente de um arquivo de recurso.<br/>                                         |
| [**LockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-lockbuffer)                 | Desabilita a contagem de referência e protege a cadeia de caracteres no buffer.<br/>                                  |
| [**MakeLower**](/windows/desktop/api/ChString/nf-chstring-chstring-makelower)                   | Converte todos os caracteres nesta cadeia de caracteres em minúsculas.<br/>                              |
| [**MakeReverse**](/windows/desktop/api/ChString/nf-chstring-chstring-makereverse)               | Inverte os caracteres nesta cadeia de caracteres.<br/>                                                             |
| [**MakeUpper**](/windows/desktop/api/ChString/nf-chstring-chstring-makeupper)                   | Converte todos os caracteres nesta cadeia de caracteres em letras maiúsculas.<br/>                              |
| [**Meio**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))                               | Sobrecarregado. Extrai a parte intermediária de uma cadeia de caracteres (como a função **mid $** básica).<br/>                |
| [**ReleaseBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-releasebuffer)           | Libera o controle do buffer retornado por [**GetBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-getbuffer).<br/>                 |
| [**ReverseFind**](/windows/desktop/api/ChString/nf-chstring-chstring-reversefind)               | Localiza um caractere dentro de uma cadeia de caracteres maior; inicia a partir do final.<br/>                                      |
| [**Certo**](/windows/desktop/api/ChString/nf-chstring-chstring-right)                           | Extrai a parte direita de uma cadeia de caracteres (como a função básica **$ $** ).<br/>                           |
| [**SetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-setat)                           | Define um caractere em uma determinada posição.<br/>                                                               |
| [**SpanExcluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanexcluding)           | Extrai uma subcadeia de caracteres que contém somente os caracteres que não estão no conjunto.<br/>                     |
| [**SpanIncluding**](/windows/desktop/api/ChString/nf-chstring-chstring-spanincluding)           | Extrai uma subcadeia de caracteres que contém apenas os caracteres em um conjunto.<br/>                                    |
| [**TrimLeft**](/windows/desktop/api/ChString/nf-chstring-chstring-trimleft)                     | Corta os caracteres de espaço em branco à esquerda da cadeia de caracteres.<br/>                                                |
| [**TrimRight**](/windows/desktop/api/ChString/nf-chstring-chstring-trimright)                   | Corta os caracteres de espaço em branco à direita da cadeia de caracteres.<br/>                                               |
| [**UnlockBuffer**](/windows/desktop/api/ChString/nf-chstring-chstring-unlockbuffer)             | Habilita a contagem de referência e libera a cadeia de caracteres no buffer.<br/>                                   |



 

### <a name="operators"></a>Operadores
`
The **CHString** class has these operators.`



| Operador                                                                                            | Descrição                                                                                                       |
|:----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| [**operador! = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385704(v=vs.85))            | Compara dois **CHStrings** para desigualdade.<br/>                                                             |
| [**operador! = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385763(v=vs.85))              | Compara um **CHString** com um **LPCWSTR** para desigualdade.<br/>                                             |
| [**operador \[\]**](/previous-versions/windows/desktop/legacy/aa386162(v=vs.85))                                                | Retorna o caractere em uma determinada substituição de operador de posição para [**GetAt**](/windows/desktop/api/ChString/nf-chstring-chstring-getat(int)).<br/> |
| [**operador +**](chstring--operator-plus.md)                                                       | Concatena duas cadeias de caracteres e retorna uma nova cadeia.<br/>                                                     |
| [**operador + =**](chstring--operator-plus-equal.md)                                                | Concatena uma nova cadeia de caracteres ao final de uma cadeia de caracteres existente.<br/>                                            |
| [**< do operador (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385695(v=vs.85))            | Compara um **CHString** com um **LPCWSTR**.<br/>                                                            |
| [**< do operador (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385689(v=vs.85))          | Compara dois **CHStrings**.<br/>                                                                            |
| [**operador <= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385676(v=vs.85))    | Compara dois **CHStrings**.<br/>                                                                            |
| [**operador <= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385683(v=vs.85))      | Compara um **CHString** com um **LPCWSTR**.<br/>                                                            |
| [**operador =**](chstring--operator-equal.md)                                                      | Atribui um novo valor a uma cadeia de caracteres **CHString** .<br/>                                                          |
| [**Operator = = (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385641(v=vs.85))          | Compara dois **CHStrings** para igualdade.<br/>                                                               |
| [**Operator = = (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385645(v=vs.85))            | Compara um **CHString** com um **LPCWSTR** para igualdade.<br/>                                               |
| [**> do operador (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385665(v=vs.85))       | Compara dois **CHStrings**.<br/>                                                                            |
| [**> do operador (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385672(v=vs.85))         | Compara um **CHString** com um **LPCWSTR**.<br/>                                                            |
| [**operador >= (CHString, CHString)**](/previous-versions/windows/desktop/legacy/aa385652(v=vs.85)) | Compara dois **CHStrings**.<br/>                                                                            |
| [**operador >= (CHString, LPCWSTR)**](/previous-versions/windows/desktop/legacy/aa385661(v=vs.85))   | Compara um **CHString** com um **LPCWSTR**.<br/>                                                            |
| [**LPCWSTR do operador**](/windows/desktop/api/ChString/nf-chstring-chstring-operatorlpcwstr)                                               | Acessa diretamente os caracteres armazenados em uma cadeia de caracteres **CHString** como uma cadeia de estilo C.<br/>                      |



 

## <a name="remarks"></a>Comentários

O destruidor para a classe é **CHString:: ~ CHString**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                                                                                |
| parâmetro<br/>                   | <dl> <dt>ChString. h (incluir FwCommon. h)</dt> </dl>                                                    |
| Biblioteca<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



