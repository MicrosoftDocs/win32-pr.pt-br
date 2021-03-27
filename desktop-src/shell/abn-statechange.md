---
description: Notifica um AppBar que o estado de ocultar automaticamente ou sempre visível da barra de tarefas foi alterado&\# 8212; ou seja, o usuário selecionou ou limpou o &\# 0034; Sempre no início&\# 0034; ou &\# 0034; Caixa de seleção Ocultar automaticamente&\# 0034; na folha de propriedades da barra de tarefas.
title: Mensagem de ABN_STATECHANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ac2c00a2-ac20-40a5-947e-6b75a2620a0b
api_name:
- ABN_STATECHANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 33879fcb5e9435e2245bc3d00a9fab75bf1cbdc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826897"
---
# <a name="abn_statechange-message"></a><span data-ttu-id="4be64-103">\_Mensagem STATECHANGE do ABN</span><span class="sxs-lookup"><span data-stu-id="4be64-103">ABN\_STATECHANGE message</span></span>

<span data-ttu-id="4be64-104">Notifica um AppBar que o estado de ocultar automaticamente ou sempre visível da barra de tarefas foi alterado ou seja, o usuário selecionou ou desmarcou a caixa de seleção "sempre visível" ou "ocultar automaticamente" na folha de propriedades da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="4be64-104">Notifies an appbar that the taskbar's autohide or always-on-top state has changed that is, the user has selected or cleared the "Always on top" or "Auto hide" check box on the taskbar's property sheet.</span></span>


```C++
ABN_STATECHANGE 
```



## <a name="parameters"></a><span data-ttu-id="4be64-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4be64-105">Parameters</span></span>

<span data-ttu-id="4be64-106">Esta mensagem não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4be64-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4be64-107">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4be64-107">Return value</span></span>

<span data-ttu-id="4be64-108">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="4be64-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4be64-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4be64-109">Remarks</span></span>

<span data-ttu-id="4be64-110">Um AppBar pode usar essa mensagem de notificação para definir seu estado de acordo com a barra de tarefas, se desejado.</span><span class="sxs-lookup"><span data-stu-id="4be64-110">An appbar can use this notification message to set its state to conform to that of the taskbar, if desired.</span></span>

## <a name="requirements"></a><span data-ttu-id="4be64-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4be64-111">Requirements</span></span>



| <span data-ttu-id="4be64-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4be64-112">Requirement</span></span> | <span data-ttu-id="4be64-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4be64-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4be64-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4be64-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4be64-115">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4be64-115">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4be64-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4be64-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4be64-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4be64-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4be64-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4be64-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4be64-119"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4be64-119"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




