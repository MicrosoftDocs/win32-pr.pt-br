---
description: Representa o recurso de reassociação de histórico de arquivo, que permite que um usuário restabeleça uma relação com um destino de backup que foi usado pelo mesmo usuário no passado. A reassociação é executada chamando os métodos da interface IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Classe FhReassociation (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756408"
---
# <a name="fhreassociation-class"></a><span data-ttu-id="5f674-104">Classe FhReassociation</span><span class="sxs-lookup"><span data-stu-id="5f674-104">FhReassociation class</span></span>

<span data-ttu-id="5f674-105">Representa o recurso de reassociação de histórico de arquivo, que permite que um usuário restabeleça uma relação com um destino de backup que foi usado pelo mesmo usuário no passado.</span><span class="sxs-lookup"><span data-stu-id="5f674-105">Represents the File History reassociation feature, which allows a user to reestablish a relationship with a backup target that was used by the same user in the past.</span></span> <span data-ttu-id="5f674-106">A reassociação é executada chamando os métodos da interface [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .</span><span class="sxs-lookup"><span data-stu-id="5f674-106">Reassociation is performed by calling the methods of the [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="5f674-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="5f674-107">When to implement</span></span>

<span data-ttu-id="5f674-108">A API de histórico de arquivo implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5f674-108">The File History API implements this class.</span></span> <span data-ttu-id="5f674-109">Para criar uma instância dessa classe, use a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="5f674-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f674-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f674-110">Requirements</span></span>



| <span data-ttu-id="5f674-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f674-111">Requirement</span></span> | <span data-ttu-id="5f674-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5f674-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5f674-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f674-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f674-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5f674-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5f674-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f674-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f674-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5f674-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5f674-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f674-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f674-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f674-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f674-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="5f674-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f674-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f674-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
