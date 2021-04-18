---
title: Propriedade IMsRdpDeviceV2 CmClassGuid
description: Contém o GUID da classe de instalação do Configuration Manager para o dispositivo.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade CmClassGuid
- Propriedade CmClassGuid Serviços de Área de Trabalho Remota, interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2, Propriedade CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757598"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a><span data-ttu-id="230a5-106">Propriedade IMsRdpDeviceV2:: CmClassGuid</span><span class="sxs-lookup"><span data-stu-id="230a5-106">IMsRdpDeviceV2::CmClassGuid property</span></span>

<span data-ttu-id="230a5-107">Contém o GUID da classe de instalação do Configuration Manager para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="230a5-107">Contains the configuration manager setup class GUID for the device.</span></span>

<span data-ttu-id="230a5-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="230a5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="230a5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="230a5-109">Syntax</span></span>


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a><span data-ttu-id="230a5-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="230a5-110">Property value</span></span>

<span data-ttu-id="230a5-111">O GUID da classe de instalação do Configuration Manager para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="230a5-111">The configuration manager setup class GUID for the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="230a5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="230a5-112">Requirements</span></span>



| <span data-ttu-id="230a5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="230a5-113">Requirement</span></span> | <span data-ttu-id="230a5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="230a5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="230a5-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="230a5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="230a5-116">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="230a5-116">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="230a5-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="230a5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="230a5-118">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="230a5-118">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="230a5-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="230a5-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="230a5-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="230a5-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="230a5-121">DLL</span><span class="sxs-lookup"><span data-stu-id="230a5-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="230a5-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="230a5-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="230a5-123">IID</span><span class="sxs-lookup"><span data-stu-id="230a5-123">IID</span></span><br/>                      | <span data-ttu-id="230a5-124">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="230a5-124">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="230a5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="230a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="230a5-126">**IMsRdpDeviceV2**</span><span class="sxs-lookup"><span data-stu-id="230a5-126">**IMsRdpDeviceV2**</span></span>](imsrdpdevicev2.md)
</dt> </dl>

 

 





