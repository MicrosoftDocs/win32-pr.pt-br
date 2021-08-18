---
description: Função SetAsyncTraceParamsEx – termina a configuração de um buffer de rastreamento com campos opcionais para rastreamentos no estilo sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Função SetAsyncTraceParamsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 6c41369e8a0d73a56dc5d9d831d0028e87a7ecec300f2e43a625f17bd25bede1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538857"
---
# <a name="setasynctraceparamsex-function"></a>Função SetAsyncTraceParamsEx

Termina a configuração de um buffer de rastreamento com campos opcionais para **rastreamentos de estilo sprintf.**

## <a name="syntax"></a>Sintaxe


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszModule* 
</dt> <dd>

O nome do módulo associado ao rastreamento.

</dd> <dt>

*pszFile* 
</dt> <dd>

O nome do arquivo de origem que contém a exceção.

</dd> <dt>

*lLine* 
</dt> <dd>

O número de linha da exceção no arquivo de origem.

</dd> <dt>

*pszFunction* 
</dt> <dd>

O nome da função da exceção.

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

Uma constante de sinalizador de rastreamento que representa um dos tipos de rastreamento disponíveis. Esse parâmetro pode ser qualquer um dos valores a seguir.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL \_ MÁSCARA \_ DE RASTREAMENTO** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERRO \_ MÁSCARA \_ DE RASTREAMENTO** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEPURAÇÃO \_ MÁSCARA \_ DE RASTREAMENTO** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**ESTADO \_ MÁSCARA \_ DE RASTREAMENTO** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_ MÁSCARA \_ DE RASTREAMENTO** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MENSAGEM \_ MÁSCARA \_ DE RASTREAMENTO** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL \_ MÁSCARA \_ DE RASTREAMENTO** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função retornará 1 se a função for bem-sucedida; caso contrário, retornará 0.

## <a name="remarks"></a>Comentários

Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP.

Essa função não tem nenhuma biblioteca de importação ou arquivo de header associado; você deve chamá-lo usando [**as funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**e GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
