---
title: Propriedade IMsRdpClientNonScriptable5 RemoteMonitorLayoutMatchesLocal
description: Especifica se o layout do monitor remoto é idêntico ao layout do monitor local.
ms.assetid: 8F3C6650-870C-417C-82FC-E145FC360012
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RemoteMonitorLayoutMatchesLocal
- Propriedade RemoteMonitorLayoutMatchesLocal Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, Propriedade RemoteMonitorLayoutMatchesLocal
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.RemoteMonitorLayoutMatchesLocal
- IMsRdpClientNonScriptable5.get_RemoteMonitorLayoutMatchesLocal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5018b22865cc683fc9231c857a1b99b8acbfeca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085869"
---
# <a name="imsrdpclientnonscriptable5remotemonitorlayoutmatcheslocal-property"></a><span data-ttu-id="54837-106">Propriedade IMsRdpClientNonScriptable5:: RemoteMonitorLayoutMatchesLocal</span><span class="sxs-lookup"><span data-stu-id="54837-106">IMsRdpClientNonScriptable5::RemoteMonitorLayoutMatchesLocal property</span></span>

<span data-ttu-id="54837-107">Especifica se o layout do monitor remoto é idêntico ao layout do monitor local.</span><span class="sxs-lookup"><span data-stu-id="54837-107">Specifies if the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="54837-108">Se essa propriedade contiver a **variante \_ true**, o layout do monitor remoto será idêntico ao layout do monitor local.</span><span class="sxs-lookup"><span data-stu-id="54837-108">If this property contains **VARIANT\_TRUE**, the remote monitor layout is identical to the local monitor layout.</span></span> <span data-ttu-id="54837-109">Se essa propriedade contiver a **variante \_ false**, os monitores remoto e local terão layouts diferentes.</span><span class="sxs-lookup"><span data-stu-id="54837-109">If this property contains **VARIANT\_FALSE**, the remote and local monitors have different layouts.</span></span>

<span data-ttu-id="54837-110">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="54837-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54837-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="54837-111">Syntax</span></span>


```C++
HRESULT get_RemoteMonitorLayoutMatchesLocal(
  [out, retval] VARIANT_BOOL *pfRemoteMatchesLocal
);
```



## <a name="property-value"></a><span data-ttu-id="54837-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="54837-112">Property value</span></span>

<span data-ttu-id="54837-113">Recebe o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="54837-113">Receives the property value.</span></span>

## <a name="requirements"></a><span data-ttu-id="54837-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54837-114">Requirements</span></span>



| <span data-ttu-id="54837-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="54837-115">Requirement</span></span> | <span data-ttu-id="54837-116">Valor</span><span class="sxs-lookup"><span data-stu-id="54837-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="54837-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54837-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54837-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54837-118">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="54837-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="54837-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54837-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="54837-120">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="54837-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="54837-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="54837-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54837-122"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="54837-123">DLL</span><span class="sxs-lookup"><span data-stu-id="54837-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54837-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54837-124"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="54837-125">IID</span><span class="sxs-lookup"><span data-stu-id="54837-125">IID</span></span><br/>                      | <span data-ttu-id="54837-126">IID \_ IMsRdpClientNonScriptable5 é definido como 4f6996d5-d7b1-412C-b0ff-063718566907</span><span class="sxs-lookup"><span data-stu-id="54837-126">IID\_IMsRdpClientNonScriptable5 is defined as 4f6996d5-d7b1-412c-b0ff-063718566907</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="54837-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="54837-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54837-128">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="54837-128">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





