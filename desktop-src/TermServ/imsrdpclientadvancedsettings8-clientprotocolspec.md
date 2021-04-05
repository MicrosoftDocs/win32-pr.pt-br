---
title: Propriedade IMsRdpClientAdvancedSettings8 ClientProtocolSpec
description: Especifica o protocolo de área de trabalho remota usado entre o cliente e o servidor.
ms.assetid: DD607D54-CAEA-43EE-94EB-F983AEA0CC1E
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade ClientProtocolSpec
- Propriedade ClientProtocolSpec Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade ClientProtocolSpec
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings8.ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.get_ClientProtocolSpec
- IMsRdpClientAdvancedSettings8.put_ClientProtocolSpec
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41e603f7587435b3701ec0511587286e1a38bcc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918134"
---
# <a name="imsrdpclientadvancedsettings8clientprotocolspec-property"></a><span data-ttu-id="103ca-106">Propriedade IMsRdpClientAdvancedSettings8:: ClientProtocolSpec</span><span class="sxs-lookup"><span data-stu-id="103ca-106">IMsRdpClientAdvancedSettings8::ClientProtocolSpec property</span></span>

<span data-ttu-id="103ca-107">Especifica o protocolo de área de trabalho remota usado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="103ca-107">Specifies the remote desktop protocol used between the client and the server.</span></span>

<span data-ttu-id="103ca-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="103ca-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="103ca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="103ca-109">Syntax</span></span>


```C++
HRESULT put_ClientProtocolSpec(
  [in]  ClientSpec ClientMode
);

HRESULT get_ClientProtocolSpec(
  [out] ClientSpec *pClientMode
);
```



## <a name="property-value"></a><span data-ttu-id="103ca-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="103ca-110">Property value</span></span>

<span data-ttu-id="103ca-111">Um valor da enumeração [**ClientSpec**](clientspec.md) que especifica o protocolo de área de trabalho remota usado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="103ca-111">A value of the [**ClientSpec**](clientspec.md) enumeration that specifies the remote desktop protocol used between the client and the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="103ca-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="103ca-112">Requirements</span></span>



| <span data-ttu-id="103ca-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="103ca-113">Requirement</span></span> | <span data-ttu-id="103ca-114">Valor</span><span class="sxs-lookup"><span data-stu-id="103ca-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="103ca-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103ca-115">Minimum supported client</span></span><br/> | <span data-ttu-id="103ca-116">Windows 8</span><span class="sxs-lookup"><span data-stu-id="103ca-116">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="103ca-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="103ca-117">Minimum supported server</span></span><br/> | <span data-ttu-id="103ca-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="103ca-118">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="103ca-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="103ca-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="103ca-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="103ca-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="103ca-121">DLL</span><span class="sxs-lookup"><span data-stu-id="103ca-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="103ca-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="103ca-122"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="103ca-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="103ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="103ca-124">**ClientSpec**</span><span class="sxs-lookup"><span data-stu-id="103ca-124">**ClientSpec**</span></span>](clientspec.md)
</dt> <dt>

[<span data-ttu-id="103ca-125">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="103ca-125">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> </dl>

 

 





