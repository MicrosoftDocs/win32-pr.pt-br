---
description: Notifica um AppBar que o usuário selecionou o comando Cascade, Tile horizontalmente ou Tile verticalmente no lado do menu de atalho da barra de tarefas.
title: Mensagem de ABN_WINDOWARRANGE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501445"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="58062-103">\_Mensagem WINDOWARRANGE do ABN</span><span class="sxs-lookup"><span data-stu-id="58062-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="58062-104">Notifica um AppBar que o usuário selecionou o comando Cascade, Tile horizontalmente ou Tile verticalmente no lado do menu de atalho da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="58062-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="58062-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58062-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58062-106">*fBeginning*</span><span class="sxs-lookup"><span data-stu-id="58062-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="58062-107">Um sinalizador que especifica se a operação em cascata ou de bloco está começando.</span><span class="sxs-lookup"><span data-stu-id="58062-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="58062-108">Esse parâmetro será **true** se a operação estiver começando e as janelas ainda não tiverem sido movidas.</span><span class="sxs-lookup"><span data-stu-id="58062-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="58062-109">Será **false** se a operação tiver sido concluída.</span><span class="sxs-lookup"><span data-stu-id="58062-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58062-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="58062-110">Return value</span></span>

<span data-ttu-id="58062-111">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="58062-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="58062-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="58062-112">Remarks</span></span>

<span data-ttu-id="58062-113">O sistema envia essa mensagem de notificação duas vezes primeiro com *lParam* definido como **true** e, em seguida, com *lParam* definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="58062-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="58062-114">A primeira notificação é enviada antes que as janelas sejam colocadas em cascata ou em blocos postais, e a segunda é enviada depois que a operação em cascata ou bloco ocorreu.</span><span class="sxs-lookup"><span data-stu-id="58062-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="58062-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58062-115">Requirements</span></span>



| <span data-ttu-id="58062-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="58062-116">Requirement</span></span> | <span data-ttu-id="58062-117">Valor</span><span class="sxs-lookup"><span data-stu-id="58062-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58062-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58062-118">Minimum supported client</span></span><br/> | <span data-ttu-id="58062-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="58062-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="58062-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="58062-120">Minimum supported server</span></span><br/> | <span data-ttu-id="58062-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="58062-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58062-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="58062-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="58062-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="58062-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




