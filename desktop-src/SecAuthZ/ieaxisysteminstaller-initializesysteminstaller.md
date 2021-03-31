---
description: Instala o objeto ActiveX especificado.
ms.assetid: c5d460d8-0df4-437a-a59e-707bf868a339
title: 'Método IeAxiSystemInstaller:: InitializeSystemInstaller'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiSystemInstaller.InitializeSystemInstaller
api_type:
- COM
api_location: ''
ms.openlocfilehash: 874bee80e23051d5dfdd22e259395293ae532619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829736"
---
# <a name="ieaxisysteminstallerinitializesysteminstaller-method"></a><span data-ttu-id="09fd7-103">Método IeAxiSystemInstaller:: InitializeSystemInstaller</span><span class="sxs-lookup"><span data-stu-id="09fd7-103">IeAxiSystemInstaller::InitializeSystemInstaller method</span></span>

<span data-ttu-id="09fd7-104">O método **InitializeSystemInstaller** instala o objeto ActiveX especificado.</span><span class="sxs-lookup"><span data-stu-id="09fd7-104">The **InitializeSystemInstaller** method installs the specified ActiveX object.</span></span>

## <a name="syntax"></a><span data-ttu-id="09fd7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09fd7-105">Syntax</span></span>


```C++
HRESULT InitializeSystemInstaller(
  [in]  BSTR     bstrUrl,
  [in]  DWORD    dwClientPID,
  [in]  IUnknown *pCallback,
  [out] BSTR     *pbstrNonce
);
```



## <a name="parameters"></a><span data-ttu-id="09fd7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09fd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09fd7-107">*bstrUrl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09fd7-107">*bstrUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fd7-108">A URL do objeto ActiveX a ser instalado.</span><span class="sxs-lookup"><span data-stu-id="09fd7-108">The URL of the ActiveX object to install.</span></span>

</dd> <dt>

<span data-ttu-id="09fd7-109">*dwClientPID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09fd7-109">*dwClientPID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fd7-110">A ID de processo do processo de chamada.</span><span class="sxs-lookup"><span data-stu-id="09fd7-110">The process ID of the calling process.</span></span>

</dd> <dt>

<span data-ttu-id="09fd7-111">*pCallback* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09fd7-111">*pCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09fd7-112">Um ponteiro para uma instância da interface [**IeAxiServiceCallback**](ieaxiservicecallback.md) que verifica se o objeto ActiveX tem permissão para ser instalado.</span><span class="sxs-lookup"><span data-stu-id="09fd7-112">A pointer to an instance of the [**IeAxiServiceCallback**](ieaxiservicecallback.md) interface that verifies whether the ActiveX object is allowed to be installed.</span></span>

</dd> <dt>

<span data-ttu-id="09fd7-113">*pbstrNonce* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09fd7-113">*pbstrNonce* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09fd7-114">Um contexto que pode ser usado para compartilhar informações de estado em chamadas para outros métodos usados para verificar e baixar o objeto ActiveX.</span><span class="sxs-lookup"><span data-stu-id="09fd7-114">A context that can be used to share state information in calls to other methods used to verify and download the ActiveX object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09fd7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09fd7-115">Return value</span></span>

<span data-ttu-id="09fd7-116">Se o método for bem sucedido, o método retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09fd7-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="09fd7-117">Se o método falhar, ele retornará um valor **HRESULT** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="09fd7-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="09fd7-118">Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="09fd7-118">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="09fd7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09fd7-119">Requirements</span></span>



| <span data-ttu-id="09fd7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="09fd7-120">Requirement</span></span> | <span data-ttu-id="09fd7-121">Valor</span><span class="sxs-lookup"><span data-stu-id="09fd7-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09fd7-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09fd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09fd7-123">Windows Vista Business, Windows Vista Enterprise, \[ somente aplicativos de área de trabalho do Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="09fd7-123">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="09fd7-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09fd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09fd7-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="09fd7-125">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="09fd7-126">IID</span><span class="sxs-lookup"><span data-stu-id="09fd7-126">IID</span></span><br/>                      | <span data-ttu-id="09fd7-127">IID \_ IeAxiSystemInstaller é definido como a50ea6f8-4764-4299-b309-022b2a8b4d8d</span><span class="sxs-lookup"><span data-stu-id="09fd7-127">IID\_IeAxiSystemInstaller is defined as a50ea6f8-4764-4299-b309-022b2a8b4d8d</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="09fd7-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="09fd7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09fd7-129">**IeAxiSystemInstaller**</span><span class="sxs-lookup"><span data-stu-id="09fd7-129">**IeAxiSystemInstaller**</span></span>](ieaxisysteminstaller.md)
</dt> </dl>

 

