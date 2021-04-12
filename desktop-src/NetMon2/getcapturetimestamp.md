---
description: A função GetCaptureTimeStamp retorna a hora e a data em que a captura começou a gravar quadros.
ms.assetid: a7120a7c-5031-4c71-a177-f08c41037b3c
title: Função GetCaptureTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 855aa8b5432fd06bb25571fcb48c091dcfe502f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501351"
---
# <a name="getcapturetimestamp-function"></a><span data-ttu-id="d1bdf-103">Função GetCaptureTimeStamp</span><span class="sxs-lookup"><span data-stu-id="d1bdf-103">GetCaptureTimeStamp function</span></span>

<span data-ttu-id="d1bdf-104">A função **GetCaptureTimeStamp** retorna a hora e a data em que a captura começou a gravar quadros.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-104">The **GetCaptureTimeStamp** function returns the time and date when the capture started recording frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1bdf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1bdf-105">Syntax</span></span>


```C++
LPSYSTEMTIME WINAPI GetCaptureTimeStamp(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="d1bdf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1bdf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1bdf-107">*hCapture* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d1bdf-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bdf-108">Identificador para a captura.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-108">Handle to the capture.</span></span> <span data-ttu-id="d1bdf-109">Para obter informações sobre como obter o identificador de captura, consulte a seção comentários deste tópico do **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="d1bdf-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTimeStamp** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1bdf-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1bdf-110">Return value</span></span>

<span data-ttu-id="d1bdf-111">Se a função for bem-sucedida, o valor de retorno será um ponteiro para uma estrutura [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="d1bdf-111">If the function is successful, the return value is a pointer to a [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

<span data-ttu-id="d1bdf-112">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-112">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1bdf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1bdf-113">Remarks</span></span>

<span data-ttu-id="d1bdf-114">A função **GetCaptureTimeStamp** retorna a hora em que o provedor de pacotes de rede (NPP) começa a coletar dados, e não quando o especialista carrega a captura para análise.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-114">The **GetCaptureTimeStamp** function returns the time when the Network Packet Provider (NPP) starts collecting data, not when the expert loads the capture for analysis.</span></span>

<span data-ttu-id="d1bdf-115">Não substitua os dados na estrutura **SYSTEMTIME** .</span><span class="sxs-lookup"><span data-stu-id="d1bdf-115">Do not overwrite the data in the **SYSTEMTIME** structure.</span></span> <span data-ttu-id="d1bdf-116">Os dados fazem parte da captura.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-116">The data is part of the capture.</span></span> <span data-ttu-id="d1bdf-117">A tentativa de modificar os dados causa uma violação de acesso.</span><span class="sxs-lookup"><span data-stu-id="d1bdf-117">Trying to modify the data causes an access violation.</span></span>

<span data-ttu-id="d1bdf-118">Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetCaptureTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="d1bdf-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1bdf-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1bdf-119">Requirements</span></span>



| <span data-ttu-id="d1bdf-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1bdf-120">Requirement</span></span> | <span data-ttu-id="d1bdf-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d1bdf-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1bdf-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1bdf-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d1bdf-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1bdf-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d1bdf-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1bdf-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d1bdf-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1bdf-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d1bdf-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1bdf-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1bdf-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1bdf-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d1bdf-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1bdf-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1bdf-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1bdf-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1bdf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d1bdf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1bdf-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1bdf-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1bdf-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1bdf-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1bdf-133">SYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="d1bdf-133">SYSTEMTIME</span></span>](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

 

