---
description: Remove uma fonte de rede ou URL.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Método patch. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752032"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="0328f-103">Método patch. SourceListClearSource</span><span class="sxs-lookup"><span data-stu-id="0328f-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="0328f-104">O método **SourceListClearSource** remove uma fonte de rede ou URL.</span><span class="sxs-lookup"><span data-stu-id="0328f-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="0328f-105">Esse método chama [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="0328f-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="0328f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0328f-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="0328f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0328f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0328f-108">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="0328f-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="0328f-109">Tipo de fonte a ser removida.</span><span class="sxs-lookup"><span data-stu-id="0328f-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="0328f-110">**\_rede MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="0328f-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="0328f-111">**URL do MSISOURCETYPE \_**</span><span class="sxs-lookup"><span data-stu-id="0328f-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="0328f-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="0328f-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0328f-113">Caminho para a origem a ser removida.</span><span class="sxs-lookup"><span data-stu-id="0328f-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0328f-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0328f-114">Return value</span></span>

<span data-ttu-id="0328f-115">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0328f-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0328f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0328f-116">Requirements</span></span>



| <span data-ttu-id="0328f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0328f-117">Requirement</span></span> | <span data-ttu-id="0328f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0328f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0328f-119">Versão</span><span class="sxs-lookup"><span data-stu-id="0328f-119">Version</span></span><br/> | <span data-ttu-id="0328f-120">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0328f-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0328f-121">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0328f-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0328f-122">Windows Installer 3,0 ou posterior no Windows Server 2003, Windows XP e Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0328f-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="0328f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0328f-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0328f-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0328f-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="0328f-125">IID</span><span class="sxs-lookup"><span data-stu-id="0328f-125">IID</span></span><br/>     | <span data-ttu-id="0328f-126">IID \_ IPatch é definido como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0328f-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0328f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0328f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0328f-128">**Patch**</span><span class="sxs-lookup"><span data-stu-id="0328f-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="0328f-129">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="0328f-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="0328f-130">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0328f-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




