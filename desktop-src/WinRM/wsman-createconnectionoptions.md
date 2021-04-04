---
title: Método WSMan. createconnectoptions (WSManDisp. h)
description: Cria um objeto ConnectionOptions que especifica o nome de usuário e a senha usados ao criar uma sessão.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Método createconnectoptions Gerenciamento Remoto do Windows
- Método createconnectoptions Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, método createconnectoptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824278"
---
# <a name="wsmancreateconnectionoptions-method"></a><span data-ttu-id="64956-106">Método WSMan. createconnectoptions</span><span class="sxs-lookup"><span data-stu-id="64956-106">WSMan.CreateConnectionOptions method</span></span>

<span data-ttu-id="64956-107">Cria um objeto [**ConnectionOptions**](connectionoptions.md) que especifica o nome de usuário e a senha usados ao criar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="64956-107">Creates a [**ConnectionOptions**](connectionoptions.md) object that specifies the user name and password used when creating a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="64956-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64956-108">Syntax</span></span>


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a><span data-ttu-id="64956-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64956-109">Parameters</span></span>

<span data-ttu-id="64956-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="64956-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="64956-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64956-111">Return value</span></span>

<span data-ttu-id="64956-112">Um objeto [**ConnectionOptions**](connectionoptions.md) usado para especificar um par de nome de usuário e senha que é usado para identificar um usuário para autenticação.</span><span class="sxs-lookup"><span data-stu-id="64956-112">A [**ConnectionOptions**](connectionoptions.md) object used to specify a user name and password pair that is used to identify a user for authentication.</span></span>

## <a name="remarks"></a><span data-ttu-id="64956-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="64956-113">Remarks</span></span>

<span data-ttu-id="64956-114">A sintaxe a seguir é usada para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="64956-114">The following syntax is used to call this method.</span></span>


```VB
Set options = wsman.CreateConnectionOptions
```



## <a name="requirements"></a><span data-ttu-id="64956-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64956-115">Requirements</span></span>



| <span data-ttu-id="64956-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="64956-116">Requirement</span></span> | <span data-ttu-id="64956-117">Valor</span><span class="sxs-lookup"><span data-stu-id="64956-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="64956-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64956-118">Minimum supported client</span></span><br/> | <span data-ttu-id="64956-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64956-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="64956-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64956-120">Minimum supported server</span></span><br/> | <span data-ttu-id="64956-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64956-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="64956-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="64956-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="64956-123"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="64956-123"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="64956-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="64956-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64956-125"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64956-125"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="64956-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="64956-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="64956-127"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="64956-127"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="64956-128">DLL</span><span class="sxs-lookup"><span data-stu-id="64956-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64956-129"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64956-129"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="64956-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="64956-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64956-131">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="64956-131">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="64956-132">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="64956-132">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> </dl>

 

 





