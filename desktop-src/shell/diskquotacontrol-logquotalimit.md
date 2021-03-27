---
description: Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Propriedade DiskQuotaControl. LogQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967305"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="4690b-103">Propriedade DiskQuotaControl. LogQuotaLimit</span><span class="sxs-lookup"><span data-stu-id="4690b-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="4690b-104">Define ou Obtém um valor booliano que indica se uma entrada do log de eventos do sistema será feita quando um usuário exceder seu limite de cota atribuído.</span><span class="sxs-lookup"><span data-stu-id="4690b-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="4690b-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4690b-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4690b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4690b-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="4690b-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4690b-107">Property value</span></span>

<span data-ttu-id="4690b-108">Essa propriedade será definida como **true** se uma entrada do log de eventos do sistema for feita quando o usuário exceder seu limite de cota ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="4690b-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="4690b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4690b-109">Requirements</span></span>



| <span data-ttu-id="4690b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="4690b-110">Requirement</span></span> | <span data-ttu-id="4690b-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4690b-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4690b-112">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4690b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4690b-113">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4690b-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4690b-114">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4690b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4690b-115">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4690b-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4690b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4690b-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4690b-117"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4690b-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4690b-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4690b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4690b-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="4690b-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4690b-120">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="4690b-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="4690b-121">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="4690b-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




