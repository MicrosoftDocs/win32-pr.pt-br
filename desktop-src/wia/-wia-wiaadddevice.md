---
description: A função WiaAddDevice invoca a interface do usuário do assistente de instalação da câmera e scanner. É equivalente a executar &\# 0034; rundll32.exe sti \_ci.dll adddevice&\# 0034; no prompt de comando.
ms.assetid: 83a1e22c-d751-4c8e-8f39-ec987042c745
title: Função WiaAddDevice (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaAddDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 694265f0a59096a5a6a58ccbf4e43c92e21fe9b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647212"
---
# <a name="wiaadddevice-function"></a><span data-ttu-id="b3c51-104">Função WiaAddDevice</span><span class="sxs-lookup"><span data-stu-id="b3c51-104">WiaAddDevice function</span></span>

<span data-ttu-id="b3c51-105">A função **WiaAddDevice** invoca a interface do usuário do assistente de instalação da câmera e scanner.</span><span class="sxs-lookup"><span data-stu-id="b3c51-105">The **WiaAddDevice** function invokes the Scanner and Camera Installation Wizard UI.</span></span> <span data-ttu-id="b3c51-106">É equivalente a executar "rundll32.exe STI \_ci.dll adddevice" no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="b3c51-106">It is equivalent to running "rundll32.exe sti\_ci.dll AddDevice" from the command prompt.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c51-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3c51-107">Syntax</span></span>


```C++
void WINAPI WiaAddDevice(void);
```



## <a name="parameters"></a><span data-ttu-id="b3c51-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3c51-108">Parameters</span></span>

<span data-ttu-id="b3c51-109">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b3c51-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3c51-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3c51-110">Return value</span></span>

<span data-ttu-id="b3c51-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b3c51-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c51-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3c51-112">Remarks</span></span>

<span data-ttu-id="b3c51-113">Essa função deve ser chamada com credenciais de administrador.</span><span class="sxs-lookup"><span data-stu-id="b3c51-113">This function should be called with administrator credentials.</span></span> <span data-ttu-id="b3c51-114">Ao ser executado sob o controle de conta de usuário (LUA), o processo deve ser elevado.</span><span class="sxs-lookup"><span data-stu-id="b3c51-114">When running under User Account Control (LUA), the process should be elevated.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c51-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c51-115">Requirements</span></span>



| <span data-ttu-id="b3c51-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c51-116">Requirement</span></span> | <span data-ttu-id="b3c51-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b3c51-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c51-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c51-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c51-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3c51-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b3c51-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3c51-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c51-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3c51-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b3c51-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3c51-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c51-123"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c51-123"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="b3c51-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3c51-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3c51-125"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3c51-125"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c51-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3c51-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c51-127">**InstallWiaDevice**</span><span class="sxs-lookup"><span data-stu-id="b3c51-127">**InstallWiaDevice**</span></span>](-wia-installwiadevice.md)
</dt> </dl>

 

 




