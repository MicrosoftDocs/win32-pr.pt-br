---
title: Método IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: O método GetContentEnablersForRevocations recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados revogados.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Formato de mídia do Windows do método GetContentEnablersForRevocations
- Método GetContentEnablersForRevocations Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747454"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="a37b0-106">Método IWMDRMSecurity:: GetContentEnablersForRevocations</span><span class="sxs-lookup"><span data-stu-id="a37b0-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="a37b0-107">O método **GetContentEnablersForRevocations** recupera as interfaces de habilitação de conteúdo que habilitam a renovação de componentes com base em certificados revogados.</span><span class="sxs-lookup"><span data-stu-id="a37b0-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a37b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a37b0-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="a37b0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a37b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a37b0-110">*rgpbCerts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-111">Matriz de certificados para recuperar habilitadores de conteúdo para o.</span><span class="sxs-lookup"><span data-stu-id="a37b0-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="a37b0-112">O número de elementos na matriz deve ser especificado por *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="a37b0-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="a37b0-113">*rgpdwCertSizes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-114">Matriz que contém os tamanhos dos certificados na matriz *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="a37b0-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="a37b0-115">O número de elementos na matriz deve ser especificado por *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="a37b0-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="a37b0-116">*rgpguidCerts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-117">Matriz que contém os tipos de certificados na matriz *rgpbCerts* .</span><span class="sxs-lookup"><span data-stu-id="a37b0-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="a37b0-118">O número de elementos na matriz deve ser especificado por *cCerts*.</span><span class="sxs-lookup"><span data-stu-id="a37b0-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="a37b0-119">Para cada elemento da matriz, use um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a37b0-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="a37b0-120">Constante de GUID</span><span class="sxs-lookup"><span data-stu-id="a37b0-120">GUID constant</span></span>                 | <span data-ttu-id="a37b0-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="a37b0-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="a37b0-122">\_aplicativo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="a37b0-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="a37b0-123">Especifica um certificado de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a37b0-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="a37b0-124">\_dispositivo WMDRM RErevocationtype \_</span><span class="sxs-lookup"><span data-stu-id="a37b0-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="a37b0-125">Especifica um certificado de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a37b0-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="a37b0-126">WMDRM \_ RErevocationtype \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="a37b0-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="a37b0-127">Especifica um certificado de Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="a37b0-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="a37b0-128">*cCerts* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-129">Número de certificados para os quais recuperar os habilitadores de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a37b0-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="a37b0-130">Esse é o número de elementos na matriz *rgpbCerts* , a matriz *rgpdwCertSizes* e a matriz *rgpguidCerts* .</span><span class="sxs-lookup"><span data-stu-id="a37b0-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="a37b0-131">*hResultHint* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-132">Valor de retorno recebido da operação que falhou devido a um certificado revogado.</span><span class="sxs-lookup"><span data-stu-id="a37b0-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="a37b0-133">Se você não estiver chamando em resposta a uma chamada de método com falha, defina para S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a37b0-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="a37b0-134">*prgContentEnablers* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-135">Matriz que recebe os endereços das interfaces **IMFContentEnabler** recém-criadas.</span><span class="sxs-lookup"><span data-stu-id="a37b0-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="a37b0-136">Defina como **NULL** para obter o número de habilitadores de conteúdo no parâmetro *pcContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="a37b0-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a37b0-137">*pcContentEnablers* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a37b0-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a37b0-138">Número de elementos na matriz *prgContentEnablers* .</span><span class="sxs-lookup"><span data-stu-id="a37b0-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="a37b0-139">Se *prgContentEnablers* for **NULL**, esse valor será definido como o número de habilitadores de conteúdo necessários na saída.</span><span class="sxs-lookup"><span data-stu-id="a37b0-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a37b0-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a37b0-140">Return value</span></span>

<span data-ttu-id="a37b0-141">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a37b0-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a37b0-142">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a37b0-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a37b0-143">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a37b0-143">Return code</span></span>                                                                          | <span data-ttu-id="a37b0-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="a37b0-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a37b0-145"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a37b0-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a37b0-146">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="a37b0-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a37b0-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="a37b0-147">Remarks</span></span>

<span data-ttu-id="a37b0-148">Se você usar a interface **IMFContentEnabler** para renovar os componentes revogados, você deverá esclarecer o processo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="a37b0-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="a37b0-149">Esse esclarecimento deve ser feito porque o processo de atualização envia informações do computador cliente para um site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a37b0-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="a37b0-150">Quando você chama **IMFContentEnabler:: AutomaticEnable**, o ativador de conteúdo inicia o navegador padrão com o endereço do serviço de atualização no site da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a37b0-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="a37b0-151">Um identificador exclusivo que identifica o componente revogado é enviado para o serviço de atualização.</span><span class="sxs-lookup"><span data-stu-id="a37b0-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="a37b0-152">Em seguida, o serviço redireciona o navegador para uma página da Web da qual o usuário poderá baixar e instalar a nova versão do componente revogado.</span><span class="sxs-lookup"><span data-stu-id="a37b0-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="a37b0-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a37b0-153">Requirements</span></span>



| <span data-ttu-id="a37b0-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="a37b0-154">Requirement</span></span> | <span data-ttu-id="a37b0-155">Valor</span><span class="sxs-lookup"><span data-stu-id="a37b0-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a37b0-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a37b0-156">Header</span></span><br/>  | <dl> <span data-ttu-id="a37b0-157"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a37b0-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a37b0-158">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a37b0-158">Library</span></span><br/> | <dl> <span data-ttu-id="a37b0-159"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a37b0-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a37b0-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="a37b0-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a37b0-161">**Revogação e renovação de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="a37b0-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="a37b0-162">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="a37b0-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





