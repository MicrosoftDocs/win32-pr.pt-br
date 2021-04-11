---
title: Método gettraduzistring INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter cadeias de caracteres localizadas.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Método gettraduzistring NAP
- Método gettraduzistring NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método gettraduzistring
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919213"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="1569c-106">Método INapComponentInfo:: gettraduzistring</span><span class="sxs-lookup"><span data-stu-id="1569c-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="1569c-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="1569c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1569c-108">O método de retorno de chamada **INapComponentInfo:: Gettraduzistring** é usado pelo sistema NAP para obter cadeias de caracteres localizadas.</span><span class="sxs-lookup"><span data-stu-id="1569c-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1569c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1569c-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="1569c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1569c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1569c-111">*msgid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1569c-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1569c-112">Uma [**MessageId**](nap-datatypes.md) que contém a ID de recurso da cadeia de caracteres a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="1569c-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="1569c-113">*cadeia de caracteres* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1569c-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1569c-114">Um ponteiro para um ponteiro para um [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que contém a versão localizada da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1569c-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1569c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1569c-115">Return value</span></span>

<span data-ttu-id="1569c-116">Retorne um desses códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="1569c-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="1569c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1569c-117">Return code</span></span>                                                                                     | <span data-ttu-id="1569c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="1569c-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1569c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1569c-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1569c-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="1569c-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1569c-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1569c-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1569c-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="1569c-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1569c-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1569c-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1569c-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="1569c-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1569c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1569c-125">Remarks</span></span>

<span data-ttu-id="1569c-126">As cadeias de caracteres devem ser localizadas de acordo com a ID do idioma do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="1569c-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="1569c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1569c-127">Requirements</span></span>



| <span data-ttu-id="1569c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1569c-128">Requirement</span></span> | <span data-ttu-id="1569c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1569c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1569c-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1569c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1569c-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1569c-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1569c-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1569c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1569c-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1569c-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1569c-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1569c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1569c-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1569c-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="1569c-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="1569c-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1569c-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1569c-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1569c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="1569c-138">See also</span></span>

<dl> <span data-ttu-id="1569c-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1569c-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1569c-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="1569c-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





