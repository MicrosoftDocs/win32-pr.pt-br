---
description: Essa função usa o atributo Origin se estiver presente do token Origin e os definirá em uma duplicata do token de herança e retornará o token duplicado.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: função srpInheritOriginClaim
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761854"
---
# <a name="srpinheritoriginclaim-function"></a><span data-ttu-id="c2a96-103">função srpInheritOriginClaim</span><span class="sxs-lookup"><span data-stu-id="c2a96-103">srpInheritOriginClaim function</span></span>

<span data-ttu-id="c2a96-104">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c2a96-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c2a96-105">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c2a96-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c2a96-106">Essa função usa o atributo Origin se estiver presente do token Origin e os definirá em uma duplicata do token de herança e retornará o token duplicado.</span><span class="sxs-lookup"><span data-stu-id="c2a96-106">This function takes the origin attribute if present from the origin token and sets them on a duplicate of the inheriting token, and returns the duplicate token.</span></span> <span data-ttu-id="c2a96-107">O chamador pode representar o token retornado.</span><span class="sxs-lookup"><span data-stu-id="c2a96-107">The caller can then impersonate the returned token.</span></span> <span data-ttu-id="c2a96-108">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="c2a96-108">This function has no associated import library.</span></span> <span data-ttu-id="c2a96-109">Você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a srpapi.dll.</span><span class="sxs-lookup"><span data-stu-id="c2a96-109">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to srpapi.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a96-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2a96-110">Syntax</span></span>


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a><span data-ttu-id="c2a96-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2a96-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a96-112">*OriginToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2a96-112">*OriginToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a96-113">Identificador para o token que está duplicado e recebe o atributo de origem herdado.</span><span class="sxs-lookup"><span data-stu-id="c2a96-113">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="c2a96-114">Esse identificador deve ser aberto com o \_ direito de acesso duplicado de token.</span><span class="sxs-lookup"><span data-stu-id="c2a96-114">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span>

</dd> <dt>

<span data-ttu-id="c2a96-115">*InheritingToken* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c2a96-115">*InheritingToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a96-116">Identificador para o token que está duplicado e recebe o atributo de origem herdado.</span><span class="sxs-lookup"><span data-stu-id="c2a96-116">Handle to the token which is duplicated and receives the inherited origin attribute.</span></span> <span data-ttu-id="c2a96-117">Esse identificador deve ser aberto com o \_ direito de acesso duplicado de token.</span><span class="sxs-lookup"><span data-stu-id="c2a96-117">This handle must be opened with the TOKEN\_DUPLICATE access right.</span></span> 

</dd> <dt>

<span data-ttu-id="c2a96-118">*ResultToken*</span><span class="sxs-lookup"><span data-stu-id="c2a96-118">*ResultToken*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a96-119">Em caso de sucesso, recebe o token duplicado.</span><span class="sxs-lookup"><span data-stu-id="c2a96-119">On success, receives the duplicated token.</span></span> <span data-ttu-id="c2a96-120">O chamador pode representá-lo para executar operações com o atributo Origin herdado.</span><span class="sxs-lookup"><span data-stu-id="c2a96-120">The caller can impersonate it to perform operations with the inherited origin attribute.</span></span> <span data-ttu-id="c2a96-121">O chamador assume a propriedade desse identificador e deve fechá-lo.</span><span class="sxs-lookup"><span data-stu-id="c2a96-121">The caller takes ownership of this handle and must close it.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a96-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2a96-122">Return value</span></span>

<span data-ttu-id="c2a96-123">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c2a96-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2a96-124">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2a96-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a96-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2a96-125">Requirements</span></span>



| <span data-ttu-id="c2a96-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a96-126">Requirement</span></span> | <span data-ttu-id="c2a96-127">Valor</span><span class="sxs-lookup"><span data-stu-id="c2a96-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a96-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2a96-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a96-129">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c2a96-129">Windows 10 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2a96-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2a96-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a96-131">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="c2a96-131">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2a96-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c2a96-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2a96-133"><dt>Srpapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2a96-133"><dt>Srpapi.dll</dt></span></span> </dl> |



 

