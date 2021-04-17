---
title: Método IWMDRMLicenseManagement CleanLicenseStore (wmdrmsdk. h)
description: O método CleanLicenseStore remove licenças inutilizáveis do armazenamento de licença temporário e desfragmenta o armazenamento de licença local para melhorar o desempenho.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Formato de mídia do Windows do método CleanLicenseStore
- Método CleanLicenseStore Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método CleanLicenseStore
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785221"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="8645b-106">Método IWMDRMLicenseManagement:: CleanLicenseStore</span><span class="sxs-lookup"><span data-stu-id="8645b-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="8645b-107">O método **CleanLicenseStore** remove licenças inutilizáveis do armazenamento de licença temporário e desfragmenta o armazenamento de licença local para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8645b-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="8645b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8645b-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="8645b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8645b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8645b-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8645b-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8645b-111">Sinalizadores que especificam as opções de limpeza do repositório de licenças a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="8645b-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="8645b-112">Defina como uma das constantes na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8645b-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="8645b-113">Constante</span><span class="sxs-lookup"><span data-stu-id="8645b-113">Constant</span></span>                            | <span data-ttu-id="8645b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8645b-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8645b-115">\_sincronização de \_ armazenamento de licença de limpeza do WMDRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="8645b-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="8645b-116">A operação de limpeza será executada de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="8645b-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="8645b-117">Esse método não será retornado até que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="8645b-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="8645b-118">armazenamento de licença de limpeza do WMDRM \_ \_ \_ \_ assíncrono</span><span class="sxs-lookup"><span data-stu-id="8645b-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="8645b-119">A operação de limpeza será executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8645b-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="8645b-120">Esse método retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8645b-120">This method will return immediately.</span></span> <span data-ttu-id="8645b-121">Quando a operação for concluída, o evento de mídia MELicenseStoreCleaned será enviado.</span><span class="sxs-lookup"><span data-stu-id="8645b-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8645b-122">*ppunkCancelationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8645b-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8645b-123">Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8645b-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="8645b-124">Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="8645b-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8645b-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8645b-125">Return value</span></span>

<span data-ttu-id="8645b-126">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8645b-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8645b-127">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8645b-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8645b-128">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8645b-128">Return code</span></span>                                                                                            | <span data-ttu-id="8645b-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="8645b-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8645b-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8645b-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="8645b-131">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8645b-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="8645b-132"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="8645b-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="8645b-133">Não há nenhum repositório de licença temporário no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="8645b-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8645b-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="8645b-134">Remarks</span></span>

<span data-ttu-id="8645b-135">Esse método é executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8645b-135">This method executes asynchronously.</span></span> <span data-ttu-id="8645b-136">Ele retorna imediatamente depois de ser chamado e, em seguida, gera um evento **MEWMDRMLicenseStoreCleaned** quando o processamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="8645b-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="8645b-137">Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="8645b-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8645b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8645b-138">Requirements</span></span>



| <span data-ttu-id="8645b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="8645b-139">Requirement</span></span> | <span data-ttu-id="8645b-140">Valor</span><span class="sxs-lookup"><span data-stu-id="8645b-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8645b-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8645b-141">Header</span></span><br/>  | <dl> <span data-ttu-id="8645b-142"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8645b-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8645b-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8645b-143">Library</span></span><br/> | <dl> <span data-ttu-id="8645b-144"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8645b-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8645b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="8645b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8645b-146">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="8645b-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





