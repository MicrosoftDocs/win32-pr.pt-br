---
description: Instala um objeto ActiveX.
ms.assetid: 0eb725a9-ceb8-40e5-808d-ac2b286a48b6
title: Interface IeAxiSystemInstaller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 391088a70aa845cd685511f10e4eb6e809dc7fcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011623"
---
# <a name="ieaxisysteminstaller-interface"></a><span data-ttu-id="9644f-103">Interface IeAxiSystemInstaller</span><span class="sxs-lookup"><span data-stu-id="9644f-103">IeAxiSystemInstaller interface</span></span>

<span data-ttu-id="9644f-104">A interface **IeAxiSystemInstaller** instala um objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="9644f-104">The **IeAxiSystemInstaller** interface installs an ActiveX object.</span></span>

<span data-ttu-id="9644f-105">Essa interface não é declarada em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="9644f-105">This interface is not declared in a public header.</span></span> <span data-ttu-id="9644f-106">Os aplicativos devem defini-lo por conta própria.</span><span class="sxs-lookup"><span data-stu-id="9644f-106">Applications must define it themselves.</span></span> <span data-ttu-id="9644f-107">O fragmento IDL (Interface Definition Language) a seguir descreve essa interface, incluindo seu IID.</span><span class="sxs-lookup"><span data-stu-id="9644f-107">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(a50ea6f8-4764-4299-b309-022b2a8b4d8d),
    
]
interface IeAxiSystemInstaller : IUnknown
{
    
    HRESULT InitializeSystemInstaller(  [in] BSTR bstrUrl,
                                  [in] DWORD dwClientPID,
                                  [in] IUnknown* pCallback,
                                  [out] BSTR * pbstrNonce);
}

```

## <a name="members"></a><span data-ttu-id="9644f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9644f-108">Members</span></span>

<span data-ttu-id="9644f-109">A interface **IeAxiSystemInstaller** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9644f-109">The **IeAxiSystemInstaller** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9644f-110">**IeAxiSystemInstaller** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9644f-110">**IeAxiSystemInstaller** also has these types of members:</span></span>

-   [<span data-ttu-id="9644f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9644f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9644f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9644f-112">Methods</span></span>

<span data-ttu-id="9644f-113">A interface **IeAxiSystemInstaller** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9644f-113">The **IeAxiSystemInstaller** interface has these methods.</span></span>



| <span data-ttu-id="9644f-114">Método</span><span class="sxs-lookup"><span data-stu-id="9644f-114">Method</span></span>                                                                              | <span data-ttu-id="9644f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9644f-115">Description</span></span>                                       |
|:------------------------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="9644f-116">**InitializeSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="9644f-116">**InitializeSystemInstaller**</span></span>](ieaxisysteminstaller-initializesysteminstaller.md) | <span data-ttu-id="9644f-117">Instala o objeto ActiveX especificado.</span><span class="sxs-lookup"><span data-stu-id="9644f-117">Installs the specified ActiveX object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9644f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9644f-118">Requirements</span></span>



| <span data-ttu-id="9644f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9644f-119">Requirement</span></span> | <span data-ttu-id="9644f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9644f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9644f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9644f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9644f-122">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="9644f-122">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="9644f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9644f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9644f-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9644f-124">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="9644f-125">IID</span><span class="sxs-lookup"><span data-stu-id="9644f-125">IID</span></span><br/>                      | <span data-ttu-id="9644f-126">IID \_ IeAxiSystemInstaller é definido como a50ea6f8-4764-4299-b309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="9644f-126">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



 

