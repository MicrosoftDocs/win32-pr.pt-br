---
title: Propriedade IMsRdpClientNonScriptable5 DisableRemoteAppCapsCheck
description: Especifica se o controle ActiveX Área de Trabalho Remota não deve verificar os recursos de RemoteApp do servidor.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade DisableRemoteAppCapsCheck
- Propriedade DisableRemoteAppCapsCheck Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade DisableRemoteAppCapsCheck
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104456003"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a><span data-ttu-id="b96ec-106">IMsRdpClientNonScriptable5: Propriedade isableRemoteAppCapsCheck de:D</span><span class="sxs-lookup"><span data-stu-id="b96ec-106">IMsRdpClientNonScriptable5::DisableRemoteAppCapsCheck property</span></span>

<span data-ttu-id="b96ec-107">Especifica se o controle ActiveX Área de Trabalho Remota não deve verificar os recursos de RemoteApp do servidor.</span><span class="sxs-lookup"><span data-stu-id="b96ec-107">Specifies whether the Remote Desktop ActiveX control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="b96ec-108">Se essa propriedade contiver a **variante \_ true**, o controle não deverá verificar o servidor em busca de recursos do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b96ec-108">If this property contains **VARIANT\_TRUE**, the control should not check the server for RemoteApp capabilities.</span></span> <span data-ttu-id="b96ec-109">Se essa propriedade contiver a **variante \_ false**, o controle poderá verificar o servidor em busca de recursos do RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b96ec-109">If this property contains **VARIANT\_FALSE**, the control can check the server for RemoteApp capabilities.</span></span>

<span data-ttu-id="b96ec-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b96ec-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b96ec-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="b96ec-111">Syntax</span></span>


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a><span data-ttu-id="b96ec-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="b96ec-112">Property value</span></span>

<span data-ttu-id="b96ec-113">Especifica o novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="b96ec-113">Specifies the new property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b96ec-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b96ec-114">Requirements</span></span>



| <span data-ttu-id="b96ec-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b96ec-115">Requirement</span></span> | <span data-ttu-id="b96ec-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b96ec-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b96ec-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b96ec-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b96ec-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b96ec-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b96ec-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b96ec-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b96ec-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b96ec-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="b96ec-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b96ec-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b96ec-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b96ec-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="b96ec-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b96ec-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b96ec-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b96ec-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="b96ec-125">IID</span><span class="sxs-lookup"><span data-stu-id="b96ec-125">IID</span></span><br/>                      | <span data-ttu-id="b96ec-126">IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="b96ec-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b96ec-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b96ec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b96ec-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b96ec-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





