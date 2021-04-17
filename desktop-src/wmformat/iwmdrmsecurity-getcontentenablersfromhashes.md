---
title: Método IWMDRMSecurity GetContentEnablersFromHashes (wmdrmsdk. h)
description: O método GetContentEnablersFromHashes recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados com hash.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Formato de mídia do Windows do método GetContentEnablersFromHashes
- Método GetContentEnablersFromHashes Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetContentEnablersFromHashes
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747453"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="cc546-106">Método IWMDRMSecurity:: GetContentEnablersFromHashes</span><span class="sxs-lookup"><span data-stu-id="cc546-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="cc546-107">O método **GetContentEnablersFromHashes** recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados com hash.</span><span class="sxs-lookup"><span data-stu-id="cc546-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc546-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc546-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="cc546-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc546-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc546-110">*rgpbCertHashes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc546-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc546-111">Matriz de hashes de certificado para obter habilitadores de conteúdo para o.</span><span class="sxs-lookup"><span data-stu-id="cc546-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="cc546-112">*cCerts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc546-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc546-113">Número de certificados para os quais recuperar os habilitadores de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cc546-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="cc546-114">Este é o número de elementos na matriz *rgpbCertHashes* .</span><span class="sxs-lookup"><span data-stu-id="cc546-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="cc546-115">*hResultHint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="cc546-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc546-116">Valor de retorno recebido da operação que falhou devido a um certificado revogado.</span><span class="sxs-lookup"><span data-stu-id="cc546-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="cc546-117">Se você não estiver chamando em resposta a uma chamada de método com falha, defina para S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc546-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="cc546-118">*prgContentEnablers* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cc546-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc546-119">Matriz que recebe os endereços das interfaces **IMFContentEnabler** recém-criadas.</span><span class="sxs-lookup"><span data-stu-id="cc546-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="cc546-120">Defina como **NULL** para obter o número de habilitadores de conteúdo no parâmetro *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="cc546-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="cc546-121">*pcContentEnablers* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="cc546-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc546-122">Número de elementos na matriz *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="cc546-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="cc546-123">Se *prgContentEnablers* for **NULL**, esse valor será definido como o número de habilitadores de conteúdo necessários na saída.</span><span class="sxs-lookup"><span data-stu-id="cc546-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc546-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc546-124">Return value</span></span>

<span data-ttu-id="cc546-125">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="cc546-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cc546-126">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc546-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cc546-127">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc546-127">Return code</span></span>                                                                          | <span data-ttu-id="cc546-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc546-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cc546-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc546-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cc546-130">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="cc546-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cc546-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc546-131">Remarks</span></span>

<span data-ttu-id="cc546-132">Se você usar a interface **IMFContentEnabler** para renovar os componentes revogados, você deverá esclarecer o processo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="cc546-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="cc546-133">Esse esclarecimento deve ser feito porque o processo de atualização envia informações do computador cliente para um site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc546-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="cc546-134">Quando você chama **IMFContentEnabler:: AutomaticEnable**, o ativador de conteúdo inicia o navegador padrão com o endereço do serviço de atualização no site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc546-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="cc546-135">Um identificador exclusivo que identifica o componente revogado é enviado para o serviço de atualização.</span><span class="sxs-lookup"><span data-stu-id="cc546-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="cc546-136">Em seguida, o serviço redireciona o navegador para uma página da Web da qual o usuário poderá baixar e instalar a nova versão do componente revogado.</span><span class="sxs-lookup"><span data-stu-id="cc546-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc546-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc546-137">Requirements</span></span>



| <span data-ttu-id="cc546-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc546-138">Requirement</span></span> | <span data-ttu-id="cc546-139">Valor</span><span class="sxs-lookup"><span data-stu-id="cc546-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc546-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc546-140">Header</span></span><br/>  | <dl> <span data-ttu-id="cc546-141"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc546-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc546-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc546-142">Library</span></span><br/> | <dl> <span data-ttu-id="cc546-143"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc546-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc546-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc546-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc546-145">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="cc546-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





