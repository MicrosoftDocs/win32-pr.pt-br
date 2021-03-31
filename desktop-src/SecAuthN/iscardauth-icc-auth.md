---
description: O \_ método de autenticação ICC permite que um aplicativo autentique o cartão inteligente.
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: 'Método ISCardAuth:: ICC_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920857"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="d08db-103">Método de autenticação ISCardAuth:: ICC \_</span><span class="sxs-lookup"><span data-stu-id="d08db-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="d08db-104">\[O método de **\_ autenticação ICC** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="d08db-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d08db-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d08db-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d08db-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="d08db-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d08db-107">O método de **\_ autenticação ICC** permite que um aplicativo autentique o cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="d08db-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08db-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d08db-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="d08db-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d08db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08db-110">*lAlgoID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d08db-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08db-111">Algoritmo a ser usado no processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d08db-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="d08db-112">*pParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d08db-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08db-113">Um objeto [**IByteBuffer**](ibytebuffer.md) que contém parâmetros específicos do fornecedor do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d08db-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="d08db-114">*pBuffer* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d08db-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d08db-115">Na entrada, contém os dados a serem usados no processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d08db-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="d08db-116">Na saída, contém o resultado do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d08db-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08db-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d08db-117">Return value</span></span>

<span data-ttu-id="d08db-118">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="d08db-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="d08db-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d08db-119">Return code</span></span>                                                                                   | <span data-ttu-id="d08db-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d08db-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="d08db-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d08db-122">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="d08db-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="d08db-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d08db-124">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="d08db-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="d08db-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d08db-126">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="d08db-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="d08db-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d08db-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d08db-128">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="d08db-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="d08db-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08db-129">Remarks</span></span>

<span data-ttu-id="d08db-130">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="d08db-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="d08db-131">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="d08db-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="d08db-132">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d08db-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d08db-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d08db-133">Requirements</span></span>



| <span data-ttu-id="d08db-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08db-134">Requirement</span></span> | <span data-ttu-id="d08db-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d08db-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d08db-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d08db-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d08db-137">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d08db-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d08db-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d08db-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d08db-139">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d08db-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d08db-140">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d08db-140">End of client support</span></span><br/>    | <span data-ttu-id="d08db-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d08db-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d08db-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d08db-142">End of server support</span></span><br/>    | <span data-ttu-id="d08db-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d08db-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="d08db-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="d08db-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08db-145">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="d08db-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
