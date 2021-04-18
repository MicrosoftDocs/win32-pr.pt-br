---
title: Propriedade IMsRdpClientShell RdpFileContents
description: Especifica ou recupera o conteúdo do arquivo de protocolo RDP (RDP) a ser iniciado a partir de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de algum outro portal da Web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RdpFileContents
- Propriedade RdpFileContents Serviços de Área de Trabalho Remota, interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell, Propriedade RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789436"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a><span data-ttu-id="fafc7-106">Propriedade IMsRdpClientShell:: RdpFileContents</span><span class="sxs-lookup"><span data-stu-id="fafc7-106">IMsRdpClientShell::RdpFileContents property</span></span>

<span data-ttu-id="fafc7-107">Especifica ou recupera o conteúdo do arquivo de protocolo RDP (RDP) a ser iniciado a partir de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de algum outro portal da Web.</span><span class="sxs-lookup"><span data-stu-id="fafc7-107">Specifies or retrieves the Remote Desktop Protocol (RDP) file content to be launched from Remote Desktop Web Access (RD Web Access) or from some other web portal.</span></span>

<span data-ttu-id="fafc7-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="fafc7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafc7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fafc7-109">Syntax</span></span>


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a><span data-ttu-id="fafc7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="fafc7-110">Property value</span></span>

<span data-ttu-id="fafc7-111">Especifica o conteúdo do arquivo RDP a ser iniciado no portal da Web.</span><span class="sxs-lookup"><span data-stu-id="fafc7-111">Specifies the RDP file content to be launched from the web portal.</span></span>

## <a name="requirements"></a><span data-ttu-id="fafc7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fafc7-112">Requirements</span></span>



| <span data-ttu-id="fafc7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="fafc7-113">Requirement</span></span> | <span data-ttu-id="fafc7-114">Valor</span><span class="sxs-lookup"><span data-stu-id="fafc7-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fafc7-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fafc7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="fafc7-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fafc7-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fafc7-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fafc7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="fafc7-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fafc7-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fafc7-119">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fafc7-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="fafc7-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafc7-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fafc7-121">DLL</span><span class="sxs-lookup"><span data-stu-id="fafc7-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafc7-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafc7-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fafc7-123">IID</span><span class="sxs-lookup"><span data-stu-id="fafc7-123">IID</span></span><br/>                      | <span data-ttu-id="fafc7-124">IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="fafc7-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="fafc7-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fafc7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafc7-126">**IMsRdpClientShell**</span><span class="sxs-lookup"><span data-stu-id="fafc7-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





