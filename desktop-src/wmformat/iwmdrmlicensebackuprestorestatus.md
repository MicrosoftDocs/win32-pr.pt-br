---
title: Interface IWMDRMLicenseBackupRestoreStatus
description: A interface IWMDRMLicenseBackupRestoreStatus fornece um método para recuperar informações detalhadas de status sobre uma operação de backup ou restauração de licença. Essa interface é entregue com eventos de progresso gerados durante as operações de backup e restauração de licença.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Formato de mídia do Windows da interface IWMDRMLicenseBackupRestoreStatus
- Formato de mídia do Windows da interface IWMDRMLicenseBackupRestoreStatus, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294346"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="1bfb0-105">Interface IWMDRMLicenseBackupRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="1bfb0-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="1bfb0-106">A interface **IWMDRMLicenseBackupRestoreStatus** fornece um método para recuperar informações detalhadas de status sobre uma operação de backup ou restauração de licença.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="1bfb0-107">Essa interface é entregue com eventos de progresso gerados durante as operações de backup e restauração de licença.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="1bfb0-108">Vários eventos **MEWMDRMLicenseBackupProgress** são gerados durante o backup de licença, cada um deles com uma instância de acompanhamento dessa interface.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="1bfb0-109">O mesmo é verdadeiro para eventos **MEWMDRMLicenseRestoreProgress** , que são gerados durante a restauração da licença.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="1bfb0-110">Para recuperar um ponteiro para uma instância da interface **IWMDRMLicenseBackupRestoreStatus** , você deve primeiro chamar o método **IMFMediaEvent:: GetValue** do evento Progress.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="1bfb0-111">O valor que você recupera do evento é um ponteiro para a interface **IUnknown** do objeto que implementa a interface **IWMDRMLicenseBackupRestoreStatus** .</span><span class="sxs-lookup"><span data-stu-id="1bfb0-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="1bfb0-112">Membros</span><span class="sxs-lookup"><span data-stu-id="1bfb0-112">Members</span></span>

<span data-ttu-id="1bfb0-113">A interface **IWMDRMLicenseBackupRestoreStatus** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1bfb0-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1bfb0-114">**IWMDRMLicenseBackupRestoreStatus** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1bfb0-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="1bfb0-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="1bfb0-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1bfb0-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="1bfb0-116">Methods</span></span>

<span data-ttu-id="1bfb0-117">A interface **IWMDRMLicenseBackupRestoreStatus** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="1bfb0-118">Método</span><span class="sxs-lookup"><span data-stu-id="1bfb0-118">Method</span></span>                                                          | <span data-ttu-id="1bfb0-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="1bfb0-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bfb0-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="1bfb0-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="1bfb0-121">Recupera informações detalhadas de status sobre uma operação de backup ou restauração de licença.</span><span class="sxs-lookup"><span data-stu-id="1bfb0-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="1bfb0-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bfb0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfb0-123">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="1bfb0-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

