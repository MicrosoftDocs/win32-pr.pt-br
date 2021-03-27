---
description: Obtém um valor booliano que indica se o arquivo de cota do volume está sendo recriado no momento.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Propriedade DiskQuotaControl. QuotaFileRebuilding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967388"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="8fef8-103">Propriedade DiskQuotaControl. QuotaFileRebuilding</span><span class="sxs-lookup"><span data-stu-id="8fef8-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="8fef8-104">Obtém um valor booliano que indica se o arquivo de cota do volume está sendo recriado no momento.</span><span class="sxs-lookup"><span data-stu-id="8fef8-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="8fef8-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="8fef8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fef8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fef8-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="8fef8-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8fef8-107">Property value</span></span>

<span data-ttu-id="8fef8-108">Essa propriedade será definida como **true** se o arquivo de cota estiver sendo recompilado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8fef8-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fef8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fef8-109">Remarks</span></span>

<span data-ttu-id="8fef8-110">O arquivo de cota é recriado automaticamente quando as cotas são habilitadas no sistema ou quando uma ou mais entradas de usuário são marcadas para exclusão.</span><span class="sxs-lookup"><span data-stu-id="8fef8-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fef8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fef8-111">Requirements</span></span>



| <span data-ttu-id="8fef8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fef8-112">Requirement</span></span> | <span data-ttu-id="8fef8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="8fef8-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fef8-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fef8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8fef8-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fef8-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8fef8-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fef8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8fef8-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fef8-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8fef8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="8fef8-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fef8-119"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8fef8-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fef8-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fef8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fef8-121">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="8fef8-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




