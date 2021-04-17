---
title: Estrutura de WM_BACKUP_RESTORE_STATUS (wmdrmsdk. h)
description: A estrutura de status de restauração de backup do WM \_ \_ \_ contém informações sobre uma operação de backup ou restauração de licença pendente.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- Formato de mídia do Windows de estrutura de WM_BACKUP_RESTORE_STATUS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811639"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="b2ca0-105">\_Estrutura de \_ status de restauração de backup do WM \_</span><span class="sxs-lookup"><span data-stu-id="b2ca0-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="b2ca0-106">A estrutura de status de restauração de backup do WM contém informações sobre uma operação de backup ou restauração de licença pendente. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2ca0-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ca0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2ca0-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="b2ca0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b2ca0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b2ca0-109">**eStatus**</span><span class="sxs-lookup"><span data-stu-id="b2ca0-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="b2ca0-110">Membro da enumeração [**de \_ status Msdrm**](msdrm-status.md) especificando o status.</span><span class="sxs-lookup"><span data-stu-id="b2ca0-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="b2ca0-111">**bstrError**</span><span class="sxs-lookup"><span data-stu-id="b2ca0-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="b2ca0-112">Cadeia de caracteres que contém o erro.</span><span class="sxs-lookup"><span data-stu-id="b2ca0-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2ca0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2ca0-113">Remarks</span></span>

<span data-ttu-id="b2ca0-114">Essa estrutura é recebida quando você chama o método [**IWMDRMLicenseBackupRestoreStatus:: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="b2ca0-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="b2ca0-115">Ele contém o status da operação pendente de backup ou restauração no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="b2ca0-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2ca0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2ca0-116">Requirements</span></span>



| <span data-ttu-id="b2ca0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2ca0-117">Requirement</span></span> | <span data-ttu-id="b2ca0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b2ca0-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2ca0-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2ca0-119">Header</span></span><br/> | <dl> <span data-ttu-id="b2ca0-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2ca0-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2ca0-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2ca0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2ca0-122">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="b2ca0-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





