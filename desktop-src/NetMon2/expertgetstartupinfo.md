---
description: A função ExpertGetStartupInfo recupera as informações de configuração de inicialização para o especialista.
ms.assetid: 15f080ed-50b7-40c6-b283-dbe416a2b0e9
title: Função ExpertGetStartupInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetStartupInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f34ecc3d0c3eeb085d2a7c0f8c4cb0426663093c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370598"
---
# <a name="expertgetstartupinfo-function"></a><span data-ttu-id="97c08-103">Função ExpertGetStartupInfo</span><span class="sxs-lookup"><span data-stu-id="97c08-103">ExpertGetStartupInfo function</span></span>

<span data-ttu-id="97c08-104">A função **ExpertGetStartupInfo** recupera as informações de configuração de inicialização para o especialista.</span><span class="sxs-lookup"><span data-stu-id="97c08-104">The **ExpertGetStartupInfo** function retrieves the startup configuration information for the expert.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c08-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97c08-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertGetStartupInfo(
  _In_  HEXPERTKEY         hExpertKey,
  _Out_ PEXPERTSTARTUPINFO pExpertStartupInfo
);
```



## <a name="parameters"></a><span data-ttu-id="97c08-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97c08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c08-107">*hExpertKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="97c08-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c08-108">Identificador de especialista exclusivo.</span><span class="sxs-lookup"><span data-stu-id="97c08-108">Unique expert identifier.</span></span> <span data-ttu-id="97c08-109">Monitor de Rede passa *hExpertKey* para o especialista ao chamar a função [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="97c08-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="97c08-110">*pExpertStartupInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="97c08-110">*pExpertStartupInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97c08-111">Ponteiro para uma estrutura [EXPERTSTARTUPINFO](expertstartupinfo.md) que contém informações de inicialização.</span><span class="sxs-lookup"><span data-stu-id="97c08-111">Pointer to an [EXPERTSTARTUPINFO](expertstartupinfo.md) structure that contains startup information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c08-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="97c08-112">Return value</span></span>

<span data-ttu-id="97c08-113">Se a função for bem-sucedida, o valor de retorno será NMERR com \_ êxito.</span><span class="sxs-lookup"><span data-stu-id="97c08-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="97c08-114">Se a função não for bem-sucedida, o valor de retorno será NMERR.</span><span class="sxs-lookup"><span data-stu-id="97c08-114">If the function is unsuccessful, the return value is NMERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c08-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="97c08-115">Remarks</span></span>

<span data-ttu-id="97c08-116">A função **ExpertGetStartupInfo** será usada se o especialista precisar determinar as informações de inicialização usadas.</span><span class="sxs-lookup"><span data-stu-id="97c08-116">The **ExpertGetStartupInfo** function is used if the expert must determine the startup information that is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c08-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97c08-117">Requirements</span></span>



| <span data-ttu-id="97c08-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c08-118">Requirement</span></span> | <span data-ttu-id="97c08-119">Valor</span><span class="sxs-lookup"><span data-stu-id="97c08-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97c08-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97c08-120">Minimum supported client</span></span><br/> | <span data-ttu-id="97c08-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="97c08-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="97c08-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97c08-122">Minimum supported server</span></span><br/> | <span data-ttu-id="97c08-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="97c08-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97c08-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="97c08-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="97c08-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c08-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="97c08-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="97c08-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="97c08-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c08-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="97c08-128">DLL</span><span class="sxs-lookup"><span data-stu-id="97c08-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97c08-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c08-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




