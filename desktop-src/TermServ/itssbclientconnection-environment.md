---
title: Propriedade de ambiente ITsSbClientConnection
description: Recupera um objeto que contém informações sobre o ambiente que hospeda o computador de destino.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de ambiente
- Propriedade de ambiente Serviços de Área de Trabalho Remota, interface ITsSbClientConnection
- Serviços de Área de Trabalho Remota de interface ITsSbClientConnection, propriedade de ambiente
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18018c8f8fc5e7d017809cf5fe109db7c52712c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455482"
---
# <a name="itssbclientconnectionenvironment-property"></a><span data-ttu-id="e87e4-106">Propriedade ITsSbClientConnection:: Environment</span><span class="sxs-lookup"><span data-stu-id="e87e4-106">ITsSbClientConnection::Environment property</span></span>

<span data-ttu-id="e87e4-107">Recupera um objeto que contém informações sobre o ambiente que hospeda o computador de destino.</span><span class="sxs-lookup"><span data-stu-id="e87e4-107">Retrieves an object that contains information about the environment that hosts the target computer.</span></span> <span data-ttu-id="e87e4-108">Por exemplo, em um cenário de área de trabalho virtual, esse objeto contém informações sobre o computador que hospeda a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e87e4-108">For example, in a virtual desktop scenario, this object would contain information about the computer that hosts the virtual machine.</span></span>

<span data-ttu-id="e87e4-109">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e87e4-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e87e4-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e87e4-110">Syntax</span></span>


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a><span data-ttu-id="e87e4-111">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e87e4-111">Property value</span></span>

<span data-ttu-id="e87e4-112">Um ponteiro para um ponteiro para um objeto de ambiente [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .</span><span class="sxs-lookup"><span data-stu-id="e87e4-112">A pointer to a pointer to an [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) environment object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e87e4-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e87e4-113">Error codes</span></span>

<span data-ttu-id="e87e4-114">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e87e4-114">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e87e4-115">Caso contrário, ele retorna um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="e87e4-115">Otherwise, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e87e4-116">Os valores possíveis incluem, mas não estão limitados a, aqueles na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="e87e4-116">Possible values include, but are not limited to, those in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e87e4-117">\_ponteiro E</span><span class="sxs-lookup"><span data-stu-id="e87e4-117">E\_POINTER</span></span>
</dt> <dd>

<span data-ttu-id="e87e4-118">O ambiente não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="e87e4-118">The environment was not found.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e87e4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e87e4-119">Remarks</span></span>

<span data-ttu-id="e87e4-120">Um plug-in de orquestração pode chamar esse método para recuperar informações de ambiente sobre uma máquina virtual de destino.</span><span class="sxs-lookup"><span data-stu-id="e87e4-120">An orchestration plug-in can call this method to retrieve environment information about a target virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="e87e4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e87e4-121">Requirements</span></span>



| <span data-ttu-id="e87e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e87e4-122">Requirement</span></span> | <span data-ttu-id="e87e4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e87e4-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e87e4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e87e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e87e4-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e87e4-125">None supported</span></span><br/>                                                            |
| <span data-ttu-id="e87e4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e87e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e87e4-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e87e4-127">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="e87e4-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="e87e4-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e87e4-129"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e87e4-129"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e87e4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e87e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87e4-131">**ITsSbClientConnection**</span><span class="sxs-lookup"><span data-stu-id="e87e4-131">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

 





