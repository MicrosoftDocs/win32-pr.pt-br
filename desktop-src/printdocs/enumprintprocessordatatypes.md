---
description: A função EnumPrintProcessorDatatypes enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.
ms.assetid: 27b6e074-d303-446b-9e5f-6cfa55c30d26
title: Função EnumPrintProcessorDatatypes (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessorDatatypes
- EnumPrintProcessorDatatypesA
- EnumPrintProcessorDatatypesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 39742aff1fce73b6dac138e77f2f8c794428ff3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505843"
---
# <a name="enumprintprocessordatatypes-function"></a>Função EnumPrintProcessorDatatypes

A função **EnumPrintProcessorDatatypes** enumera os tipos de dados aos quais um processador de impressão especificado dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumPrintProcessorDatatypes(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pPrintProcessorName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDatatypes,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o processador de impressão reside. Se esse parâmetro for **nulo**, os tipos de dados do processador de impressão local serão enumerados.

</dd> <dt>

*pPrintProcessorName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão cujos tipos de dados são enumerados.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de informação retornado no buffer *pDatatypes* . Esse parâmetro deve ser 1.

</dd> <dt>

*pDatatypes* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de tipos de conjuntos de [**\_ informações \_ 1**](datatypes-info-1.md) estruturas. Cada estrutura descreve um tipo de dados disponível. O buffer deve ser grande o suficiente para receber a matriz de estruturas e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.

Para determinar o tamanho do buffer necessário, chame **EnumPrintProcessorDatatypes** com *cbBuf* definido como zero. **EnumPrintProcessorDatatypes** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pDatatypes*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pDatatypes* se a função for realizada com sucesso. Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.

</dd> <dt>

*pcReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas retornadas no buffer *pDatatypes* . Este é o número de tipos de dados com suporte.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

v

A partir do Windows Vista, as informações de tipo de dados de servidores de impressão remotos são recuperadas de um cache local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrintProcessorDatatypesW** (Unicode) e **EnumPrintProcessorDatatypesA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Informações de tipos de tipo \_ \_ 1**](datatypes-info-1.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

