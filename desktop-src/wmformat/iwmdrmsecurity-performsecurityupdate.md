---
title: Método IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: O método PerformSecurityUpdate inicia uma atualização de segurança para o subsistema DRM no computador local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Formato de mídia do Windows do método PerformSecurityUpdate
- Método PerformSecurityUpdate Windows Media Format, interface IWMDRMSecurity
- Formato de mídia do Windows de interface IWMDRMSecurity, método PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782609"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="2044a-106">IWMDRMSecurity: método erformSecurityUpdate de:P</span><span class="sxs-lookup"><span data-stu-id="2044a-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="2044a-107">O método **PerformSecurityUpdate** inicia uma atualização de segurança para o subsistema DRM no computador local.</span><span class="sxs-lookup"><span data-stu-id="2044a-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2044a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2044a-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="2044a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2044a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2044a-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2044a-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2044a-111">Opção de atualização expressa como um dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2044a-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="2044a-112">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="2044a-112">Flag</span></span>                                          | <span data-ttu-id="2044a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2044a-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2044a-114">segurança do WMDRM \_ \_ executar \_ indiv</span><span class="sxs-lookup"><span data-stu-id="2044a-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="2044a-115">Faz com que o componente DRM seja individualizado somente se a versão do cliente estiver desatualizada.</span><span class="sxs-lookup"><span data-stu-id="2044a-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="2044a-116">segurança do WMDRM \_ \_ executar \_ atualização de revogação \_</span><span class="sxs-lookup"><span data-stu-id="2044a-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="2044a-117">Faz com que as listas de revogação no computador cliente sejam atualizadas.</span><span class="sxs-lookup"><span data-stu-id="2044a-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="2044a-118">segurança do WMDRM \_ \_ executar \_ forçar \_ indiv</span><span class="sxs-lookup"><span data-stu-id="2044a-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="2044a-119">Faz com que o componente DRM seja individualizado mesmo que a versão do cliente esteja atualizada.</span><span class="sxs-lookup"><span data-stu-id="2044a-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2044a-120">*ppunkCancelationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2044a-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2044a-121">Endereço de uma variável que recebe um ponteiro para um objeto que pode ser usado para cancelar esta operação.</span><span class="sxs-lookup"><span data-stu-id="2044a-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2044a-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2044a-122">Return value</span></span>

<span data-ttu-id="2044a-123">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2044a-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2044a-124">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2044a-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2044a-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2044a-125">Return code</span></span>                                                                          | <span data-ttu-id="2044a-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="2044a-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="2044a-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2044a-128">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="2044a-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2044a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="2044a-129">Remarks</span></span>

<span data-ttu-id="2044a-130">Esse método é executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2044a-130">This method executes asynchronously.</span></span> <span data-ttu-id="2044a-131">Ele retorna imediatamente depois de ser chamado e, em seguida, gera eventos dependendo do sinalizador definido no parâmetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="2044a-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="2044a-132">Para individualização (sinalizador definido como \_ segurança WMDRM \_ Execute \_ indiv ou WMDRM \_ Security \_ Execute \_ Force \_ indiv), uma série de eventos **MEWMDRMIndividualizationProgress** é gerada seguida por um evento **MEWMDRMIndividualizationCompleted** quando o processamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="2044a-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="2044a-133">O valor de cada um dos eventos **MEWMDRMIndividualizationProgress** obtidos chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="2044a-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="2044a-134">Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="2044a-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="2044a-135">Para atualizar as listas de revogação (sinalizador definido como WMDRM \_ Security \_ perform \_ Revocation \_ Refresh), um evento **MEWMDRMREvocationDownloadCompleted** é gerado quando o processamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="2044a-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="2044a-136">Quando o **PerformSecurityUpdate** conclui a individualização, os únicos objetos existentes que refletirão o novo estado individual são aqueles que herdam de **IWMDRMSecurity**.</span><span class="sxs-lookup"><span data-stu-id="2044a-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="2044a-137">Todos os outros objetos existentes não serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="2044a-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="2044a-138">Você deve liberar e recriar outros objetos para que eles reflitam o novo estado individual.</span><span class="sxs-lookup"><span data-stu-id="2044a-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="2044a-139">Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="2044a-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2044a-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2044a-140">Requirements</span></span>



| <span data-ttu-id="2044a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2044a-141">Requirement</span></span> | <span data-ttu-id="2044a-142">Valor</span><span class="sxs-lookup"><span data-stu-id="2044a-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2044a-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2044a-143">Header</span></span><br/>  | <dl> <span data-ttu-id="2044a-144"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="2044a-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2044a-145">Library</span></span><br/> | <dl> <span data-ttu-id="2044a-146"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2044a-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2044a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="2044a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2044a-148">**Revogação e renovação de componentes automatizados**</span><span class="sxs-lookup"><span data-stu-id="2044a-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="2044a-149">**Exemplo de individualização de DRM**</span><span class="sxs-lookup"><span data-stu-id="2044a-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="2044a-150">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="2044a-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="2044a-151">**Executando individualização de DRM**</span><span class="sxs-lookup"><span data-stu-id="2044a-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





