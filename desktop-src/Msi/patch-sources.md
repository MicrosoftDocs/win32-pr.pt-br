---
description: A propriedade sources enumera todas as fontes para a instância de patch. Essa propriedade chama MsiSourceListEnumSources e retorna uma matriz de cadeias de caracteres e aceita o tipo de origem como argumento.
ms.assetid: 4a052518-4d76-4a95-be9e-7acae36db626
title: Propriedade patch. Sources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.Sources
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18b9e6ab867d68908bc8dd7e7f87f942f8cd015c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752244"
---
# <a name="patchsources-property"></a><span data-ttu-id="45423-104">Propriedade patch. Sources</span><span class="sxs-lookup"><span data-stu-id="45423-104">Patch.Sources property</span></span>

<span data-ttu-id="45423-105">A propriedade **sources** enumera todas as fontes para a instância de patch.</span><span class="sxs-lookup"><span data-stu-id="45423-105">The **Sources** property enumerates all the sources for the patch instance.</span></span> <span data-ttu-id="45423-106">Essa propriedade chama [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) e retorna uma matriz de cadeias de caracteres e aceita o tipo de origem como argumento.</span><span class="sxs-lookup"><span data-stu-id="45423-106">This property calls [**MsiSourceListEnumSources**](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa) and returns an array of strings, and accepts the source type as argument.</span></span>

<span data-ttu-id="45423-107">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="45423-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="45423-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45423-108">Syntax</span></span>


```JScript
propVal = Patch.Sources
```



## <a name="property-value"></a><span data-ttu-id="45423-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="45423-109">Property value</span></span>

<span data-ttu-id="45423-110">O tipo de origem a ser enumerado.</span><span class="sxs-lookup"><span data-stu-id="45423-110">The type of source to enumerate.</span></span> <span data-ttu-id="45423-111">O valor pode ser *msiInstallSourceTypeNetwork* (1) ou *msiInstallSourceTypeURL* (2).</span><span class="sxs-lookup"><span data-stu-id="45423-111">The value can be *msiInstallSourceTypeNetwork* (1) or *msiInstallSourceTypeURL* (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="45423-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45423-112">Requirements</span></span>



| <span data-ttu-id="45423-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="45423-113">Requirement</span></span> | <span data-ttu-id="45423-114">Valor</span><span class="sxs-lookup"><span data-stu-id="45423-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45423-115">Versão</span><span class="sxs-lookup"><span data-stu-id="45423-115">Version</span></span><br/> | <span data-ttu-id="45423-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="45423-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="45423-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="45423-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="45423-118">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="45423-118">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="45423-119">DLL</span><span class="sxs-lookup"><span data-stu-id="45423-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="45423-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45423-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="45423-121">IID</span><span class="sxs-lookup"><span data-stu-id="45423-121">IID</span></span><br/>     | <span data-ttu-id="45423-122">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="45423-122">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="45423-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="45423-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45423-124">**Patch**</span><span class="sxs-lookup"><span data-stu-id="45423-124">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="45423-125">**MsiSourceListEnumSources**</span><span class="sxs-lookup"><span data-stu-id="45423-125">**MsiSourceListEnumSources**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistenumsourcesa)
</dt> <dt>

[<span data-ttu-id="45423-126">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="45423-126">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




