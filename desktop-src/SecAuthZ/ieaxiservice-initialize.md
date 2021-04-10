---
description: Verifica e baixa um objeto ActiveX.
ms.assetid: a477c6dc-32a7-4d17-a997-6df4967d6c55
title: 'Método IeAxiService:: Initialize'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Initialize
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2b2e388f955c968220223519150fc4dc5b7af4a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171678"
---
# <a name="ieaxiserviceinitialize-method"></a><span data-ttu-id="76ce3-103">Método IeAxiService:: Initialize</span><span class="sxs-lookup"><span data-stu-id="76ce3-103">IeAxiService::Initialize method</span></span>

<span data-ttu-id="76ce3-104">O método **Initialize** verifica e baixa um objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="76ce3-104">The **Initialize** method checks and downloads an ActiveX object.</span></span> <span data-ttu-id="76ce3-105">Se o objeto atender aos requisitos da política, esse método inicializará um objeto do sistema que instala o objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="76ce3-105">If the object meets policy requirements, this method initializes a system object that installs the ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="76ce3-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76ce3-106">Syntax</span></span>


```C++
SECURITY_STATUS Initialize(
  [in]  HWND     hwndParent,
  [in]  DWORD    dwClientPID,
  [in]  BSTR     bstrDesktop,
  [in]  BSTR     bstrClsID,
  [in]  BSTR     bstrURL,
  [out] BSTR     *pbstrNonce,
  [out] IUnknown **ppISyncBrokerInterface
);
```



## <a name="parameters"></a><span data-ttu-id="76ce3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76ce3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76ce3-108">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-109">Um identificador para a janela pai da janela que está tentando instalar o controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="76ce3-109">A handle to the parent window of the window that is attempting to install the ActiveX control.</span></span>

</dd> <dt>

<span data-ttu-id="76ce3-110">*dwClientPID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-110">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-111">A ID de processo do processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="76ce3-111">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="76ce3-112">*bstrDesktop* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-112">*bstrDesktop* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-113">A área de trabalho para o objeto.</span><span class="sxs-lookup"><span data-stu-id="76ce3-113">The desktop for the object.</span></span>

</dd> <dt>

<span data-ttu-id="76ce3-114">*bstrClsID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-114">*bstrClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-115">A ID de classe do objeto ActiveX a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="76ce3-115">The class ID of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="76ce3-116">*bstrURL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-116">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-117">A URL do objeto ActiveX a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="76ce3-117">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="76ce3-118">*pbstrNonce* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-118">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-119">Um contexto que pode ser usado para compartilhar informações de estado em chamadas para outros métodos usados para verificar e baixar o objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="76ce3-119">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> <dt>

<span data-ttu-id="76ce3-120">*ppISyncBrokerInterface* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-120">*ppISyncBrokerInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76ce3-121">Um ponteiro para a instância da interface [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) que instala o controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="76ce3-121">A pointer to the instance of the [**IeAxiSystemInstaller**](ieaxisysteminstaller.md) interface that installs the ActiveX control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76ce3-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76ce3-122">Return value</span></span>

<span data-ttu-id="76ce3-123">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="76ce3-123">If the function succeeds, the return value is S\_OK.</span></span>

<span data-ttu-id="76ce3-124">Se a função falhar, o valor de retorno poderá ser um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="76ce3-124">If the function fails, the return value can be one of the following error codes.</span></span>



| <span data-ttu-id="76ce3-125">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="76ce3-125">Return code/value</span></span>                                                                                                                                                              | <span data-ttu-id="76ce3-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="76ce3-126">Description</span></span>                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="76ce3-127"><dt>**Confiar \_ E \_ assunto \_ não \_ confiável**</dt> <dt>0x800B0004</dt></span><span class="sxs-lookup"><span data-stu-id="76ce3-127"><dt>**TRUST\_E\_SUBJECT\_NOT\_TRUSTED**</dt> <dt>0x800B0004</dt></span></span> </dl> | <span data-ttu-id="76ce3-128">O objeto ActiveX não deve ser instalado.</span><span class="sxs-lookup"><span data-stu-id="76ce3-128">The ActiveX object should not be installed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="76ce3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76ce3-129">Requirements</span></span>



| <span data-ttu-id="76ce3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="76ce3-130">Requirement</span></span> | <span data-ttu-id="76ce3-131">Valor</span><span class="sxs-lookup"><span data-stu-id="76ce3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76ce3-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76ce3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="76ce3-133">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="76ce3-133">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="76ce3-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76ce3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="76ce3-135">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="76ce3-135">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="76ce3-136">IID</span><span class="sxs-lookup"><span data-stu-id="76ce3-136">IID</span></span><br/>                      | <span data-ttu-id="76ce3-137">IID \_ IeAxiService é definido como E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="76ce3-137">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="76ce3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="76ce3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76ce3-139">**IeAxiService**</span><span class="sxs-lookup"><span data-stu-id="76ce3-139">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

 




