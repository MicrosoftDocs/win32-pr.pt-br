---
title: Propriedade TransportType IMsRdpClientAdvancedSettings
description: Especifica o tipo de transporte usado pelo cliente.
ms.assetid: 752f5fbc-eb5a-48eb-8750-fc25c8a2f024
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TransportType
- Propriedade TransportType Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade TransportType
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.TransportType
- IMsRdpClientAdvancedSettings.get_TransportType
- IMsRdpClientAdvancedSettings.put_TransportType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0664e0c792725dc112baf786d63c5175eb450dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758386"
---
# <a name="imsrdpclientadvancedsettingstransporttype-property"></a><span data-ttu-id="3cd31-106">Propriedade IMsRdpClientAdvancedSettings:: TransportType</span><span class="sxs-lookup"><span data-stu-id="3cd31-106">IMsRdpClientAdvancedSettings::TransportType property</span></span>

<span data-ttu-id="3cd31-107">Especifica o tipo de transporte usado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="3cd31-107">Specifies the transport type used by the client.</span></span> <span data-ttu-id="3cd31-108">Essa propriedade não é usada pelo controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="3cd31-108">This property is not used by the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="3cd31-109">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3cd31-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd31-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cd31-110">Syntax</span></span>


```C++
HRESULT put_TransportType(
  [in]  LONG transportType
);

HRESULT get_TransportType(
  [out] LONG *ptransportType
);
```



## <a name="property-value"></a><span data-ttu-id="3cd31-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="3cd31-111">Property value</span></span>

<span data-ttu-id="3cd31-112">Define o tipo de transporte.</span><span class="sxs-lookup"><span data-stu-id="3cd31-112">Sets the transport type.</span></span> <span data-ttu-id="3cd31-113">Esse método pode ter sucesso, mas o conjunto de valores nunca é usado pelo controle ActiveX Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="3cd31-113">This method may succeed, but the value set is never used by the Remote Desktop ActiveX control.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd31-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3cd31-114">Remarks</span></span>

<span data-ttu-id="3cd31-115">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3cd31-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd31-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cd31-116">Requirements</span></span>



| <span data-ttu-id="3cd31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cd31-117">Requirement</span></span> | <span data-ttu-id="3cd31-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3cd31-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd31-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cd31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3cd31-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cd31-120">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="3cd31-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3cd31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3cd31-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cd31-122">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="3cd31-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3cd31-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="3cd31-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cd31-124"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3cd31-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3cd31-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cd31-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cd31-126"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3cd31-127">IID</span><span class="sxs-lookup"><span data-stu-id="3cd31-127">IID</span></span><br/>                      | <span data-ttu-id="3cd31-128">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="3cd31-128">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cd31-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3cd31-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cd31-130">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="3cd31-130">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





