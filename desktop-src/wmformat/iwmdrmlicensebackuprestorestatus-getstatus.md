---
title: Método GetStatus IWMDRMLicenseBackupRestoreStatus (wmdrmsdk. h)
description: O método GetStatus recupera informações detalhadas de status sobre uma operação de backup ou restauração de licença.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- Método GetStatus Windows Media Format
- Método GetStatus Windows Media Format, interface IWMDRMLicenseBackupRestoreStatus
- Formato de mídia do Windows da interface IWMDRMLicenseBackupRestoreStatus, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789307"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="2540f-106">Método IWMDRMLicenseBackupRestoreStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="2540f-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="2540f-107">O método **GetStatus** recupera informações detalhadas de status sobre uma operação de backup ou restauração de licença.</span><span class="sxs-lookup"><span data-stu-id="2540f-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2540f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2540f-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="2540f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2540f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2540f-110">*pStatus* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2540f-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2540f-111">Ponteiro para uma estrutura de status de restauração de backup do WM que recebe as informações de status. [**\_ \_ \_**](wm-backup-restore-status.md)</span><span class="sxs-lookup"><span data-stu-id="2540f-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2540f-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2540f-112">Return value</span></span>

<span data-ttu-id="2540f-113">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2540f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2540f-114">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2540f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2540f-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2540f-115">Return code</span></span>                                                                          | <span data-ttu-id="2540f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2540f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2540f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2540f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2540f-118">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2540f-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2540f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2540f-119">Remarks</span></span>

<span data-ttu-id="2540f-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2540f-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="2540f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2540f-121">Requirements</span></span>



| <span data-ttu-id="2540f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2540f-122">Requirement</span></span> | <span data-ttu-id="2540f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2540f-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2540f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2540f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2540f-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2540f-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="2540f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2540f-126">Library</span></span><br/> | <dl> <span data-ttu-id="2540f-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2540f-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2540f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2540f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2540f-129">**Interface IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="2540f-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





