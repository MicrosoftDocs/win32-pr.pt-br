---
title: Método IWMDRMLicenseManagement BackupLicenses (wmdrmsdk. h)
description: O método BackupLicenses cria um backup das licenças no repositório de licenças local.
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- Formato de mídia do Windows do método BackupLicenses
- Método BackupLicenses Windows Media Format, interface IWMDRMLicenseManagement
- Formato de mídia do Windows de interface IWMDRMLicenseManagement, método BackupLicenses
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798176"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a><span data-ttu-id="23af4-106">Método IWMDRMLicenseManagement:: BackupLicenses</span><span class="sxs-lookup"><span data-stu-id="23af4-106">IWMDRMLicenseManagement::BackupLicenses method</span></span>

<span data-ttu-id="23af4-107">O método **BackupLicenses** cria um backup das licenças no repositório de licenças local.</span><span class="sxs-lookup"><span data-stu-id="23af4-107">The **BackupLicenses** method creates a backup of the licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="23af4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23af4-108">Syntax</span></span>


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="23af4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23af4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23af4-110">*bstrBackupDirectory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23af4-110">*bstrBackupDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23af4-111">Caminho UNC do local para o qual será feito o backup das licenças.</span><span class="sxs-lookup"><span data-stu-id="23af4-111">UNC path of the location to which the licenses will be backed up.</span></span>

</dd> <dt>

<span data-ttu-id="23af4-112">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23af4-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23af4-113">Sinalizadores que especificam as opções de backup a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="23af4-113">Flags specifying the backup options to use.</span></span> <span data-ttu-id="23af4-114">O único sinalizador com suporte no momento é a \_ substituição de backup do WMDRM \_ , que configura o método para substituir os arquivos de backup existentes no diretório.</span><span class="sxs-lookup"><span data-stu-id="23af4-114">The only flag currently supported is WMDRM\_BACKUP\_OVERWRITE, which configures the method to overwrite any existing backup files in the directory.</span></span>

</dd> <dt>

<span data-ttu-id="23af4-115">*ppunkCancelationCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="23af4-115">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23af4-116">Ponteiro que recebe um ponteiro para a interface **IUnknown** de um objeto que identifica essa chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="23af4-116">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="23af4-117">Esse ponteiro de interface pode ser usado para cancelar a chamada assíncrona chamando o método [**IWMDRMEventGenerator:: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .</span><span class="sxs-lookup"><span data-stu-id="23af4-117">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23af4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23af4-118">Return value</span></span>

<span data-ttu-id="23af4-119">O método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="23af4-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="23af4-120">Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="23af4-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="23af4-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="23af4-121">Return code</span></span>                                                                          | <span data-ttu-id="23af4-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="23af4-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="23af4-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="23af4-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="23af4-124">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="23af4-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="23af4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="23af4-125">Remarks</span></span>

<span data-ttu-id="23af4-126">Esse método é executado de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="23af4-126">This method executes asynchronously.</span></span> <span data-ttu-id="23af4-127">Ele retorna imediatamente depois de ser chamado e, em seguida, gera uma série de eventos **MEWMDRMLicenseBackupProgress** seguidos por um evento **MEWMDRMLicenseBackupCompleted** quando o processamento é concluído.</span><span class="sxs-lookup"><span data-stu-id="23af4-127">It returns immediately after being called and then generates a series of **MEWMDRMLicenseBackupProgress** events followed by an **MEWMDRMLicenseBackupCompleted** event when processing is complete.</span></span> <span data-ttu-id="23af4-128">O valor de cada um dos eventos **MEWMDRMLicenseBackupProgress** obtidos chamando **IMFMediaEvent:: GetValue** é um ponteiro **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="23af4-128">The value of each of the **MEWMDRMLicenseBackupProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="23af4-129">Você pode chamar o método **QueryInterface** da interface **IUnknown** recuperada para obter uma instância da interface [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="23af4-129">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interface.</span></span>

<span data-ttu-id="23af4-130">Para obter mais informações sobre como usar os métodos assíncronos das APIs estendidas do cliente DRM do Windows Media, consulte [usando o modelo de evento Media Foundation](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="23af4-130">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

<span data-ttu-id="23af4-131">Nem todas as licenças têm permissão para fazer backup.</span><span class="sxs-lookup"><span data-stu-id="23af4-131">Not all licenses are permitted to be backed up.</span></span> <span data-ttu-id="23af4-132">Esse método faz backup apenas de licenças que o permitem.</span><span class="sxs-lookup"><span data-stu-id="23af4-132">This method only backs up licenses that allow it.</span></span>

## <a name="requirements"></a><span data-ttu-id="23af4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23af4-133">Requirements</span></span>



| <span data-ttu-id="23af4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="23af4-134">Requirement</span></span> | <span data-ttu-id="23af4-135">Valor</span><span class="sxs-lookup"><span data-stu-id="23af4-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23af4-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23af4-136">Header</span></span><br/>  | <dl> <span data-ttu-id="23af4-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="23af4-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="23af4-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="23af4-138">Library</span></span><br/> | <dl> <span data-ttu-id="23af4-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23af4-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23af4-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="23af4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23af4-141">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="23af4-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





