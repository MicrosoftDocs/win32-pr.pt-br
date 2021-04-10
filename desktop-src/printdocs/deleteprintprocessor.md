---
description: A função DeletePrintProcessor remove um processador de impressão adicionado pela função AddPrintProcessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: Função DeletePrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 241efaad91e1587209f2ef2a905bc0e095c6b40c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169349"
---
# <a name="deleteprintprocessor-function"></a>Função DeletePrintProcessor

A função **DeletePrintProcessor** remove um processador de impressão adicionado pela função [**AddPrintProcessor**](addprintprocessor.md) .

## <a name="syntax"></a>Sintaxe


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o processador deve ser removido. Se esse parâmetro for **nulo**, o processador da impressora será removido localmente.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o processador deve ser removido (por exemplo, Windows NT x86, Windows IA64 ou Windows x64). Se esse parâmetro for **nulo**, o processador será removido do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão). **NULL** é o valor recomendado, pois fornece a portabilidade máxima.

</dd> <dt>

*pPrintProcessorName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **DeletePrintProcessorW** (Unicode) e **DeletePrintProcessorA** (ANSI)<br/>                       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

