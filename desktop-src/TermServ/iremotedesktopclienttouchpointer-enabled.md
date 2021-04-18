---
title: Propriedade habilitada para IRemoteDesktopClientTouchPointer
description: Se o recurso de ponteiro de toque está habilitado no controle de cliente do contêiner de aplicativo RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Propriedade habilitada Serviços de Área de Trabalho Remota
- Propriedade Enabled Serviços de Área de Trabalho Remota, interface IRemoteDesktopClientTouchPointer
- Serviços de Área de Trabalho Remota de interface IRemoteDesktopClientTouchPointer, Propriedade Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760310"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a><span data-ttu-id="92a6a-106">Propriedade IRemoteDesktopClientTouchPointer:: Enabled</span><span class="sxs-lookup"><span data-stu-id="92a6a-106">IRemoteDesktopClientTouchPointer::Enabled property</span></span>

<span data-ttu-id="92a6a-107">Se o recurso de ponteiro de toque está habilitado no controle de cliente do contêiner de aplicativo RDP.</span><span class="sxs-lookup"><span data-stu-id="92a6a-107">Whether the touch pointer feature is enabled on the RDP app container client control.</span></span>

<span data-ttu-id="92a6a-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="92a6a-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a6a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a6a-109">Syntax</span></span>


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a><span data-ttu-id="92a6a-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="92a6a-110">Property value</span></span>

<span data-ttu-id="92a6a-111">**true** se o recurso de ponteiro de toque estiver habilitado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="92a6a-111">**true** if the touch pointer feature is enabled; otherwise, **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a6a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92a6a-112">Requirements</span></span>



| <span data-ttu-id="92a6a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="92a6a-113">Requirement</span></span> | <span data-ttu-id="92a6a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="92a6a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a6a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92a6a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="92a6a-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="92a6a-116">Windows 8</span></span><br/>                                                                                |
| <span data-ttu-id="92a6a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92a6a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="92a6a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92a6a-118">Windows Server 2012</span></span><br/>                                                                      |
| <span data-ttu-id="92a6a-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="92a6a-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="92a6a-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a6a-120"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="92a6a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="92a6a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92a6a-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92a6a-122"><dt>MsTscAx.dll</dt></span></span> </dl>              |
| <span data-ttu-id="92a6a-123">IID</span><span class="sxs-lookup"><span data-stu-id="92a6a-123">IID</span></span><br/>                      | <span data-ttu-id="92a6a-124">IID \_ IRemoteDesktopClientTouchPointer é definido como 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span><span class="sxs-lookup"><span data-stu-id="92a6a-124">IID\_IRemoteDesktopClientTouchPointer is defined as 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92a6a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a6a-126">**IRemoteDesktopClientTouchPointer**</span><span class="sxs-lookup"><span data-stu-id="92a6a-126">**IRemoteDesktopClientTouchPointer**</span></span>](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

