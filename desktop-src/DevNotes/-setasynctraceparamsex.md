---
description: Função SetAsyncTraceParamsEx – conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo sprintf.
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
ms.openlocfilehash: 5a9dc0eee2f4ea3f65fa45914c3340a99ac2d45b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085764"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="a4b05-103">Função SetAsyncTraceParamsEx</span><span class="sxs-lookup"><span data-stu-id="a4b05-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="a4b05-104">Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="a4b05-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4b05-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="a4b05-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4b05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b05-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="a4b05-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b05-108">O nome do módulo que está associado ao rastreamento.</span><span class="sxs-lookup"><span data-stu-id="a4b05-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="a4b05-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="a4b05-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b05-110">O nome do arquivo de origem que contém a exceção.</span><span class="sxs-lookup"><span data-stu-id="a4b05-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="a4b05-111">*lLine*</span><span class="sxs-lookup"><span data-stu-id="a4b05-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b05-112">O número de linha da exceção no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="a4b05-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="a4b05-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="a4b05-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b05-114">O nome da função da exceção.</span><span class="sxs-lookup"><span data-stu-id="a4b05-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="a4b05-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="a4b05-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b05-116">Uma constante de sinalizador de rastreamento que representa um dos tipos de rastreamento disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a4b05-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="a4b05-117">Esse parâmetro pode ser qualquer um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a4b05-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a4b05-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Fatal \_ \_Máscara de rastreamento** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="a4b05-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="a4b05-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Erro \_ do \_Máscara de rastreamento** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="a4b05-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="a4b05-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Depurar \_ \_Máscara de rastreamento** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="a4b05-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="a4b05-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Estado \_ \_Máscara de rastreamento** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="a4b05-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="a4b05-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**\_ Funct \_Máscara de rastreamento** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="a4b05-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="a4b05-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Mensagem \_ de \_Máscara de rastreamento** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="a4b05-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="a4b05-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Todos \_ \_Máscara de rastreamento** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="a4b05-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b05-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a4b05-125">Return value</span></span>

<span data-ttu-id="a4b05-126">Essa função retornará 1 se a função tiver sucesso; caso contrário, retornará 0.</span><span class="sxs-lookup"><span data-stu-id="a4b05-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b05-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4b05-127">Remarks</span></span>

<span data-ttu-id="a4b05-128">Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="a4b05-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="a4b05-129">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a4b05-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b05-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4b05-130">Requirements</span></span>



| <span data-ttu-id="a4b05-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4b05-131">Requirement</span></span> | <span data-ttu-id="a4b05-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a4b05-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b05-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a4b05-133">DLL</span></span><br/> | <dl> <span data-ttu-id="a4b05-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4b05-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
