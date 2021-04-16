---
title: Método IWMDRMLicenseManagement RestoreLicenses (wmdrmsdk. h)
description: O método RestoreLicenses restaura licenças de um backup de licença que foi criado chamando o método BackupLicenses.
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- Formato de mídia do Windows do método RestoreLicenses
- Método RestoreLicenses Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método RestoreLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb07f3989ff19faa723e4b1d1cd50dc4e269f219
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765035"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a><span data-ttu-id="37044-106">Método IWMDRMLicenseManagement:: RestoreLicenses</span><span class="sxs-lookup"><span data-stu-id="37044-106">IWMDRMLicenseManagement::RestoreLicenses method</span></span>

<span data-ttu-id="37044-107">O método **RestoreLicenses** restaura licenças de um backup de licença que foi criado chamando o método [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) .</span><span class="sxs-lookup"><span data-stu-id="37044-107">The **RestoreLicenses** method restores licenses from a license backup that was created by calling the [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37044-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37044-108">Syntax</span></span>


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="37044-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37044-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37044-110">*bstrBackupDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37044-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37044-111">Caminho UNC do local do qual as licenças serão restauradas.</span><span class="sxs-lookup"><span data-stu-id="37044-111">UNC path of the location from which the licenses will be restored.</span></span>

</dd> <dt>

<span data-ttu-id="37044-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="37044-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37044-113">Sinalizadores que especificam as opções de restauração a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="37044-113">Flags specifying the restore options to use.</span></span> <span data-ttu-id="37044-114">O único sinalizador com suporte no momento é o WMDRM \_ Restore \_ individual, que configura o método para executar individualização como parte da restauração, se necessário.</span><span class="sxs-lookup"><span data-stu-id="37044-114">The only flag currently supported is WMDRM\_RESTORE\_INDIVIDUALIZE, which configures the method to perform individualization as part of the restoration, if required.</span></span>

</dd> <dt>

<span data-ttu-id="37044-115">*ppunkCancelationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="37044-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37044-116">Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="37044-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="37044-117">Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="37044-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37044-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37044-118">Return value</span></span>

<span data-ttu-id="37044-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="37044-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="37044-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="37044-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="37044-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="37044-121">Return code</span></span>                                                                          | <span data-ttu-id="37044-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="37044-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="37044-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="37044-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="37044-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="37044-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="37044-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="37044-125">Remarks</span></span>

<span data-ttu-id="37044-126">Esse método é executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="37044-126">This method executes asynchronously.</span></span> <span data-ttu-id="37044-127">Ele retorna imediatamente depois de ser chamado e, em seguida, gera uma série de eventos **MEWMDRMLicenseRestoreProgress** seguidos por um evento **MEWMDRMLicenseRestoreCompleted** quando o processamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="37044-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseRestoreProgress** events followed by an **MEWMDRMLicenseRestoreCompleted** event when processing is complete.</span></span> <span data-ttu-id="37044-128">O valor de cada um dos eventos **MEWMDRMLicenseRestoreProgress** obtidos chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="37044-128">The value of each of the **MEWMDRMLicenseRestoreProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="37044-129">Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="37044-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="37044-130">Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="37044-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="37044-131">O backup pode ser do computador local ou de um computador diferente.</span><span class="sxs-lookup"><span data-stu-id="37044-131">The backup can be from the local machine or from a different machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="37044-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37044-132">Requirements</span></span>



| <span data-ttu-id="37044-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="37044-133">Requirement</span></span> | <span data-ttu-id="37044-134">Valor</span><span class="sxs-lookup"><span data-stu-id="37044-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="37044-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37044-135">Header</span></span><br/>  | <dl> <span data-ttu-id="37044-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="37044-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="37044-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37044-137">Library</span></span><br/> | <dl> <span data-ttu-id="37044-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37044-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37044-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="37044-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37044-140">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="37044-140">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





