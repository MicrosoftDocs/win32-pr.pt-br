---
title: Método INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Recupera o número total de atributos na SoH.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- Método GetNumberOfAttributes NAP
- Método GetNumberOfAttributes NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, método GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499372"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="60359-106">Método INapSoHProcessor:: GetNumberOfAttributes</span><span class="sxs-lookup"><span data-stu-id="60359-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="60359-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="60359-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="60359-108">O método **INapSoHProcessor:: GetNumberOfAttributes** recupera o número total de atributos na soh.</span><span class="sxs-lookup"><span data-stu-id="60359-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="60359-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="60359-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="60359-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60359-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60359-111">*attributeCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="60359-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60359-112">Um ponteiro para a contagem de atributos retornados.</span><span class="sxs-lookup"><span data-stu-id="60359-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60359-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="60359-113">Return value</span></span>

<span data-ttu-id="60359-114">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="60359-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="60359-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="60359-115">Return code</span></span>                                                                                     | <span data-ttu-id="60359-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="60359-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="60359-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60359-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="60359-118">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="60359-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="60359-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="60359-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="60359-120">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="60359-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="60359-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="60359-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="60359-122">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="60359-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="60359-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60359-123">Requirements</span></span>



| <span data-ttu-id="60359-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="60359-124">Requirement</span></span> | <span data-ttu-id="60359-125">Valor</span><span class="sxs-lookup"><span data-stu-id="60359-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="60359-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60359-126">Minimum supported client</span></span><br/> | <span data-ttu-id="60359-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="60359-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="60359-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60359-128">Minimum supported server</span></span><br/> | <span data-ttu-id="60359-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="60359-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="60359-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60359-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="60359-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="60359-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="60359-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="60359-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="60359-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="60359-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="60359-134">DLL</span><span class="sxs-lookup"><span data-stu-id="60359-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60359-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60359-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="60359-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="60359-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60359-137">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="60359-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





