---
description: Representa a configuração do histórico de arquivos do usuário sob o qual o objeto FhConfigMgr é criado. Todas as operações de configuração são executadas chamando os métodos da interface IFhConfigMgr.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: Classe FhConfigMgr (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826368"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="3812d-104">Classe FhConfigMgr</span><span class="sxs-lookup"><span data-stu-id="3812d-104">FhConfigMgr class</span></span>

<span data-ttu-id="3812d-105">Representa a configuração do histórico de arquivos do usuário sob o qual o objeto **FhConfigMgr** é criado.</span><span class="sxs-lookup"><span data-stu-id="3812d-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="3812d-106">Todas as operações de configuração são executadas chamando os métodos da interface [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .</span><span class="sxs-lookup"><span data-stu-id="3812d-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="3812d-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="3812d-107">When to implement</span></span>

<span data-ttu-id="3812d-108">A API de histórico de arquivo implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3812d-108">The File History API implements this class.</span></span> <span data-ttu-id="3812d-109">Para criar uma instância dessa classe, use a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="3812d-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3812d-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3812d-110">Requirements</span></span>



| <span data-ttu-id="3812d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3812d-111">Requirement</span></span> | <span data-ttu-id="3812d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3812d-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3812d-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3812d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3812d-114">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3812d-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3812d-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3812d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3812d-116">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3812d-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3812d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3812d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3812d-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3812d-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="3812d-119">INSERI</span><span class="sxs-lookup"><span data-stu-id="3812d-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3812d-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3812d-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
