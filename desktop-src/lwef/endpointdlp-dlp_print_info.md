---
description: Especifica informações sobre um documento que está associado a uma operação de impressão de DLP de ponto de extremidade.
title: Estrutura DLP_PRINT_INFO (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_PRINT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: e55b3dc22c77d85e15499ea0fb2a6634ece044496637c811ae42e4afd632704e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725816"
---
# <a name="dlp_print_info-structure"></a>Estrutura de DLP_PRINT_INFO

Especifica informações sobre um documento que está associado a uma operação de impressão de DLP de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DLP_PRINT_INFO {
    DWORD Version;
    LPCWSTR PrinterName;
    LPCWSTR JobName;
    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;
```


## <a name="members"></a>Membros

<dl> <dt>

*Versão* \[ do no\]
</dt> <dd>

Um DWORD que especifica a versão da API. Esse valor sempre deve ser **DLP_PRINT_INFO_V_LATEST**. Essa constante é definida na listagem de arquivos de cabeçalho de exemplo endpointdlp. h no artigo [prevenção de perda de dados do ponto de extremidade](endpointdlp-endpoint-data-loss-prevention.md).

</dd> </dl>

<dl> <dt>

*PrinterName* \[ no\]
</dt> <dd>

Um LPCWSTR que identifica a impressora de destino.

</dd> </dl>

<dl> <dt>

*JobName* \[ no\]
</dt> <dd>

Um LPCWSTR especificando o nome do trabalho de impressão.

</dd> </dl>

<dl> <dt>

*NomeDoArquivoDeSaída* \[ no\]
</dt> <dd>

Um LPCWSTR que especifica o caminho para o arquivo de saída ao imprimir em um arquivo.

</dd> </dl>



## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |

