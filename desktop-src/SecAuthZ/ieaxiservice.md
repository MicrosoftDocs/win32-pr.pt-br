---
description: Inicializa um objeto de serviço do sistema para instalar um objeto ActiveX quando o usuário atual não tem permissão para instalar o objeto.
ms.assetid: 42f7cf83-789b-42ea-bb1a-4b79137188ea
title: Interface IeAxiService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService
api_type:
- COM
api_location: ''
ms.openlocfilehash: 34c4743327b2539616dee6b09c34d9f479aa3303
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755968"
---
# <a name="ieaxiservice-interface"></a><span data-ttu-id="dd234-103">Interface IeAxiService</span><span class="sxs-lookup"><span data-stu-id="dd234-103">IeAxiService interface</span></span>

<span data-ttu-id="dd234-104">A interface **IAxiService** Inicializa um objeto de serviço do sistema para instalar um objeto ActiveX quando o usuário atual não tem permissão para instalar o objeto.</span><span class="sxs-lookup"><span data-stu-id="dd234-104">The **IAxiService** interface initializes a system service object to install an ActiveX object when the current user does not have permission to install the object.</span></span>

<span data-ttu-id="dd234-105">A classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="dd234-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="dd234-106">Essa interface não é declarada em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="dd234-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="dd234-107">Os aplicativos devem defini-lo por conta própria.</span><span class="sxs-lookup"><span data-stu-id="dd234-107">Applications must define it themselves.</span></span> <span data-ttu-id="dd234-108">O fragmento IDL (Interface Definition Language) a seguir descreve essa interface, incluindo seu IID.</span><span class="sxs-lookup"><span data-stu-id="dd234-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(E9E92380-9ECD-4982-A0EB-6815A56CCF27),
    pointer_default(unique)
]

interface IeAxiService : IUnknown{

    
    HRESULT Initialize(
            [in]        HWND            hwndParent,
            [in]        DWORD           dwClientPID,
            [in]        BSTR            bstrDesktop,
            [in]        BSTR            bstrClsID,              
            [in]        BSTR            bstrURL,                
            [out]       BSTR *          pbstrNonce,            
            [out]       IUnknown**      ppISyncBrokerInterface  
            );  
 
    HRESULT Cleanup();
};
```

## <a name="members"></a><span data-ttu-id="dd234-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dd234-109">Members</span></span>

<span data-ttu-id="dd234-110">A interface **IeAxiService** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dd234-110">The **IeAxiService** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dd234-111">**IeAxiService** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dd234-111">**IeAxiService** also has these types of members:</span></span>

-   [<span data-ttu-id="dd234-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd234-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dd234-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dd234-113">Methods</span></span>

<span data-ttu-id="dd234-114">A interface **IeAxiService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dd234-114">The **IeAxiService** interface has these methods.</span></span>



| <span data-ttu-id="dd234-115">Método</span><span class="sxs-lookup"><span data-stu-id="dd234-115">Method</span></span>                                        | <span data-ttu-id="dd234-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd234-116">Description</span></span>                                                        |
|:----------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="dd234-117">**Eliminação**</span><span class="sxs-lookup"><span data-stu-id="dd234-117">**Cleanup**</span></span>](ieaxiservice-cleanup.md)       | <span data-ttu-id="dd234-118">Libera recursos usados pela interface **IeAxiService** .</span><span class="sxs-lookup"><span data-stu-id="dd234-118">Frees resources used by the **IeAxiService** interface.</span></span><br/> |
| [<span data-ttu-id="dd234-119">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="dd234-119">**Initialize**</span></span>](ieaxiservice-initialize.md) | <span data-ttu-id="dd234-120">Verifica e baixa um objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="dd234-120">Checks and downloads an ActiveX object.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="dd234-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd234-121">Requirements</span></span>



| <span data-ttu-id="dd234-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd234-122">Requirement</span></span> | <span data-ttu-id="dd234-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dd234-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd234-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd234-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dd234-125">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="dd234-125">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dd234-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd234-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dd234-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dd234-127">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="dd234-128">IID</span><span class="sxs-lookup"><span data-stu-id="dd234-128">IID</span></span><br/>                      | <span data-ttu-id="dd234-129">IID \_ IeAxiService é definido como E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="dd234-129">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



 

