---
description: Obtém o limite de cota padrão como uma cadeia de texto.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Propriedade DiskQuotaControl. DefaultQuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090016"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="b0c60-103">Propriedade DiskQuotaControl. DefaultQuotaThresholdText</span><span class="sxs-lookup"><span data-stu-id="b0c60-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="b0c60-104">Obtém o limite de cota padrão como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="b0c60-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="b0c60-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="b0c60-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0c60-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0c60-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="b0c60-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b0c60-107">Property value</span></span>

<span data-ttu-id="b0c60-108">Um valor de cadeia de caracteres que contém o limite de cota padrão para o volume.</span><span class="sxs-lookup"><span data-stu-id="b0c60-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c60-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0c60-109">Remarks</span></span>

<span data-ttu-id="b0c60-110">O limite de cota padrão é aplicado automaticamente a novos usuários do volume.</span><span class="sxs-lookup"><span data-stu-id="b0c60-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="b0c60-111">Se o uso do disco de um usuário exceder esse valor e a propriedade [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) for definida como **true**, o sistema gerará uma entrada de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="b0c60-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="b0c60-112">Por exemplo, se o limite padrão for 10,0 MB, o valor da propriedade será "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="b0c60-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="b0c60-113">Se o volume não tiver um limite padrão, a propriedade será definida como "sem limite" ou o equivalente localizado.</span><span class="sxs-lookup"><span data-stu-id="b0c60-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c60-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0c60-114">Requirements</span></span>



| <span data-ttu-id="b0c60-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0c60-115">Requirement</span></span> | <span data-ttu-id="b0c60-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b0c60-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c60-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0c60-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c60-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0c60-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0c60-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0c60-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c60-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b0c60-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b0c60-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b0c60-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0c60-122"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="b0c60-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c60-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0c60-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0c60-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="b0c60-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




