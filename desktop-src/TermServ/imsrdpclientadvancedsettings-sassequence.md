---
title: Propriedade IMsRdpClientAdvancedSettings SasSequence
description: Especifica a Secure Access Sequence (SAS) que o cliente usará para acessar a tela de logon no servidor.
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade SasSequence
- Propriedade SasSequence Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade SasSequence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454652"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="52365-106">Propriedade IMsRdpClientAdvancedSettings:: SasSequence</span><span class="sxs-lookup"><span data-stu-id="52365-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="52365-107">Especifica a Secure Access Sequence (SAS) que o cliente usará para acessar a tela de logon no servidor.</span><span class="sxs-lookup"><span data-stu-id="52365-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="52365-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="52365-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52365-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="52365-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="52365-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="52365-110">Property value</span></span>

<span data-ttu-id="52365-111">Um valor **longo** que contém o indicador SAS.</span><span class="sxs-lookup"><span data-stu-id="52365-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="52365-112">O único valor com suporte é 0xaa03, que indica a sequência CTRL + ALT + DELETE padrão.</span><span class="sxs-lookup"><span data-stu-id="52365-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="52365-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="52365-113">Remarks</span></span>

<span data-ttu-id="52365-114">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="52365-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52365-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52365-115">Requirements</span></span>



| <span data-ttu-id="52365-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="52365-116">Requirement</span></span> | <span data-ttu-id="52365-117">Valor</span><span class="sxs-lookup"><span data-stu-id="52365-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52365-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52365-118">Minimum supported client</span></span><br/> | <span data-ttu-id="52365-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52365-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="52365-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52365-120">Minimum supported server</span></span><br/> | <span data-ttu-id="52365-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52365-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="52365-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52365-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="52365-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52365-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="52365-124">DLL</span><span class="sxs-lookup"><span data-stu-id="52365-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52365-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52365-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="52365-126">IID</span><span class="sxs-lookup"><span data-stu-id="52365-126">IID</span></span><br/>                      | <span data-ttu-id="52365-127">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="52365-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="52365-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="52365-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52365-129">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="52365-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





