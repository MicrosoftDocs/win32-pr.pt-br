---
description: O método SourceListForceResolution limpa a última propriedade de origem usada.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Método patch. SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752245"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="d2c5b-103">Método patch. SourceListForceResolution</span><span class="sxs-lookup"><span data-stu-id="d2c5b-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="d2c5b-104">O método **SourceListForceResolution** limpa a última propriedade de origem usada.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="d2c5b-105">Isso forçará o instalador a Pesquisar a lista de origem em busca de uma origem de patch válida na próxima vez em que a origem do patch for necessária.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="d2c5b-106">Por exemplo, o instalador requer a origem do patch para executar uma instalação ou reinstalação quando a cópia do cache local do patch está ausente.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="d2c5b-107">Esse método chama [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="d2c5b-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2c5b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d2c5b-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="d2c5b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2c5b-109">Parameters</span></span>

<span data-ttu-id="d2c5b-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d2c5b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d2c5b-111">Return value</span></span>

<span data-ttu-id="d2c5b-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2c5b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2c5b-113">Requirements</span></span>



| <span data-ttu-id="d2c5b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2c5b-114">Requirement</span></span> | <span data-ttu-id="d2c5b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d2c5b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2c5b-116">Versão</span><span class="sxs-lookup"><span data-stu-id="d2c5b-116">Version</span></span><br/> | <span data-ttu-id="d2c5b-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d2c5b-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d2c5b-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d2c5b-119">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d2c5b-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="d2c5b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d2c5b-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="d2c5b-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2c5b-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="d2c5b-122">IID</span><span class="sxs-lookup"><span data-stu-id="d2c5b-122">IID</span></span><br/>     | <span data-ttu-id="d2c5b-123">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d2c5b-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="d2c5b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d2c5b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2c5b-125">**Patch**</span><span class="sxs-lookup"><span data-stu-id="d2c5b-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="d2c5b-126">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="d2c5b-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="d2c5b-127">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d2c5b-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




