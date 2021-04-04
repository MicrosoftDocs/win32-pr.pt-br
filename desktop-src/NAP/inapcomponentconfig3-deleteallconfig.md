---
title: Método INapComponentConfig3 DeleteAllConfig (NapCommon. h)
description: É implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.
ms.assetid: 7f079743-1c32-430d-a250-b49a96b99f14
keywords:
- Método DeleteAllConfig NAP
- Método DeleteAllConfig NAP, interface INapComponentConfig3
- INapComponentConfig3 interface NAP, método DeleteAllConfig
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteAllConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a766690114db20fb9be5cccbd4508f4565f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824290"
---
# <a name="inapcomponentconfig3deleteallconfig-method"></a><span data-ttu-id="2eb16-106">INapComponentConfig3: método eleteAllConfig de:D</span><span class="sxs-lookup"><span data-stu-id="2eb16-106">INapComponentConfig3::DeleteAllConfig method</span></span>

> [!Note]  
> <span data-ttu-id="2eb16-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="2eb16-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2eb16-108">O método **DeleteAllConfig** é implementado por SHVs (validadores da integridade do sistema) para fornecer uma maneira de redefinir o armazenamento SHV para seu estado original após a instalação.</span><span class="sxs-lookup"><span data-stu-id="2eb16-108">The **DeleteAllConfig** method is implemented by system health validators (SHVs) to provide a way to reset the SHV store to its original state after setup.</span></span> <span data-ttu-id="2eb16-109">Todos os dados de configuração, exceto a configuração padrão, devem ser excluídos.</span><span class="sxs-lookup"><span data-stu-id="2eb16-109">All configuration data except for the default configuration must be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb16-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2eb16-110">Syntax</span></span>


```C++
HRESULT DeleteAllConfig();
```



## <a name="parameters"></a><span data-ttu-id="2eb16-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2eb16-111">Parameters</span></span>

<span data-ttu-id="2eb16-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2eb16-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2eb16-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2eb16-113">Return value</span></span>

<span data-ttu-id="2eb16-114">Retorna um dos seguintes códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="2eb16-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="2eb16-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2eb16-115">Return code</span></span>                                                                           | <span data-ttu-id="2eb16-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="2eb16-116">Description</span></span>                             |
|---------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="2eb16-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2eb16-117"><dt>**S\_OK** </dt></span></span> </dl> | <span data-ttu-id="2eb16-118">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="2eb16-118">The operation is successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2eb16-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eb16-119">Requirements</span></span>



| <span data-ttu-id="2eb16-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eb16-120">Requirement</span></span> | <span data-ttu-id="2eb16-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2eb16-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb16-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb16-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb16-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2eb16-123">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2eb16-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eb16-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb16-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="2eb16-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2eb16-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2eb16-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eb16-127"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eb16-127"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="2eb16-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="2eb16-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2eb16-129"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2eb16-129"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eb16-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eb16-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb16-131">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="2eb16-131">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





