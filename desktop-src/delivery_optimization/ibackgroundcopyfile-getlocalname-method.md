---
title: Método getlocalname IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera o nome local do arquivo.
ms.assetid: 9AA57EB7-5C29-4E5E-972B-DD34B130E6E4
keywords:
- Método getlocalname
- Método getlocalname, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, método getlocalname
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetLocalName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1c3a957e64701242d9c698a014ec2ab4028cd85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009283"
---
# <a name="ibackgroundcopyfilegetlocalname-method"></a><span data-ttu-id="62a6e-106">Método IBackgroundCopyFile:: getlocalname</span><span class="sxs-lookup"><span data-stu-id="62a6e-106">IBackgroundCopyFile::GetLocalName method</span></span>

<span data-ttu-id="62a6e-107">Recupera o nome local do arquivo.</span><span class="sxs-lookup"><span data-stu-id="62a6e-107">Retrieves the local name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a6e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62a6e-108">Syntax</span></span>


```C++
HRESULT GetLocalName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="62a6e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62a6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a6e-110">*ppName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="62a6e-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62a6e-111">Cadeia de caracteres terminada em nulo que contém o nome do arquivo no cliente.</span><span class="sxs-lookup"><span data-stu-id="62a6e-111">Null-terminated string that contains the name of the file on the client.</span></span> <span data-ttu-id="62a6e-112">O nome é totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="62a6e-112">The name is fully qualified.</span></span> <span data-ttu-id="62a6e-113">Chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="62a6e-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a6e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62a6e-114">Return value</span></span>

<span data-ttu-id="62a6e-115">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="62a6e-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a6e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a6e-116">Requirements</span></span>



| <span data-ttu-id="62a6e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a6e-117">Requirement</span></span> | <span data-ttu-id="62a6e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="62a6e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a6e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62a6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="62a6e-120">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="62a6e-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="62a6e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62a6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="62a6e-122">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="62a6e-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="62a6e-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62a6e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="62a6e-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="62a6e-124"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="62a6e-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="62a6e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="62a6e-126"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="62a6e-126"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="62a6e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62a6e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="62a6e-128"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62a6e-128"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="62a6e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="62a6e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a6e-130"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a6e-130"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="62a6e-131">IID</span><span class="sxs-lookup"><span data-stu-id="62a6e-131">IID</span></span><br/>                      | <span data-ttu-id="62a6e-132">IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="62a6e-132">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="62a6e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="62a6e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a6e-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="62a6e-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="62a6e-135">**IBackgroundCopyFile:: getremotename**</span><span class="sxs-lookup"><span data-stu-id="62a6e-135">**IBackgroundCopyFile::GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md)
</dt> </dl>

 

