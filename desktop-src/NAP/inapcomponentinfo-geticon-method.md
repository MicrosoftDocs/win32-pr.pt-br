---
title: Método GetIcon INapComponentInfo (NapCommon. h)
description: É usado pelo sistema NAP para obter o ícone de um cliente de integridade.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Método GetIcon NAP
- Método GetIcon NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, método GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919064"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="47f8a-106">Método INapComponentInfo:: GetIcon</span><span class="sxs-lookup"><span data-stu-id="47f8a-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="47f8a-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="47f8a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="47f8a-108">O método de retorno de chamada **INapComponentInfo:: GetIcon** é usado pelo sistema NAP para obter o ícone de um cliente de integridade.</span><span class="sxs-lookup"><span data-stu-id="47f8a-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f8a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47f8a-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="47f8a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47f8a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f8a-111">*dllFilePath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="47f8a-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f8a-112">Um ponteiro para um ponteiro para um [**contadostring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) usado para retornar o caminho do arquivo da dll que contém o ícone.</span><span class="sxs-lookup"><span data-stu-id="47f8a-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="47f8a-113">*iconResourceId* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="47f8a-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f8a-114">Um ponteiro para o valor usado para retornar a ID de recurso do ícone a ser usado.</span><span class="sxs-lookup"><span data-stu-id="47f8a-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f8a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47f8a-115">Return value</span></span>

<span data-ttu-id="47f8a-116">Retorne um desses códigos de erro com base no resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="47f8a-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="47f8a-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="47f8a-117">Return code</span></span>                                                                                     | <span data-ttu-id="47f8a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="47f8a-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="47f8a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47f8a-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="47f8a-120">A operação teve êxito.</span><span class="sxs-lookup"><span data-stu-id="47f8a-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="47f8a-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="47f8a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="47f8a-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="47f8a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="47f8a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="47f8a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="47f8a-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="47f8a-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47f8a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="47f8a-125">Remarks</span></span>

<span data-ttu-id="47f8a-126">Os ícones devem ser localizados de acordo com a ID do idioma do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="47f8a-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f8a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47f8a-127">Requirements</span></span>



| <span data-ttu-id="47f8a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f8a-128">Requirement</span></span> | <span data-ttu-id="47f8a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="47f8a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f8a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47f8a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="47f8a-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="47f8a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="47f8a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="47f8a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="47f8a-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="47f8a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="47f8a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47f8a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="47f8a-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f8a-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="47f8a-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="47f8a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47f8a-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47f8a-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f8a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="47f8a-138">See also</span></span>

<dl> <span data-ttu-id="47f8a-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="47f8a-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="47f8a-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="47f8a-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





