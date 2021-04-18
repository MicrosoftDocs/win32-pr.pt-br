---
description: Solicita uma verificação do usuário.
ms.assetid: e8b7155c-3444-4aa8-8a15-3b3624a44a77
title: 'Método ISCardVerify:: Verify'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.Verify
api_type:
- COM
api_location: ''
ms.openlocfilehash: 68f3a97df672d97e635180f41405a75c4cb84661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751820"
---
# <a name="iscardverifyverify-method"></a><span data-ttu-id="3e08d-103">Método ISCardVerify:: Verify</span><span class="sxs-lookup"><span data-stu-id="3e08d-103">ISCardVerify::Verify method</span></span>

<span data-ttu-id="3e08d-104">\[O método **Verify** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3e08d-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e08d-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3e08d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3e08d-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3e08d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3e08d-107">O método **Verify** solicita uma verificação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3e08d-107">The **Verify** method requests a verification of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e08d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e08d-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in] LPBYTEBUFFER pCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="3e08d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e08d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e08d-110">*Pcode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e08d-110">*pCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e08d-111">Contém o código a ser apresentado ao [*cartão inteligente*](../secgloss/s-gly.md) no processo de CHV (verificação de titular de cartão).</span><span class="sxs-lookup"><span data-stu-id="3e08d-111">Contains the code to be presented to the [*smart card*](../secgloss/s-gly.md) in the CHV (card holder verification) process.</span></span>

</dd> <dt>

<span data-ttu-id="3e08d-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="3e08d-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e08d-113">Indica se o código é global ou local.</span><span class="sxs-lookup"><span data-stu-id="3e08d-113">Indicates whether the code is global or local.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="3e08d-114">**SC \_ fl \_ IHV \_ global**</span><span class="sxs-lookup"><span data-stu-id="3e08d-114">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="3e08d-115">**SC \_ fl \_ IHV \_ local**</span><span class="sxs-lookup"><span data-stu-id="3e08d-115">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3e08d-116">*lRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3e08d-116">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e08d-117">Referência específica do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="3e08d-117">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e08d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e08d-118">Return value</span></span>

<span data-ttu-id="3e08d-119">O método **Verify** retorna um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="3e08d-119">The **Verify** method returns one of the following values:</span></span>



| <span data-ttu-id="3e08d-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3e08d-120">Return code</span></span>                                                                                   | <span data-ttu-id="3e08d-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3e08d-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3e08d-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e08d-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3e08d-123">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3e08d-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3e08d-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e08d-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3e08d-125">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3e08d-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3e08d-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e08d-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3e08d-127">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="3e08d-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3e08d-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3e08d-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3e08d-129">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="3e08d-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3e08d-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e08d-130">Remarks</span></span>

<span data-ttu-id="3e08d-131">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="3e08d-131">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="3e08d-132">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3e08d-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3e08d-133">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3e08d-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e08d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e08d-134">Requirements</span></span>



| <span data-ttu-id="3e08d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e08d-135">Requirement</span></span> | <span data-ttu-id="3e08d-136">Valor</span><span class="sxs-lookup"><span data-stu-id="3e08d-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3e08d-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e08d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="3e08d-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3e08d-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3e08d-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3e08d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="3e08d-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e08d-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3e08d-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3e08d-141">End of client support</span></span><br/>    | <span data-ttu-id="3e08d-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e08d-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3e08d-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3e08d-143">End of server support</span></span><br/>    | <span data-ttu-id="3e08d-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3e08d-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3e08d-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e08d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e08d-146">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="3e08d-146">**ISCardVerify**</span></span>](iscardverify.md)
</dt> </dl>

 

 
