---
description: A função AddPrintProcessor instala um processador de impressão no servidor especificado e adiciona o nome do processador de impressão à lista de processadores de impressão com suporte.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: Função AddPrintProcessor (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 83de05dd6aa0ef6541322a45894dcf24cffa3cc6bebcbbd3b42e6c48941360b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117868741"
---
# <a name="addprintprocessor-function"></a>Função AddPrintProcessor

A função **AddPrintProcessor** instala um processador de impressão no servidor especificado e adiciona o nome do processador de impressão à lista de processadores de impressão com suporte.

## <a name="syntax"></a>Sintaxe


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor no qual o processador de impressão deve ser instalado. Se esse parâmetro for **nulo**, o processador de impressão será instalado localmente.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL**, o ambiente atual do chamador/cliente (não do destino/servidor) será usado.

</dd> <dt>

*pPathName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo que contém o processador de impressão. Esse arquivo deve estar no diretório de processador de impressão do sistema.

</dd> <dt>

*pPrintProcessorName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

Antes de chamar a função **AddPrintProcessor** , um aplicativo deve verificar se o arquivo que contém o processador de impressão está armazenado no diretório do processador de impressão do sistema. Um aplicativo pode recuperar o nome do diretório do processador de impressão do sistema chamando a função [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .

Um aplicativo pode determinar o nome dos processadores de impressão existentes chamando a função [**EnumPrintProcessors**](enumprintprocessors.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AddPrintProcessorW** (Unicode) e **AddPrintProcessorA** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> <dt>

[**GetPrintProcessorDirectory**](getprintprocessordirectory.md)
</dt> </dl>

 

