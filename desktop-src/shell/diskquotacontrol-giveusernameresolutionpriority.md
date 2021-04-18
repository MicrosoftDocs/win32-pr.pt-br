---
description: Coloca o objeto de usuário especificado próximo na linha para resolução de nomes.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Método DiskQuotaControl. GiveUserNameResolutionPriority (Dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501415"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="f0137-103">Método DiskQuotaControl. GiveUserNameResolutionPriority</span><span class="sxs-lookup"><span data-stu-id="f0137-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="f0137-104">Coloca o objeto de usuário especificado próximo na linha para resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="f0137-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0137-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0137-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="f0137-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0137-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="f0137-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="f0137-108">Tipo: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f0137-108">Type: **Object**</span></span>

<span data-ttu-id="f0137-109">Uma expressão de objeto que é avaliada como o objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) do usuário.</span><span class="sxs-lookup"><span data-stu-id="f0137-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0137-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0137-110">Return value</span></span>

<span data-ttu-id="f0137-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f0137-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0137-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0137-112">Remarks</span></span>

<span data-ttu-id="f0137-113">Se a resolução assíncrona de nomes estiver habilitada, os objetos de usuário serão colocados em uma fila.</span><span class="sxs-lookup"><span data-stu-id="f0137-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="f0137-114">Por padrão, eles são atendidos na ordem em que são colocados na fila.</span><span class="sxs-lookup"><span data-stu-id="f0137-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="f0137-115">O método **GiveUserNameResolutionPriority** move um objeto para a frente da fila para que ele seja o próximo da linha a ser atendida.</span><span class="sxs-lookup"><span data-stu-id="f0137-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="f0137-116">Use a propriedade [**UserNameResolution**](diskquotacontrol-usernameresolution.md) para habilitar a resolução de nome assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f0137-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0137-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0137-117">Requirements</span></span>



| <span data-ttu-id="f0137-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0137-118">Requirement</span></span> | <span data-ttu-id="f0137-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f0137-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0137-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0137-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0137-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0137-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0137-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0137-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0137-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f0137-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f0137-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f0137-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0137-125"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0137-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="f0137-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f0137-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0137-127"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="f0137-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0137-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0137-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0137-129">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="f0137-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




