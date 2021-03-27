---
description: Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Propriedade DiskQuotaControl. LogQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967304"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="4c0cf-103">Propriedade DiskQuotaControl. LogQuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="4c0cf-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="4c0cf-104">Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="4c0cf-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c0cf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c0cf-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="4c0cf-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4c0cf-107">Property value</span></span>

<span data-ttu-id="4c0cf-108">Essa propriedade será definida como **true** se uma entrada do log de eventos do sistema for feita quando o usuário exceder seu limite de aviso de cota ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c0cf-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c0cf-109">Requirements</span></span>



| <span data-ttu-id="4c0cf-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c0cf-110">Requirement</span></span> | <span data-ttu-id="4c0cf-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4c0cf-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c0cf-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c0cf-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4c0cf-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c0cf-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4c0cf-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c0cf-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4c0cf-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4c0cf-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4c0cf-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4c0cf-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c0cf-117"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4c0cf-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c0cf-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c0cf-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c0cf-119">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="4c0cf-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="4c0cf-120">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="4c0cf-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="4c0cf-121">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="4c0cf-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




