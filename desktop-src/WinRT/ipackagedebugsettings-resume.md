---
description: Retoma os processos do pacote se eles estiverem suspensos no momento.
ms.assetid: c5376e00-b4b7-4a81-a84c-3a46758fe130
title: 'Método IPackageDebugSettings:: resume'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPackageDebugSettings.Resume
api_type:
- COM
api_location:
- Shobjidl.idl
ms.openlocfilehash: 2d36b11baffdc3f587924acd1732cbdfdb43d37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807960"
---
# <a name="ipackagedebugsettingsresume-method"></a><span data-ttu-id="b10ec-103">Método IPackageDebugSettings:: resume</span><span class="sxs-lookup"><span data-stu-id="b10ec-103">IPackageDebugSettings::Resume method</span></span>

<span data-ttu-id="b10ec-104">Retoma os processos do pacote se eles estiverem suspensos no momento.</span><span class="sxs-lookup"><span data-stu-id="b10ec-104">Resumes the processes of the package if they are currently suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="b10ec-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b10ec-105">Syntax</span></span>


```C++
HRESULT Resume(
  [in] LPCWSTR packageFullName
);
```



## <a name="parameters"></a><span data-ttu-id="b10ec-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b10ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b10ec-107">*packageFullName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b10ec-107">*packageFullName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b10ec-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="b10ec-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="b10ec-109">O nome completo do pacote.</span><span class="sxs-lookup"><span data-stu-id="b10ec-109">The package full name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b10ec-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b10ec-110">Return value</span></span>

<span data-ttu-id="b10ec-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b10ec-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b10ec-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b10ec-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b10ec-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b10ec-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b10ec-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b10ec-114">Remarks</span></span>

<span data-ttu-id="b10ec-115">Cada processo recebe o evento de [**retomada**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="b10ec-115">Each process receives the [**Resuming**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) event.</span></span> <span data-ttu-id="b10ec-116">Pode ser útil para os desenvolvedores percorrer como seus aplicativos respondem a esse evento.</span><span class="sxs-lookup"><span data-stu-id="b10ec-116">It can be useful for developers to step through how their apps respond to this event.</span></span>

## <a name="requirements"></a><span data-ttu-id="b10ec-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b10ec-117">Requirements</span></span>



| <span data-ttu-id="b10ec-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b10ec-118">Requirement</span></span> | <span data-ttu-id="b10ec-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b10ec-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b10ec-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b10ec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b10ec-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b10ec-121">Windows 8</span></span><br/>                                                                    |
| <span data-ttu-id="b10ec-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b10ec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b10ec-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b10ec-123">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="b10ec-124">INSERI</span><span class="sxs-lookup"><span data-stu-id="b10ec-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b10ec-125"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b10ec-125"><dt>Shobjidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b10ec-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b10ec-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b10ec-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b10ec-127">[**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85))</span></span>
</dt> </dl>

 

 
