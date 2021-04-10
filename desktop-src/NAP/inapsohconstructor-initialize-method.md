---
title: Método de inicialização de INapSoHConstructor (NapProtocol. h)
description: Inicializa um pacote de protocolo SoH no sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Inicializar método NAP
- Método Initialize NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, método Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918376"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="e5d62-106">Método INapSoHConstructor:: Initialize</span><span class="sxs-lookup"><span data-stu-id="e5d62-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="e5d62-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="e5d62-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e5d62-108">O método **INapSoHConstructor:: Initialize** Inicializa um pacote de protocolo soh no sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="e5d62-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d62-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5d62-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="e5d62-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5d62-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d62-111">*ID* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-112">Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do SHA ou SHV que está construindo o pacote.</span><span class="sxs-lookup"><span data-stu-id="e5d62-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="e5d62-113">*Isrequest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d62-114">Um **bool** que será **verdadeiro** se o pacote for um [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se for um **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="e5d62-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d62-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5d62-115">Return value</span></span>

<span data-ttu-id="e5d62-116">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="e5d62-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e5d62-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5d62-117">Return code</span></span>                                                                                     | <span data-ttu-id="e5d62-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5d62-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e5d62-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e5d62-120">Operação concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="e5d62-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e5d62-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e5d62-122">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e5d62-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e5d62-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e5d62-124">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e5d62-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5d62-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5d62-125">Remarks</span></span>

<span data-ttu-id="e5d62-126">Esse método deve ser chamado exatamente uma vez por pacote.</span><span class="sxs-lookup"><span data-stu-id="e5d62-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="e5d62-127">O [SystemHealthEntityId](nap-datatypes.md) especificado na *ID* é o primeiro TLV no pacote soh criado recentemente e tem o tipo de atributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span><span class="sxs-lookup"><span data-stu-id="e5d62-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5d62-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5d62-128">Requirements</span></span>



| <span data-ttu-id="e5d62-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5d62-129">Requirement</span></span> | <span data-ttu-id="e5d62-130">Valor</span><span class="sxs-lookup"><span data-stu-id="e5d62-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d62-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5d62-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d62-132">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e5d62-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5d62-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d62-134">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e5d62-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e5d62-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5d62-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5d62-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="e5d62-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="e5d62-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5d62-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5d62-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d62-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d62-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5d62-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="e5d62-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5d62-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d62-142">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="e5d62-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





