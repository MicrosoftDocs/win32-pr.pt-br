---
description: Recupera uma cadeia de caracteres de mensagem não formatada quando um identificador de código de erro (IDA) é fornecido.
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: Função JetErrIDARawMessage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749412"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="ab068-103">Função JetErrIDARawMessage</span><span class="sxs-lookup"><span data-stu-id="ab068-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="ab068-104">Recupera uma cadeia de caracteres de mensagem não formatada quando um identificador de código de erro (IDA) é fornecido.</span><span class="sxs-lookup"><span data-stu-id="ab068-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab068-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab068-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="ab068-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab068-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab068-107">*Ida*</span><span class="sxs-lookup"><span data-stu-id="ab068-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="ab068-108">Um número que mapeia para um código de erro específico e é exibido para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ab068-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="ab068-109">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="ab068-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="ab068-110">Um ponteiro para a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="ab068-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="ab068-111">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="ab068-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="ab068-112">Uma contagem do número de bytes na mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="ab068-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="ab068-113">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="ab068-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="ab068-114">Um ponteiro para o número real de bytes lidos.</span><span class="sxs-lookup"><span data-stu-id="ab068-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="ab068-115">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="ab068-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="ab068-116">Um ponteiro para o identificador de contexto associado ao arquivo de ajuda.</span><span class="sxs-lookup"><span data-stu-id="ab068-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="ab068-117">*pwszHelp/arquivo*</span><span class="sxs-lookup"><span data-stu-id="ab068-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="ab068-118">Um ponteiro para um ponteiro para o arquivo que explica o erro.</span><span class="sxs-lookup"><span data-stu-id="ab068-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab068-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab068-119">Return value</span></span>

<span data-ttu-id="ab068-120">Se a função tiver êxito, ela retornará **Jet \_ errSuccess**; caso contrário, ela retornará uma mensagem não formatada que indica o motivo específico da falha.</span><span class="sxs-lookup"><span data-stu-id="ab068-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab068-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab068-121">Remarks</span></span>

<span data-ttu-id="ab068-122">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ab068-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab068-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab068-123">Requirements</span></span>



| <span data-ttu-id="ab068-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab068-124">Requirement</span></span> | <span data-ttu-id="ab068-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ab068-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab068-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ab068-126">DLL</span></span><br/> | <dl> <span data-ttu-id="ab068-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab068-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
