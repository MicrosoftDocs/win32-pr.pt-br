---
description: O método de autenticação de aplicativo \_ autentica o aplicativo. Ele permite que um aplicativo se autentique (usando um protocolo de desafio/assinatura) quando a autenticação é solicitada por um cartão inteligente.
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: 'Método ISCardAuth:: APP_Auth'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827596"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="4db49-104">Método de autenticação ISCardAuth:: APP \_</span><span class="sxs-lookup"><span data-stu-id="4db49-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="4db49-105">\[O método de **\_ autenticação de aplicativo** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="4db49-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4db49-106">Ele não está disponível para uso no Windows Server 2003 com Service Pack 1 (SP1) e posterior, no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="4db49-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4db49-107">Os [módulos de cartão inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) fornecem funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="4db49-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4db49-108">O método de **\_ autenticação de aplicativo** autentica o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4db49-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="4db49-109">Ele permite que um aplicativo se autentique (usando um protocolo de desafio/assinatura) quando a autenticação é solicitada por um [*cartão inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4db49-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4db49-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4db49-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="4db49-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4db49-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db49-112">*lAlgoID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db49-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db49-113">Algoritmo a ser usado no processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4db49-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="4db49-114">*pParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db49-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db49-115">Um [**IByteBuffer**](ibytebuffer.md) que contém parâmetros específicos do fornecedor do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="4db49-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="4db49-116">*pBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4db49-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4db49-117">Dados necessários para o cálculo.</span><span class="sxs-lookup"><span data-stu-id="4db49-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4db49-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4db49-118">Return value</span></span>

<span data-ttu-id="4db49-119">O método retorna um dos seguintes valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="4db49-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4db49-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4db49-120">Return code</span></span>                                                                                   | <span data-ttu-id="4db49-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="4db49-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4db49-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4db49-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4db49-123">Operação concluída com sucesso.</span><span class="sxs-lookup"><span data-stu-id="4db49-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4db49-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4db49-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4db49-125">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="4db49-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="4db49-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="4db49-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4db49-127">Um ponteiro inadequado foi passado.</span><span class="sxs-lookup"><span data-stu-id="4db49-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="4db49-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4db49-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4db49-129">Sem memória.</span><span class="sxs-lookup"><span data-stu-id="4db49-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4db49-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4db49-130">Remarks</span></span>

<span data-ttu-id="4db49-131">Para obter uma lista de todos os métodos fornecidos por essa interface, consulte [**ISCardAuth**](iscardauth.md).</span><span class="sxs-lookup"><span data-stu-id="4db49-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="4db49-132">Além dos códigos de erro COM listados acima, essa interface pode retornar um código de erro de cartão inteligente se uma função de cartão inteligente foi chamada para concluir a solicitação.</span><span class="sxs-lookup"><span data-stu-id="4db49-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4db49-133">Para obter mais informações, consulte [valores de retorno de cartão inteligente](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4db49-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4db49-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4db49-134">Requirements</span></span>



| <span data-ttu-id="4db49-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4db49-135">Requirement</span></span> | <span data-ttu-id="4db49-136">Valor</span><span class="sxs-lookup"><span data-stu-id="4db49-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4db49-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4db49-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4db49-138">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4db49-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4db49-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4db49-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4db49-140">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4db49-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4db49-141">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="4db49-141">End of client support</span></span><br/>    | <span data-ttu-id="4db49-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4db49-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4db49-143">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="4db49-143">End of server support</span></span><br/>    | <span data-ttu-id="4db49-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4db49-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4db49-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="4db49-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db49-146">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="4db49-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="4db49-147">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="4db49-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
