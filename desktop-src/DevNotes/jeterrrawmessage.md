---
description: Recupera um IDA (identificador de código de erro) e uma cadeia de caracteres de mensagem não formatada quando um erro de Jet é fornecido.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: Função JetErrRawMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751955"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="a6fb2-103">Função JetErrRawMessage</span><span class="sxs-lookup"><span data-stu-id="a6fb2-103">JetErrRawMessage function</span></span>

<span data-ttu-id="a6fb2-104">Recupera um IDA (identificador de código de erro) e uma cadeia de caracteres de mensagem não formatada quando um erro de Jet é fornecido.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6fb2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6fb2-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="a6fb2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6fb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6fb2-107">*erra*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-108">O erro de Jet que corresponde às informações que estão sendo obtidas.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="a6fb2-109">*pIda*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-110">Um ponteiro para IDA.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="a6fb2-111">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-112">Um ponteiro para a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="a6fb2-113">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-114">Uma contagem do número de bytes na mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="a6fb2-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-116">Um ponteiro para o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="a6fb2-117">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-118">Um ponteiro para o identificador de contexto associado ao arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="a6fb2-119">*pwszHelp/arquivo*</span><span class="sxs-lookup"><span data-stu-id="a6fb2-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="a6fb2-120">Aponta para um ponteiro para o arquivo que explica o erro.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6fb2-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6fb2-121">Return value</span></span>

<span data-ttu-id="a6fb2-122">Se a função for realizada com êxito, ela retornará **Jet \_ errSuccess**; caso contrário, ela retornará uma mensagem de erro não formatada que indica o motivo específico da falha.</span><span class="sxs-lookup"><span data-stu-id="a6fb2-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6fb2-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6fb2-123">Remarks</span></span>

<span data-ttu-id="a6fb2-124">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="a6fb2-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6fb2-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6fb2-125">Requirements</span></span>



| <span data-ttu-id="a6fb2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6fb2-126">Requirement</span></span> | <span data-ttu-id="a6fb2-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a6fb2-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fb2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a6fb2-128">DLL</span></span><br/> | <dl> <span data-ttu-id="a6fb2-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6fb2-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
