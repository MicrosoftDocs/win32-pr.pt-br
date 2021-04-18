---
description: O método ExtractPatchXMLData do objeto do instalador extrai informações de um patch como uma cadeia de caracteres XML. As informações podem ser usadas para determinar se o patch se aplica a um sistema de destino. Esse método chama MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Método Installer. ExtractPatchXMLData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752642"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="408a9-105">Método Installer. ExtractPatchXMLData</span><span class="sxs-lookup"><span data-stu-id="408a9-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="408a9-106">O método **ExtractPatchXMLData** do objeto do [**instalador**](installer-object.md) extrai informações de um patch como uma cadeia de caracteres XML.</span><span class="sxs-lookup"><span data-stu-id="408a9-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="408a9-107">As informações podem ser usadas para determinar se o patch se aplica a um sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="408a9-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="408a9-108">Esse método chama [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="408a9-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="408a9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="408a9-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="408a9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="408a9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408a9-111">*PatchPath*</span><span class="sxs-lookup"><span data-stu-id="408a9-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="408a9-112">Caminho completo do patch do qual as informações de aplicabilidade serão extraídas.</span><span class="sxs-lookup"><span data-stu-id="408a9-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408a9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="408a9-113">Return value</span></span>

<span data-ttu-id="408a9-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="408a9-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="408a9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="408a9-115">Requirements</span></span>



| <span data-ttu-id="408a9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="408a9-116">Requirement</span></span> | <span data-ttu-id="408a9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="408a9-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="408a9-118">Versão</span><span class="sxs-lookup"><span data-stu-id="408a9-118">Version</span></span><br/> | <span data-ttu-id="408a9-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="408a9-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="408a9-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="408a9-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="408a9-121">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="408a9-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="408a9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="408a9-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="408a9-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408a9-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="408a9-124">IID</span><span class="sxs-lookup"><span data-stu-id="408a9-124">IID</span></span><br/>     | <span data-ttu-id="408a9-125">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="408a9-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="408a9-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="408a9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408a9-127">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="408a9-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="408a9-128">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="408a9-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




