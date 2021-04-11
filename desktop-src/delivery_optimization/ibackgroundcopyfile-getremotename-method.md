---
title: Método getremotename IBackgroundCopyFile (Deliveryoptimization. h)
description: Recupera o nome remoto do arquivo.
ms.assetid: 518857E0-C16A-400B-8F3D-5264B3CB43FF
keywords:
- Método getremotename
- Método getremotename, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, método getremotename
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9984ed9971fdfb91279dabc5810490b62804b7e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009281"
---
# <a name="ibackgroundcopyfilegetremotename-method"></a><span data-ttu-id="b0505-106">Método IBackgroundCopyFile:: getremotename</span><span class="sxs-lookup"><span data-stu-id="b0505-106">IBackgroundCopyFile::GetRemoteName method</span></span>

<span data-ttu-id="b0505-107">Recupera o nome remoto do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b0505-107">Retrieves the remote name of the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0505-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0505-108">Syntax</span></span>


```C++
HRESULT GetRemoteName(
  [out] LPWSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="b0505-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0505-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0505-110">*ppName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0505-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0505-111">Cadeia de caracteres terminada em nulo que contém o nome remoto do arquivo a ser transferido.</span><span class="sxs-lookup"><span data-stu-id="b0505-111">Null-terminated string that contains the remote name of the file to transfer.</span></span> <span data-ttu-id="b0505-112">O nome é totalmente qualificado.</span><span class="sxs-lookup"><span data-stu-id="b0505-112">The name is fully qualified.</span></span> <span data-ttu-id="b0505-113">Chame a função [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar *ppName* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="b0505-113">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0505-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0505-114">Return value</span></span>

<span data-ttu-id="b0505-115">Esse método retorna **S_OK** em caso de êxito ou um dos valores padrão com **HRESULT** em erro.</span><span class="sxs-lookup"><span data-stu-id="b0505-115">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0505-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0505-116">Remarks</span></span>

<span data-ttu-id="b0505-117">Para alterar o nome do arquivo remoto, chame o método [**IBackgroundCopyFile2:: Setremotoname**](ibackgroundcopyfile2-setremotename-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b0505-117">To change the remote file name, call the [**IBackgroundCopyFile2::SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0505-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0505-118">Requirements</span></span>



| <span data-ttu-id="b0505-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0505-119">Requirement</span></span> | <span data-ttu-id="b0505-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b0505-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0505-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0505-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b0505-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="b0505-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b0505-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0505-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b0505-124">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="b0505-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b0505-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0505-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0505-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0505-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0505-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="b0505-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b0505-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b0505-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b0505-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0505-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0505-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0505-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b0505-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b0505-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0505-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0505-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b0505-133">IID</span><span class="sxs-lookup"><span data-stu-id="b0505-133">IID</span></span><br/>                      | <span data-ttu-id="b0505-134">IID_IBackgroundCopyFile é definido como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="b0505-134">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="b0505-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0505-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0505-136">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="b0505-136">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="b0505-137">**IBackgroundCopyFile:: getlocalname**</span><span class="sxs-lookup"><span data-stu-id="b0505-137">**IBackgroundCopyFile::GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)
</dt> </dl>

 

