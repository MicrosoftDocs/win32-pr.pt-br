---
description: Obtém o limite de cota padrão como uma cadeia de texto.
title: Propriedade DiskQuotaControl. DefaultQuotaLimitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090017"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="7c021-103">Propriedade DiskQuotaControl. DefaultQuotaLimitText</span><span class="sxs-lookup"><span data-stu-id="7c021-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="7c021-104">Obtém o limite de cota padrão como uma cadeia de texto.</span><span class="sxs-lookup"><span data-stu-id="7c021-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="7c021-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="7c021-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c021-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c021-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="7c021-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7c021-107">Property value</span></span>

<span data-ttu-id="7c021-108">Um valor de cadeia de caracteres que contém o limite de cota padrão para novos usuários do volume.</span><span class="sxs-lookup"><span data-stu-id="7c021-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="7c021-109">Por exemplo, se a cota padrão for de 10,5 MB, o valor da propriedade será "10,5 MB".</span><span class="sxs-lookup"><span data-stu-id="7c021-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="7c021-110">Se o volume não tiver nenhuma cota padrão, a propriedade será definida como "sem limite" ou o equivalente localizado.</span><span class="sxs-lookup"><span data-stu-id="7c021-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c021-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c021-111">Requirements</span></span>



| <span data-ttu-id="7c021-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c021-112">Requirement</span></span> | <span data-ttu-id="7c021-113">Valor</span><span class="sxs-lookup"><span data-stu-id="7c021-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c021-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c021-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7c021-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c021-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c021-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7c021-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7c021-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7c021-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7c021-118">DLL</span><span class="sxs-lookup"><span data-stu-id="7c021-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c021-119"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7c021-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c021-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c021-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c021-121">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="7c021-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="7c021-122">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="7c021-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




