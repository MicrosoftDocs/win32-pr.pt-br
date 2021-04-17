---
description: Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo sprintf.
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
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748696"
---
# <a name="setasynctraceparamsex-function"></a>Função SetAsyncTraceParamsEx

Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo **sprintf**.

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

O nome do módulo que está associado ao rastreamento.

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

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Fatal \_ \_Máscara de rastreamento** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Erro \_ do \_Máscara de rastreamento** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Depurar \_ \_Máscara de rastreamento** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Estado \_ \_Máscara de rastreamento** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**\_ Funct \_Máscara de rastreamento** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Mensagem \_ de \_Máscara de rastreamento** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Todos \_ \_Máscara de rastreamento** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retornará 1 se a função tiver sucesso; caso contrário, retornará 0.

## <a name="remarks"></a>Comentários

Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
