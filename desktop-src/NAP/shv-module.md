---
title: Módulo SHV
description: 'Observação: a plataforma de proteção de acesso à rede não está disponível a partir do Windows 10 configura um módulo de validador da integridade do sistema (SHV), incluindo registro e cancelamento de registro com o sistema NAP.'
ms.assetid: 0f2edd23-d44a-4a01-ae33-f7eef0e4b27f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95784d05f4bf377f356a91fe5b0c1811fb9671d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635667"
---
# <a name="shv-module"></a><span data-ttu-id="7189f-103">Módulo SHV</span><span class="sxs-lookup"><span data-stu-id="7189f-103">SHV Module</span></span>

> [!Note]  
> <span data-ttu-id="7189f-104">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="7189f-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7189f-105">Configura um módulo de validador da integridade do sistema (SHV), incluindo o registro e o cancelamento de registro com o sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="7189f-105">Sets up a system health validator (SHV) module including registration and unregistration with the NAP system.</span></span>

> [!Note]  
> <span data-ttu-id="7189f-106">O SDK do NAP também contém um conjunto completo de códigos de exemplo que podem ser encontrados no. \\ .. Exemplos \\ de \\ NAP NetDS... diretório da instalação do SDK.</span><span class="sxs-lookup"><span data-stu-id="7189f-106">The NAP SDK also contains a full set of sample code that can be found in the ...\\Samples\\NetDS\\NAP... directory of your SDK installation.</span></span> <span data-ttu-id="7189f-107">Este conjunto de amostras inclui um SHA (agente de integridade do sistema), SHV e cliente de imposição (EC).</span><span class="sxs-lookup"><span data-stu-id="7189f-107">This sample set includes a system health agent (SHA), SHV, and enforcement client (EC).</span></span> <span data-ttu-id="7189f-108">Ele tem cenários NAP de trabalho completo Configurando a comunicação entre SHA-SHV e SHA-EC.</span><span class="sxs-lookup"><span data-stu-id="7189f-108">It has full working NAP scenarios setting up communication between SHA-SHV and SHA-EC.</span></span>

 


```C++
#include <windows.h>
#include "stdafx.h"
#include "NapUtil.h"

static const wchar_t friendlyName[] = L"SDK SHV Sample";
static const wchar_t version[] = L"1.0.0.1";
static const wchar_t description[] = L"System Health Validator(SHV)";
static const wchar_t vendor[] = L"Microsoft";

/// Registers the SDK SHV with the NAP Server.
HRESULT RegisterSdkShv()
{
    HRESULT hr = S_OK;
    CComPtr<INapServerManagement> pSHVMgmt = NULL;
    
    NapComponentRegistrationInfo shvInfo;
    ZeroMemory (&shvInfo, sizeof(shvInfo));

    hr = pSHVMgmt.CoCreateInstance(CLSID_NapServerManagement, NULL, CLSCTX_INPROC_SERVER);
    hr = FillShvComponentRegistrationInfo(&shvInfo);
    hr = pSHVMgmt->RegisterSystemHealthValidator(&shvInfo, (CLSID *)&__uuidof(CSampleShv));
    
    FreeComponentRegistration(&shvInfo);
    return hr;
}

/// Unregisters the SDK SHV with the NAP Server.
HRESULT UnregisterSdkShv()
{
    HRESULT hr = S_OK;
    CComPtr<INapServerManagement> pSHVMgmt = NULL;

    hr = pSHVMgmt.CoCreateInstance(CLSID_NapServerManagement, NULL, CLSCTX_INPROC_SERVER);
    hr = pSHVMgmt->UnregisterSystemHealthValidator(QuarSampleSystemHealthId);
    return hr;
}

/// Fill the NapComponentRegistrationInfo structure that needs to be passed during registration.
HRESULT FillShvComponentRegistrationInfo (NapComponentRegistrationInfo *shvInfo)
{
    HRESULT hr = S_OK;
    shvInfo->id = QuarSampleSystemHealthId;

    //<Temporarily till implement the Info Class>
    shvInfo->infoClsid = GUID_NULL; 

    hr = ConstructCountedString(friendlyName, sizeof(friendlyName), &(shvInfo->friendlyName));
    hr = ConstructCountedString(description, sizeof(description), &(shvInfo->description));
    hr = ConstructCountedString(version, sizeof(version), &(shvInfo->version));
    hr = ConstructCountedString(vendor, sizeof(vendor), &(shvInfo->vendorName));
    return hr;
}

// Helper Function for FillShvComponentRegistrationInfo.
HRESULT ConstructCountedString(const WCHAR* src, UINT16 len, CountedString* dest)
{
    HRESULT hr = S_OK;
    DWORD retCode = ERROR_SUCCESS;
    hr = AllocateMemory(dest->string, ((len+1)*sizeof(WCHAR)));
    dest->length = len;
    retCode = StringCchCopy(dest->string, len+1, src);
    return hr;
}

// Helper Function for releasing ShaComponentRegistrationInfo members
void FreeComponentRegistration(NapComponentRegistrationInfo *shvInfo)
{
    FreeMemory(shvInfo->friendlyName.string);
    FreeMemory(shvInfo->description.string);
    FreeMemory(shvInfo->version.string);
    FreeMemory(shvInfo->vendorName.string);
}

```



 

 




