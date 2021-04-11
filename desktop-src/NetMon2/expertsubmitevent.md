---
description: A função ExpertSubmitEvent indica que existe uma condição de evento e fornece uma estrutura de dados que descreve a condição.
ms.assetid: 2339b530-427b-4028-aef6-c2cdd1353f77
title: Função ExpertSubmitEvent (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertSubmitEvent
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 448d77e9cb009b8aced0aba752526dc08b503066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296201"
---
# <a name="expertsubmitevent-function"></a><span data-ttu-id="52dac-103">Função ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="52dac-103">ExpertSubmitEvent function</span></span>

<span data-ttu-id="52dac-104">A função **ExpertSubmitEvent** indica que existe uma condição de evento e fornece uma estrutura de dados que descreve a condição.</span><span class="sxs-lookup"><span data-stu-id="52dac-104">The **ExpertSubmitEvent** function indicates that an event condition exists and provides a data structure that describes the condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="52dac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="52dac-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertSubmitEvent(
  _In_ HEXPERTKEY   hExpertKey,
  _In_ PNMEVENTDATA pExpertEvent
);
```



## <a name="parameters"></a><span data-ttu-id="52dac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52dac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52dac-107">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52dac-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52dac-108">Identificador exclusivo do especialista.</span><span class="sxs-lookup"><span data-stu-id="52dac-108">Unique identifier of the expert.</span></span> <span data-ttu-id="52dac-109">Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="52dac-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="52dac-110">*pExpertEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="52dac-110">*pExpertEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52dac-111">Um ponteiro para uma estrutura **NMEVENTDATA** que descreve a condição do evento.</span><span class="sxs-lookup"><span data-stu-id="52dac-111">A pointer to an **NMEVENTDATA** structure that describes the event condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52dac-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52dac-112">Return value</span></span>

<span data-ttu-id="52dac-113">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="52dac-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="52dac-114">Se a função não for bem-sucedida, o valor de retorno indicará o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="52dac-114">If the function is unsuccessful, the return value indicates the reason for the failure.</span></span> <span data-ttu-id="52dac-115">Se o valor de retorno for NMERR \_ expert \_ Finalize, o especialista limpará e retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="52dac-115">If the return value is NMERR\_EXPERT\_TERMINATE, the expert immediately cleans up and returns.</span></span>

## <a name="requirements"></a><span data-ttu-id="52dac-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52dac-116">Requirements</span></span>



| <span data-ttu-id="52dac-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="52dac-117">Requirement</span></span> | <span data-ttu-id="52dac-118">Valor</span><span class="sxs-lookup"><span data-stu-id="52dac-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="52dac-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52dac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="52dac-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52dac-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="52dac-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52dac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="52dac-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="52dac-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="52dac-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="52dac-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="52dac-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="52dac-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="52dac-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="52dac-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="52dac-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52dac-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="52dac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="52dac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52dac-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52dac-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




