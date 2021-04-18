---
title: Método AcquireLicense IWMDRMLicenseManagement (wmdrmsdk. h)
description: O método AcquireLicense adquire de forma assíncrona uma licença de uma URL especificada.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- Método AcquireLicense Windows Media Format
- Método AcquireLicense Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows da interface IWMDRMLicenseManagement, método AcquireLicense
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793273"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="53f94-106">Método IWMDRMLicenseManagement:: AcquireLicense</span><span class="sxs-lookup"><span data-stu-id="53f94-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="53f94-107">O método **AcquireLicense** adquire de forma assíncrona uma licença de uma URL especificada.</span><span class="sxs-lookup"><span data-stu-id="53f94-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f94-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53f94-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="53f94-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53f94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f94-110">*bstrURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53f94-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f94-111">URL do servidor de licença do qual a licença será adquirida.</span><span class="sxs-lookup"><span data-stu-id="53f94-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="53f94-112">Passe **NULL** para que o método analise a URL do cabeçalho de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="53f94-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="53f94-113">*bstrHeaderData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53f94-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f94-114">Cabeçalho de conteúdo a ser passado para o servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="53f94-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="53f94-115">Se *bstrURL* for **NULL**, o método analisará a URL desse cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="53f94-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="53f94-116">Se *dwFlags* estiver definido como WMDRM \_ adquirir \_ licença \_ herdada \_ não silenciosa, defina esse valor como a ID da chave em vez de todo o cabeçalho do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="53f94-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="53f94-117">*bstrActions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53f94-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f94-118">Cadeia de caracteres que contém zero ou mais ações para as quais solicitar permissão na licença.</span><span class="sxs-lookup"><span data-stu-id="53f94-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="53f94-119">A cadeia de caracteres deve ser formatada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53f94-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="53f94-120">Cada ação deve ser definida dentro de um elemento ACTION.</span><span class="sxs-lookup"><span data-stu-id="53f94-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="53f94-121">Os dados do elemento são a cadeia de caracteres de ação.</span><span class="sxs-lookup"><span data-stu-id="53f94-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="53f94-122">Todos os elementos de ação devem estar contidos em um elemento ACTIONlist.</span><span class="sxs-lookup"><span data-stu-id="53f94-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="53f94-123">Por exemplo, a cadeia de caracteres para solicitar uma licença para reproduzir conteúdo é formatada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="53f94-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="53f94-124">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="53f94-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53f94-125">Sinalizadores de opção de aquisição de licença.</span><span class="sxs-lookup"><span data-stu-id="53f94-125">License acquisition option flags.</span></span> <span data-ttu-id="53f94-126">Defina como uma das constantes na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="53f94-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="53f94-127">Constante</span><span class="sxs-lookup"><span data-stu-id="53f94-127">Constant</span></span>                                   | <span data-ttu-id="53f94-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="53f94-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f94-129">licença de aquisição do WMDRM \_ \_ \_ silenciosa</span><span class="sxs-lookup"><span data-stu-id="53f94-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="53f94-130">A licença será emitida diretamente pela Internet sem nenhuma confirmação do aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="53f94-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="53f94-131">licença de aquisição de WMDRM não \_ \_ \_ silenciosa</span><span class="sxs-lookup"><span data-stu-id="53f94-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="53f94-132">O subsistema DRM criará uma solicitação de licença que será retornada de forma assíncrona para o lançamento no servidor de licença.</span><span class="sxs-lookup"><span data-stu-id="53f94-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="53f94-133">WMDRM \_ adquirir \_ licença \_ HERDAda não \_ silenciosa</span><span class="sxs-lookup"><span data-stu-id="53f94-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="53f94-134">O mesmo que o WMDRM \_ adquire a \_ licença \_ não silenciosa, exceto que um desafio de licença do DRM versão 1 será criado.</span><span class="sxs-lookup"><span data-stu-id="53f94-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="53f94-135">*ppunkCancelationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="53f94-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53f94-136">Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="53f94-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="53f94-137">Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="53f94-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53f94-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53f94-138">Return value</span></span>

<span data-ttu-id="53f94-139">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="53f94-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="53f94-140">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="53f94-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="53f94-141">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="53f94-141">Return code</span></span>                                                                          | <span data-ttu-id="53f94-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="53f94-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="53f94-143"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53f94-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="53f94-144">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="53f94-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53f94-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="53f94-145">Remarks</span></span>

<span data-ttu-id="53f94-146">Esse método é executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="53f94-146">This method executes asynchronously.</span></span> <span data-ttu-id="53f94-147">Ele retorna imediatamente depois de ser chamado e, em seguida, gera um evento **MEWMDRMLicenseAcquisitionCompleted** quando o processamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="53f94-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="53f94-148">Para operações de aquisição de licença não silenciosa, o valor do evento obtido chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="53f94-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="53f94-149">Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .</span><span class="sxs-lookup"><span data-stu-id="53f94-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="53f94-150">Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="53f94-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53f94-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53f94-151">Requirements</span></span>



| <span data-ttu-id="53f94-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f94-152">Requirement</span></span> | <span data-ttu-id="53f94-153">Valor</span><span class="sxs-lookup"><span data-stu-id="53f94-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53f94-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53f94-154">Header</span></span><br/>  | <dl> <span data-ttu-id="53f94-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f94-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="53f94-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53f94-156">Library</span></span><br/> | <dl> <span data-ttu-id="53f94-157"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53f94-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f94-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="53f94-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f94-159">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="53f94-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="53f94-160">**Aquisição de licença silenciosa**</span><span class="sxs-lookup"><span data-stu-id="53f94-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 





