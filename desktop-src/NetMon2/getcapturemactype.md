---
description: A função GetCaptureMacType retorna o tipo de MAC de uma determinada captura.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Função GetCaptureMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646798"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="2f169-103">Função GetCaptureMacType</span><span class="sxs-lookup"><span data-stu-id="2f169-103">GetCaptureMacType function</span></span>

<span data-ttu-id="2f169-104">A função **GetCaptureMacType** retorna o tipo de Mac de uma determinada captura.</span><span class="sxs-lookup"><span data-stu-id="2f169-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f169-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f169-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="2f169-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f169-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f169-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2f169-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f169-108">Identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="2f169-108">Handle to the capture.</span></span> <span data-ttu-id="2f169-109">Para obter informações sobre como obter o identificador de captura, consulte a seção comentários neste tópico de **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="2f169-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f169-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2f169-110">Return value</span></span>

<span data-ttu-id="2f169-111">Se a função for bem-sucedida, o valor de retorno será um dos tipos de MAC a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f169-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="2f169-112">tipo de MAC \_ \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="2f169-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="2f169-113">tipo de MAC \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="2f169-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="2f169-114">tipo de MAC \_ \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="2f169-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="2f169-115">tipo de MAC \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="2f169-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="2f169-116">Se a função não for bem-sucedida, o valor de retorno será um código de erro.</span><span class="sxs-lookup"><span data-stu-id="2f169-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="2f169-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2f169-117">Return code</span></span>                                                                                              | <span data-ttu-id="2f169-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f169-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="2f169-119"><dt>**tipo de NMERR de \_ Mac \_ \_ desconhecido**</dt></span><span class="sxs-lookup"><span data-stu-id="2f169-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="2f169-120">Monitor de Rede não pôde encontrar um tipo de MAC conhecido.</span><span class="sxs-lookup"><span data-stu-id="2f169-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f169-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f169-121">Remarks</span></span>

<span data-ttu-id="2f169-122">O identificador da captura pode ser obtido de várias maneiras, dependendo de quem faz a chamada.</span><span class="sxs-lookup"><span data-stu-id="2f169-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="2f169-123">Para especialistas, o identificador é especificado no membro **hCapture** da estrutura [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="2f169-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="2f169-124">Para analisadores, o identificador de captura pode ser obtido chamando a função [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="2f169-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="2f169-125">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="2f169-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f169-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f169-126">Requirements</span></span>



| <span data-ttu-id="2f169-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f169-127">Requirement</span></span> | <span data-ttu-id="2f169-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2f169-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f169-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f169-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f169-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f169-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2f169-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f169-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f169-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2f169-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2f169-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2f169-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f169-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f169-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2f169-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f169-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f169-136"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f169-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f169-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2f169-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f169-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f169-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




