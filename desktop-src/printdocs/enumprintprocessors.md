---
description: A função EnumPrintProcessors enumera os processadores de impressão instalados no servidor especificado.
ms.assetid: 98c9185c-c89d-4b4e-8c1e-7e22b315f188
title: Função EnumPrintProcessors (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumPrintProcessors
- EnumPrintProcessorsA
- EnumPrintProcessorsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 800ed5afcf332a0c34dc272158f98fed64e47e86cb3c16cb24d6013951ffd3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846036"
---
# <a name="enumprintprocessors-function"></a>Função EnumPrintProcessors

A função **EnumPrintProcessors** enumera os processadores de impressão instalados no servidor especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumPrintProcessors(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual os processadores de impressão residem. Se esse parâmetro for **nulo**, os processadores de impressão local serão enumerados.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL**, o ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão) será usado.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de informação retornado no buffer *pPrintProcessorInfo* . Esse parâmetro deve ser 1.

</dd> <dt>

*pPrintProcessorInfo* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz de estruturas de [**informações do multiprocessador \_ \_ 1**](printprocessor-info-1.md) . Cada estrutura descreve um processador de impressão disponível. O buffer deve ser grande o suficiente para receber a matriz de estruturas e todas as cadeias de caracteres às quais os membros da estrutura apontam.

Para determinar o tamanho do buffer necessário, chame **EnumPrintProcessors** com *cbBuf* definido como zero. **EnumPrintProcessors** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer apontado por *pPrintProcessorInfo*.

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes copiados para o buffer *pPrintProcessorInfo* se a função for realizada com sucesso. Se o buffer for muito pequeno, a função falhará e a variável receberá o número de bytes necessários.

</dd> <dt>

*pcReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas retornadas no buffer *pPrintProcessorInfo* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumPrintProcessorsW** (Unicode) e **EnumPrintProcessorsA** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> <dt>

[**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md)
</dt> <dt>

[**Informações do multiprocessador \_ \_ 1**](printprocessor-info-1.md)
</dt> </dl>

 

