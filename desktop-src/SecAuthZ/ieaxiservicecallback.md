---
description: Chamado pela interface IeAxiSystemInstaller para verificar se um objeto ActiveX pode ser instalado.
ms.assetid: d5cd6263-d07e-4261-9463-b9a06e883f16
title: Interface IeAxiServiceCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiServiceCallback
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3ad276126548ac6d5fdc2c828f722c90b43ad679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837392"
---
# <a name="ieaxiservicecallback-interface"></a><span data-ttu-id="4cef0-103">Interface IeAxiServiceCallback</span><span class="sxs-lookup"><span data-stu-id="4cef0-103">IeAxiServiceCallback interface</span></span>

<span data-ttu-id="4cef0-104">A interface **IeAxiServiceCallback** é chamada pela interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) para verificar se um objeto ActiveX pode ser instalado.</span><span class="sxs-lookup"><span data-stu-id="4cef0-104">The **IeAxiServiceCallback** interface is called by the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface to verify that an ActiveX object can be installed.</span></span>

<span data-ttu-id="4cef0-105">A classe [**CIeAxiInstallerService**](cieaxiinstallerservice.md) implementa essa interface.</span><span class="sxs-lookup"><span data-stu-id="4cef0-105">The [**CIeAxiInstallerService**](cieaxiinstallerservice.md) class implements this interface.</span></span>

<span data-ttu-id="4cef0-106">Essa interface não é declarada em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="4cef0-106">This interface is not declared in a public header.</span></span> <span data-ttu-id="4cef0-107">Os aplicativos devem defini-lo por conta própria.</span><span class="sxs-lookup"><span data-stu-id="4cef0-107">Applications must define it themselves.</span></span> <span data-ttu-id="4cef0-108">O fragmento IDL (Interface Definition Language) a seguir descreve essa interface, incluindo seu IID.</span><span class="sxs-lookup"><span data-stu-id="4cef0-108">The following Interface Definition Language (IDL) fragment describes this interface, including its IID.</span></span>

``` syntax
[
    object,
    uuid(1823E7BA-EC36-447a-9B2E-B4912E15AFE7),
    dual,
    nonextensible,
    pointer_default(unique)
]

interface IeAxiServiceCallback : IUnknown
{
    HRESULT VerifyFile(
                       [in] BSTR bstrFileUrl,
                       [out] BSTR * bstrApprovedFileName);
}

```

## <a name="members"></a><span data-ttu-id="4cef0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="4cef0-109">Members</span></span>

<span data-ttu-id="4cef0-110">A interface **IeAxiServiceCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4cef0-110">The **IeAxiServiceCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4cef0-111">**IeAxiServiceCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4cef0-111">**IeAxiServiceCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="4cef0-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="4cef0-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4cef0-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="4cef0-113">Methods</span></span>

<span data-ttu-id="4cef0-114">A interface **IeAxiServiceCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4cef0-114">The **IeAxiServiceCallback** interface has these methods.</span></span>



| <span data-ttu-id="4cef0-115">Método</span><span class="sxs-lookup"><span data-stu-id="4cef0-115">Method</span></span>                                                | <span data-ttu-id="4cef0-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="4cef0-116">Description</span></span>                                                                                                                                    |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4cef0-117">**Verificarfile**</span><span class="sxs-lookup"><span data-stu-id="4cef0-117">**VerifyFile**</span></span>](ieaxiservicecallback-verifyfile.md) | <span data-ttu-id="4cef0-118">Executa verificações de segurança no objeto ActiveX especificado e retorna o local onde o arquivo. cab correspondente foi baixado.</span><span class="sxs-lookup"><span data-stu-id="4cef0-118">Performs security checks on the specified ActiveX object and returns the location where the corresponding .cab file was downloaded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4cef0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cef0-119">Requirements</span></span>



| <span data-ttu-id="4cef0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cef0-120">Requirement</span></span> | <span data-ttu-id="4cef0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4cef0-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cef0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cef0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4cef0-123">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="4cef0-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4cef0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4cef0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4cef0-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="4cef0-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="4cef0-126">IID</span><span class="sxs-lookup"><span data-stu-id="4cef0-126">IID</span></span><br/>                      | <span data-ttu-id="4cef0-127">IID \_ IeAxiServiceCallback é definido como 1823E7BA-EC36-447A-9B2E-B4912E15AFE7</span><span class="sxs-lookup"><span data-stu-id="4cef0-127">IID\_IeAxiServiceCallback is defined as 1823E7BA-EC36-447a-9B2E-B4912E15AFE7</span></span><br/>                   |



 

