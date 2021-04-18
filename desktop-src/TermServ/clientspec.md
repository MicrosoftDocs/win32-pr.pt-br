---
title: Enumeração ClientSpec
description: Usado com a propriedade ClientProtocolSpec para especificar o protocolo de área de trabalho remota usado entre o cliente e o servidor.
ms.assetid: BFB2CD3C-04BF-4CB3-B156-8B08AE697327
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração ClientSpec
topic_type:
- apiref
api_name:
- ClientSpec
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f52fbdbaa37c392de727dd2640580800d813d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781026"
---
# <a name="clientspec-enumeration"></a><span data-ttu-id="8cb0d-104">Enumeração ClientSpec</span><span class="sxs-lookup"><span data-stu-id="8cb0d-104">ClientSpec enumeration</span></span>

<span data-ttu-id="8cb0d-105">Usado com a propriedade [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) para especificar o protocolo de área de trabalho remota usado entre o cliente e o servidor.</span><span class="sxs-lookup"><span data-stu-id="8cb0d-105">Used with the [**ClientProtocolSpec**](imsrdpclientadvancedsettings8-clientprotocolspec.md) property to specify the remote desktop protocol used between the client and the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cb0d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cb0d-106">Syntax</span></span>


```C++
typedef enum  { 
  FullMode        = 0,
  ThinClientMode,
  SmallCacheMode
} ClientSpec;
```



## <a name="constants"></a><span data-ttu-id="8cb0d-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="8cb0d-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8cb0d-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**Fullmode**</span><span class="sxs-lookup"><span data-stu-id="8cb0d-108"><span id="FullMode"></span><span id="fullmode"></span><span id="FULLMODE"></span>**FullMode**</span></span>
</dt> <dd>

<span data-ttu-id="8cb0d-109">O protocolo é um protocolo Windows 8 Área de Trabalho Remota completo.</span><span class="sxs-lookup"><span data-stu-id="8cb0d-109">The protocol is full Windows 8 Remote Desktop protocol.</span></span>

</dd> <dt>

<span data-ttu-id="8cb0d-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span><span class="sxs-lookup"><span data-stu-id="8cb0d-110"><span id="ThinClientMode"></span><span id="thinclientmode"></span><span id="THINCLIENTMODE"></span>**ThinClientMode**</span></span>
</dt> <dd>

<span data-ttu-id="8cb0d-111">O protocolo é limitado ao uso do codec RemoteFX do Windows 7 com SP1 e um cache menor.</span><span class="sxs-lookup"><span data-stu-id="8cb0d-111">The protocol is limited to using the Windows 7 with SP1 RemoteFX codec and a smaller cache.</span></span> <span data-ttu-id="8cb0d-112">Todos os outros codecs estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="8cb0d-112">All other codecs are disabled.</span></span> <span data-ttu-id="8cb0d-113">Esse protocolo tem o menor volume de memória.</span><span class="sxs-lookup"><span data-stu-id="8cb0d-113">This protocol has the smallest memory footprint.</span></span>

</dd> <dt>

<span data-ttu-id="8cb0d-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span><span class="sxs-lookup"><span data-stu-id="8cb0d-114"><span id="SmallCacheMode"></span><span id="smallcachemode"></span><span id="SMALLCACHEMODE"></span>**SmallCacheMode**</span></span>
</dt> <dd>

<span data-ttu-id="8cb0d-115">O protocolo é o mesmo que **fullmode**, exceto pelo fato de ele usar um cache menor.</span><span class="sxs-lookup"><span data-stu-id="8cb0d-115">The protocol is the same as **FullMode**, except it uses a smaller cache.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8cb0d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cb0d-116">Requirements</span></span>



| <span data-ttu-id="8cb0d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cb0d-117">Requirement</span></span> | <span data-ttu-id="8cb0d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8cb0d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cb0d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8cb0d-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8cb0d-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="8cb0d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8cb0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8cb0d-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8cb0d-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="8cb0d-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8cb0d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="8cb0d-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cb0d-124"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cb0d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cb0d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cb0d-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span><span class="sxs-lookup"><span data-stu-id="8cb0d-126">**IMsRdpClientAdvancedSettings8::ClientProtocolSpec**</span></span>](imsrdpclientadvancedsettings8-clientprotocolspec.md)
</dt> </dl>

 

 





