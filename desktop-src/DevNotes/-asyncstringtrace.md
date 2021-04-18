---
description: Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo sprintf.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Função AsyncStringTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751355"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="0adcf-103">Função AsyncStringTrace</span><span class="sxs-lookup"><span data-stu-id="0adcf-103">AsyncStringTrace function</span></span>

<span data-ttu-id="0adcf-104">Conclui a configuração de um buffer de rastreamento com campos opcionais para rastreamentos de estilo **sprintf**.</span><span class="sxs-lookup"><span data-stu-id="0adcf-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="0adcf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0adcf-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="0adcf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0adcf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0adcf-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0adcf-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0adcf-108">Um parâmetro de rastreamento de 32 bits que é usado para filtragem no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0adcf-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="0adcf-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="0adcf-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="0adcf-110">Uma cadeia de caracteres terminada em zero que descreve o formato do rastreamento.</span><span class="sxs-lookup"><span data-stu-id="0adcf-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="0adcf-111">*Marker*</span><span class="sxs-lookup"><span data-stu-id="0adcf-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="0adcf-112">Um marcador para as funções **vsprintf** .</span><span class="sxs-lookup"><span data-stu-id="0adcf-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0adcf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0adcf-113">Return value</span></span>

<span data-ttu-id="0adcf-114">Essa função retorna o comprimento da instrução Trace, em bytes.</span><span class="sxs-lookup"><span data-stu-id="0adcf-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="0adcf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0adcf-115">Remarks</span></span>

<span data-ttu-id="0adcf-116">Exstrace.dll é um componente opcional que é instalado com o protocolo SMTP e o protocolo NNTP (Network News Transfer Protocol).</span><span class="sxs-lookup"><span data-stu-id="0adcf-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="0adcf-117">O tipo de dados da **\_ lista de VA** é um tipo padrão usado para manter as informações necessárias pelas macros **VA \_ ARG** e **VA \_ end** .</span><span class="sxs-lookup"><span data-stu-id="0adcf-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="0adcf-118">Para obter mais informações, consulte [tipos padrão](/cpp/c-runtime-library/standard-types?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="0adcf-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="0adcf-119">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0adcf-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0adcf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0adcf-120">Requirements</span></span>



| <span data-ttu-id="0adcf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0adcf-121">Requirement</span></span> | <span data-ttu-id="0adcf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0adcf-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0adcf-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0adcf-123">DLL</span></span><br/> | <dl> <span data-ttu-id="0adcf-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0adcf-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

