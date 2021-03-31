---
description: Suspende os processos do pacote se eles estiverem em execução no momento.
ms.assetid: 83f44285-46ed-4968-b0af-7964dfacf602
title: 'Método IPackageDebugSettings:: Suspend'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Suspend
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 385ddc856661090caec4345df6651605b67fe883
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647148"
---
# <a name="ipackagedebugsettingssuspend-method"></a><span data-ttu-id="71898-103">Método IPackageDebugSettings:: Suspend</span><span class="sxs-lookup"><span data-stu-id="71898-103">IPackageDebugSettings::Suspend method</span></span>

<span data-ttu-id="71898-104">Suspende os processos do pacote se eles estiverem em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="71898-104">Suspends the processes of the package if they are currently running.</span></span>

## <a name="syntax"></a><span data-ttu-id="71898-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71898-105">Syntax</span></span>


```C++
HRESULT Suspend(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="71898-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71898-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71898-107">*packageFullName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71898-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71898-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="71898-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="71898-109">O nome completo do pacote.</span><span class="sxs-lookup"><span data-stu-id="71898-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71898-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71898-110">Return value</span></span>

<span data-ttu-id="71898-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71898-111">Type: **HRESULT**</span></span>

<span data-ttu-id="71898-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="71898-112">This method can return one of these values.</span></span>



| <span data-ttu-id="71898-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="71898-113">Return code</span></span>                                                                                            | <span data-ttu-id="71898-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="71898-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="71898-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71898-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="71898-116">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="71898-116">The operation succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="71898-117"><dt>**E \_ \_ STATECHANGE ilegais**</dt></span><span class="sxs-lookup"><span data-stu-id="71898-117"><dt>**E\_ILLEGAL\_STATECHANGE**</dt></span></span> </dl> | <span data-ttu-id="71898-118">O processo não está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="71898-118">The process is not currently running.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71898-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="71898-119">Remarks</span></span>

<span data-ttu-id="71898-120">Cada processo recebe o evento de [**suspensão**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="71898-120">Each process receives the [**Suspending**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="71898-121">Pode ser útil para os desenvolvedores percorrer como seus aplicativos respondem a esse evento.</span><span class="sxs-lookup"><span data-stu-id="71898-121">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="71898-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71898-122">Requirements</span></span>



| <span data-ttu-id="71898-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="71898-123">Requirement</span></span> | <span data-ttu-id="71898-124">Valor</span><span class="sxs-lookup"><span data-stu-id="71898-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71898-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71898-125">Minimum supported client</span></span><br/> | <span data-ttu-id="71898-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="71898-126">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="71898-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71898-127">Minimum supported server</span></span><br/> | <span data-ttu-id="71898-128">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="71898-128">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="71898-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="71898-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71898-130"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71898-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71898-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="71898-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="71898-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="71898-132">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
