---
description: O método de autenticação de usuário \_ permite o acesso aos serviços de autenticação de usuário.
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: 'Método ISCardAuth:: User_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827033"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="3b945-103">Método de autenticação de usuário ISCardAuth:: \_</span><span class="sxs-lookup"><span data-stu-id="3b945-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="3b945-104">\[O método de **\_ autenticação de usuário** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="3b945-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3b945-105">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3b945-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3b945-106">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3b945-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3b945-107">O método de autenticação de **usuário \_** permite o acesso aos serviços de autenticação de usuário.</span><span class="sxs-lookup"><span data-stu-id="3b945-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b945-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b945-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3b945-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b945-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b945-110">*lAlgorID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b945-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b945-111">Algoritmo a ser usado no processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3b945-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="3b945-112">*pParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b945-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b945-113">Um objeto [**IByteBuffer**](ibytebuffer.md) que contém parâmetros específicos do fornecedor do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3b945-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="3b945-114">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b945-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b945-115">Dados a serem usados no processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="3b945-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b945-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b945-116">Return value</span></span>

<span data-ttu-id="3b945-117">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="3b945-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3b945-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b945-118">Return code</span></span>                                                                                   | <span data-ttu-id="3b945-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b945-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3b945-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3b945-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3b945-121">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="3b945-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3b945-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3b945-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3b945-123">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="3b945-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3b945-124"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="3b945-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3b945-125">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="3b945-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3b945-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3b945-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3b945-127">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="3b945-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3b945-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b945-128">Remarks</span></span>

<span data-ttu-id="3b945-129">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="3b945-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="3b945-130">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de [*cartão inteligente*](../secgloss/s-gly.md) se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="3b945-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3b945-131">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3b945-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b945-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b945-132">Requirements</span></span>



| <span data-ttu-id="3b945-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b945-133">Requirement</span></span> | <span data-ttu-id="3b945-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3b945-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b945-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b945-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3b945-136">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3b945-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3b945-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b945-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3b945-138">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3b945-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3b945-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="3b945-139">End of client support</span></span><br/>    | <span data-ttu-id="3b945-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3b945-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3b945-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="3b945-141">End of server support</span></span><br/>    | <span data-ttu-id="3b945-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3b945-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3b945-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b945-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b945-144">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="3b945-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="3b945-145">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="3b945-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
