---
title: Interface INapSoHProcessor (NapProtocol. h)
description: São usados por SHAs para processar o conteúdo de SoHResponses e por SHVs para processar o conteúdo de SoHRequests.
ms.assetid: c2dd71ca-a4dd-44d2-81ab-b83e90599a2f
keywords:
- INapSoHProcessor da interface NAP
- INapSoHProcessor interface NAP, descrita
topic_type:
- apiref
api_name:
- INapSoHProcessor
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c43abf137bb267468deeb9d4bd47546275ba6c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008892"
---
# <a name="inapsohprocessor-interface"></a><span data-ttu-id="bd47b-105">Interface INapSoHProcessor</span><span class="sxs-lookup"><span data-stu-id="bd47b-105">INapSoHProcessor interface</span></span>

> [!Note]  
> <span data-ttu-id="bd47b-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="bd47b-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bd47b-107">O **INapSoHProcessor** fornece métodos que são usados por SHAs para processar o conteúdo de [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) e por SHVs para processar o conteúdo de **SoHRequests**.</span><span class="sxs-lookup"><span data-stu-id="bd47b-107">The **INapSoHProcessor** provides methods that are used by SHAs to process the contents of [**SoHResponses**](/windows/win32/api/naptypes/ns-naptypes-soh) and by SHVs to process the contents of **SoHRequests**.</span></span>

## <a name="members"></a><span data-ttu-id="bd47b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="bd47b-108">Members</span></span>

<span data-ttu-id="bd47b-109">A interface **INapSoHProcessor** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bd47b-109">The **INapSoHProcessor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd47b-110">**INapSoHProcessor** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bd47b-110">**INapSoHProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="bd47b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd47b-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd47b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="bd47b-112">Methods</span></span>

<span data-ttu-id="bd47b-113">A interface **INapSoHProcessor** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="bd47b-113">The **INapSoHProcessor** interface has these methods.</span></span>



| <span data-ttu-id="bd47b-114">Método</span><span class="sxs-lookup"><span data-stu-id="bd47b-114">Method</span></span>                                                                                           | <span data-ttu-id="bd47b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="bd47b-115">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd47b-116">**INapSoHProcessor::FindNextAttribute**</span><span class="sxs-lookup"><span data-stu-id="bd47b-116">**INapSoHProcessor::FindNextAttribute**</span></span>](inapsohprocessor-findnextattribute-method.md)         | <span data-ttu-id="bd47b-117">Localiza o índice de localização do próximo atributo de pacote SoH.</span><span class="sxs-lookup"><span data-stu-id="bd47b-117">Finds the location index of the next SoH packet attribute.</span></span><br/>                 |
| [<span data-ttu-id="bd47b-118">**INapSoHProcessor:: GetAttribute**</span><span class="sxs-lookup"><span data-stu-id="bd47b-118">**INapSoHProcessor::GetAttribute**</span></span>](inapsohprocessor-getattribute-method.md)                   | <span data-ttu-id="bd47b-119">Recupera o tipo de atributo e o valor.</span><span class="sxs-lookup"><span data-stu-id="bd47b-119">Retrieves the attribute type and value.</span></span><br/>                                    |
| [<span data-ttu-id="bd47b-120">**INapSoHProcessor::GetNumberOfAttributes**</span><span class="sxs-lookup"><span data-stu-id="bd47b-120">**INapSoHProcessor::GetNumberOfAttributes**</span></span>](inapsohprocessor-getnumberofattributes-method.md) | <span data-ttu-id="bd47b-121">Recupera o número de atributos contidos na SoH.</span><span class="sxs-lookup"><span data-stu-id="bd47b-121">Retrieves the number of attributes contained in the SoH.</span></span><br/>                   |
| [<span data-ttu-id="bd47b-122">**INapSoHProcessor:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="bd47b-122">**INapSoHProcessor::Initialize**</span></span>](inapsohprocessor-initialize-method.md)                       | <span data-ttu-id="bd47b-123">Inicializa o pacote de protocolo SoH e o sistema NAP para processamento de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="bd47b-123">Initializes the SoH protocol packet and NAP System for content processing.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd47b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd47b-124">Requirements</span></span>



| <span data-ttu-id="bd47b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd47b-125">Requirement</span></span> | <span data-ttu-id="bd47b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="bd47b-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd47b-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd47b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bd47b-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd47b-128">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bd47b-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd47b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bd47b-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd47b-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bd47b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd47b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd47b-132"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd47b-132"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd47b-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="bd47b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd47b-134"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd47b-134"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd47b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bd47b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd47b-136"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd47b-136"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="bd47b-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd47b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd47b-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="bd47b-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bd47b-139">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="bd47b-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

