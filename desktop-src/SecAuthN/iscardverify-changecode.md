---
description: Substitui o código atual de CHV (verificação de titular de cartão) por um novo código CHV.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Método ISCardVerify:: ChangeCode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662328"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="edb4b-103">Método ISCardVerify:: ChangeCode</span><span class="sxs-lookup"><span data-stu-id="edb4b-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="edb4b-104">\[O método **ChangeCode** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="edb4b-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="edb4b-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="edb4b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="edb4b-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="edb4b-107">O método **ChangeCode** substitui o código de CHV atual (verificação de titular de cartão) pelo novo código CHV.</span><span class="sxs-lookup"><span data-stu-id="edb4b-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb4b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="edb4b-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="edb4b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edb4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb4b-110">*pOldCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb4b-111">Ponteiro para um [**IByteBuffer**](ibytebuffer.md) que contém o código atual do usuário.</span><span class="sxs-lookup"><span data-stu-id="edb4b-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="edb4b-112">*pNewCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb4b-113">Ponteiro para um [**IByteBuffer**](ibytebuffer.md) que contém o novo código que será apresentado ao [*cartão inteligente*](../secgloss/s-gly.md) durante o processo de alteração para autenticar o usuário.</span><span class="sxs-lookup"><span data-stu-id="edb4b-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="edb4b-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb4b-115">Indica se o código é global ou local e se o código deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="edb4b-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="edb4b-116">**SC \_ fl \_ IHV \_ global**</span><span class="sxs-lookup"><span data-stu-id="edb4b-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="edb4b-117">**SC \_ fl \_ IHV \_ local**</span><span class="sxs-lookup"><span data-stu-id="edb4b-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="edb4b-118">**\_habilitar SC FL \_ IHV \_**</span><span class="sxs-lookup"><span data-stu-id="edb4b-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="edb4b-119">**\_desabilitar o \_ IHV \_ fl do SC**</span><span class="sxs-lookup"><span data-stu-id="edb4b-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="edb4b-120">*lRef* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb4b-121">Referência específica do cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="edb4b-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb4b-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="edb4b-122">Return value</span></span>

<span data-ttu-id="edb4b-123">O método retorna um dos seguintes valores possíveis:</span><span class="sxs-lookup"><span data-stu-id="edb4b-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="edb4b-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="edb4b-124">Return code</span></span>                                                                                   | <span data-ttu-id="edb4b-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="edb4b-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="edb4b-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="edb4b-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="edb4b-127">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="edb4b-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="edb4b-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="edb4b-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="edb4b-129">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="edb4b-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="edb4b-130"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="edb4b-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="edb4b-131">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="edb4b-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="edb4b-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="edb4b-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="edb4b-133">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="edb4b-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="edb4b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="edb4b-134">Remarks</span></span>

<span data-ttu-id="edb4b-135">Para obter uma lista de todos os métodos definidos por essa interface, consulte [**ISCardVerify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="edb4b-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="edb4b-136">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="edb4b-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="edb4b-137">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="edb4b-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edb4b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edb4b-138">Requirements</span></span>



| <span data-ttu-id="edb4b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb4b-139">Requirement</span></span> | <span data-ttu-id="edb4b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="edb4b-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="edb4b-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edb4b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="edb4b-142">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="edb4b-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="edb4b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="edb4b-144">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="edb4b-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="edb4b-145">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="edb4b-145">End of client support</span></span><br/>    | <span data-ttu-id="edb4b-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="edb4b-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="edb4b-147">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="edb4b-147">End of server support</span></span><br/>    | <span data-ttu-id="edb4b-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="edb4b-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="edb4b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="edb4b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb4b-150">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="edb4b-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="edb4b-151">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="edb4b-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="edb4b-152">Valores de retorno do cartão inteligente</span><span class="sxs-lookup"><span data-stu-id="edb4b-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
