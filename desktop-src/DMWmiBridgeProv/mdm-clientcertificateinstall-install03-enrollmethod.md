---
title: Método EnrollMethod da classe MDM_ClientCertificateInstall_Install03
description: Dispara o dispositivo para iniciar o registro de certificado.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Método EnrollMethod
- Método EnrollMethod, classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, método EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644934"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="27512-106">Método EnrollMethod da \_ classe Install03 do MDM ClientCertificateInstall \_</span><span class="sxs-lookup"><span data-stu-id="27512-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="27512-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="27512-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="27512-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="27512-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="27512-109">Dispara o dispositivo para iniciar o registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="27512-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="27512-110">O dispositivo não notificará o servidor MDM após a conclusão do registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="27512-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="27512-111">O servidor MDM pode consultar o dispositivo posteriormente para descobrir se o novo certificado foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="27512-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="27512-112">Consulte também [**registrar**](/windows/client-management/mdm/clientcertificateinstall-csp).</span><span class="sxs-lookup"><span data-stu-id="27512-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="27512-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27512-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="27512-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27512-114">Parameters</span></span>

<span data-ttu-id="27512-115">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="27512-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="27512-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27512-116">Return value</span></span>

<span data-ttu-id="27512-117">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="27512-117">Required.</span></span> <span data-ttu-id="27512-118">Dispara o dispositivo para iniciar o registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="27512-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="27512-119">O dispositivo não notificará o servidor MDM após a conclusão do registro de certificado.</span><span class="sxs-lookup"><span data-stu-id="27512-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="27512-120">O servidor MDM pode consultar o dispositivo posteriormente para descobrir se o novo certificado foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="27512-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="27512-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27512-121">Requirements</span></span>



| <span data-ttu-id="27512-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="27512-122">Requirement</span></span> | <span data-ttu-id="27512-123">Valor</span><span class="sxs-lookup"><span data-stu-id="27512-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27512-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27512-124">Minimum supported client</span></span><br/> | <span data-ttu-id="27512-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="27512-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27512-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27512-126">Minimum supported server</span></span><br/> | <span data-ttu-id="27512-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="27512-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="27512-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="27512-128">Namespace</span></span><br/>                | <span data-ttu-id="27512-129">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="27512-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="27512-130">MOF</span><span class="sxs-lookup"><span data-stu-id="27512-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27512-131"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27512-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="27512-132">DLL</span><span class="sxs-lookup"><span data-stu-id="27512-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27512-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27512-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27512-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="27512-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27512-135">**\_Install03 CLIENTCERTIFICATEINSTALL \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="27512-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="27512-136">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="27512-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

