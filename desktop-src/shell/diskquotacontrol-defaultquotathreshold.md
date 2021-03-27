---
description: Define ou Obtém o limite de cota padrão.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Propriedade DiskQuotaControl. DefaultQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967311"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="80c0e-103">Propriedade DiskQuotaControl. DefaultQuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="80c0e-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="80c0e-104">Define ou Obtém o limite de cota padrão.</span><span class="sxs-lookup"><span data-stu-id="80c0e-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="80c0e-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="80c0e-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c0e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="80c0e-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="80c0e-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="80c0e-107">Property value</span></span>

<span data-ttu-id="80c0e-108">Um valor **inteiro** que é definido como o limite de aviso padrão para novos usuários, em bytes.</span><span class="sxs-lookup"><span data-stu-id="80c0e-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="80c0e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="80c0e-109">Remarks</span></span>

<span data-ttu-id="80c0e-110">O limite de cota padrão é aplicado automaticamente a novos usuários do volume.</span><span class="sxs-lookup"><span data-stu-id="80c0e-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="80c0e-111">Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **true**, o sistema gerará uma entrada de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="80c0e-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="80c0e-112">Por exemplo, se o limite padrão for 10,0 MB, o valor da propriedade será "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="80c0e-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="80c0e-113">Se o volume não tiver um limite padrão, a propriedade será definida como "sem limite" ou o equivalente localizado.</span><span class="sxs-lookup"><span data-stu-id="80c0e-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c0e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80c0e-114">Requirements</span></span>



| <span data-ttu-id="80c0e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="80c0e-115">Requirement</span></span> | <span data-ttu-id="80c0e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="80c0e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c0e-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c0e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80c0e-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="80c0e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="80c0e-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80c0e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80c0e-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="80c0e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="80c0e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="80c0e-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80c0e-122"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="80c0e-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c0e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="80c0e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c0e-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="80c0e-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




