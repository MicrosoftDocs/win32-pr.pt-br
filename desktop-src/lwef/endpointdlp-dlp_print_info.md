---
description: Especifica informações sobre um documento que está associado a uma operação de impressão de DLP de ponto de extremidade.
title: Estrutura de DLP_PRINT_INFO (endpointdlp. h)
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
ms.openlocfilehash: 37bde9f62de07083aac6a3d2fb367b021caf3732
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495363"
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

