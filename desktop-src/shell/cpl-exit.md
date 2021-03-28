---
description: Enviado uma vez para a função CPlApplet de um aplicativo do painel de controle antes que a DLL que contém o aplicativo do painel de controle seja liberada.
ms.assetid: 1afcb0d3-41a7-4fd8-9561-d96e1e8f0ddb
title: Mensagem de CPL_EXIT (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0adea6c4b05ee752829634f7478df2ac651e69f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164312"
---
# <a name="cpl_exit-message"></a><span data-ttu-id="515e2-103">Mensagem de saída de CPL \_</span><span class="sxs-lookup"><span data-stu-id="515e2-103">CPL\_EXIT message</span></span>

<span data-ttu-id="515e2-104">Enviado uma vez para a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) de um aplicativo do painel de controle antes que a DLL que contém o aplicativo do painel de controle seja liberada.</span><span class="sxs-lookup"><span data-stu-id="515e2-104">Sent once to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application before the DLL containing the Control Panel application is released.</span></span>

## <a name="parameters"></a><span data-ttu-id="515e2-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="515e2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="515e2-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="515e2-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="515e2-107">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="515e2-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="515e2-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="515e2-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="515e2-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="515e2-109">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="515e2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="515e2-110">Return value</span></span>

<span data-ttu-id="515e2-111">Se a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processar essa mensagem com êxito, ela deverá retornar zero.</span><span class="sxs-lookup"><span data-stu-id="515e2-111">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="515e2-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="515e2-112">Remarks</span></span>

<span data-ttu-id="515e2-113">Essa mensagem é enviada depois que a última mensagem de [**\_ parada de CPL**](cpl-stop.md) é enviada.</span><span class="sxs-lookup"><span data-stu-id="515e2-113">This message is sent after the last [**CPL\_STOP**](cpl-stop.md) message is sent.</span></span>

<span data-ttu-id="515e2-114">Em resposta a essa mensagem, um aplicativo do painel de controle deve liberar qualquer memória alocada e executar a limpeza em nível global.</span><span class="sxs-lookup"><span data-stu-id="515e2-114">In response to this message, a Control Panel application must free any memory that it has allocated and perform global-level cleanup.</span></span>

## <a name="requirements"></a><span data-ttu-id="515e2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="515e2-115">Requirements</span></span>



| <span data-ttu-id="515e2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="515e2-116">Requirement</span></span> | <span data-ttu-id="515e2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="515e2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="515e2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="515e2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="515e2-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="515e2-119">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="515e2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="515e2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="515e2-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="515e2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="515e2-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="515e2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="515e2-123"><dt>CPL. h</dt></span><span class="sxs-lookup"><span data-stu-id="515e2-123"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="515e2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="515e2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="515e2-125">**FreeLibrary**</span><span class="sxs-lookup"><span data-stu-id="515e2-125">**FreeLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
