---
title: Função CleanupCredentialCache
description: Implementado por determinados provedores de suporte de segurança (SSP) para liberar o cache de credenciais do SSP.
ms.assetid: e60870e6-22d3-4321-abca-a5b9d2b0ce2d
keywords:
- Função CleanupCredentialCache WinINet
topic_type:
- apiref
api_name:
- CleanupCredentialCache
api_location:
- MSNSSPC.dll
- MSAPSSPC.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53464073dd59837ba8026bbec03118055fba20cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085187"
---
# <a name="cleanupcredentialcache-function"></a><span data-ttu-id="9cb34-104">Função CleanupCredentialCache</span><span class="sxs-lookup"><span data-stu-id="9cb34-104">CleanupCredentialCache function</span></span>

<span data-ttu-id="9cb34-105">A função **CleanupCredentialCache** é implementada por determinados provedores de suporte de segurança (SSP) para liberar o cache de credenciais do SSP.</span><span class="sxs-lookup"><span data-stu-id="9cb34-105">The **CleanupCredentialCache** function is implemented by certain Security Support Providers (SSP) to flush the SSP credential cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cb34-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cb34-106">Syntax</span></span>


```C++
BOOL WINAPI CleanupCredentialCache(void);
```



## <a name="parameters"></a><span data-ttu-id="9cb34-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cb34-107">Parameters</span></span>

<span data-ttu-id="9cb34-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9cb34-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9cb34-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9cb34-109">Return value</span></span>

<span data-ttu-id="9cb34-110">**True** se a função for realizada com sucesso; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9cb34-110">**TRUE** if the function succeeds; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cb34-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="9cb34-111">Remarks</span></span>

<span data-ttu-id="9cb34-112">A função **CleanupCredentialCache** é implementada pelos seguintes SSPs:</span><span class="sxs-lookup"><span data-stu-id="9cb34-112">The **CleanupCredentialCache** function is implemented by the following SSPs:</span></span>

-   <span data-ttu-id="9cb34-113">MSNSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="9cb34-113">MSNSSPC.dll</span></span>
-   <span data-ttu-id="9cb34-114">MSAPSSPC.dll</span><span class="sxs-lookup"><span data-stu-id="9cb34-114">MSAPSSPC.dll</span></span>

<span data-ttu-id="9cb34-115">A implementação de **CleanupCredentialCache** por esses SSPs sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="9cb34-115">The implementation of **CleanupCredentialCache** by these SSPs always returns **TRUE**.</span></span>

<span data-ttu-id="9cb34-116">Antes de tentar obter um identificador de módulo para exportar **CleanupCredentialCache**, o aplicativo deve verificar se o SSP que foi carregado é um dos SSPs conhecidos que implementam a função **CleanupCredentialCache** .</span><span class="sxs-lookup"><span data-stu-id="9cb34-116">Before attempting to obtain a module handle to export **CleanupCredentialCache**, the application must verify that the SSP that has been loaded is one of the known SSPs implementing the **CleanupCredentialCache** function.</span></span>

<span data-ttu-id="9cb34-117">Para liberar o cache de credenciais do SSP, o aplicativo deve obter um identificador de módulo para o SSP chamando a função [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) .</span><span class="sxs-lookup"><span data-stu-id="9cb34-117">In order to flush the SSP credential cache, the application must obtain a module handle for the SSP by calling the [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) function.</span></span> <span data-ttu-id="9cb34-118">Depois de obter o módulo, o aplicativo deve exportar a função **CleanupCredentialCache** implementada pelo SSP chamando a função [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) , passando o módulo retornado por **GetModuleHandle** e **CleanupCredentialCache** como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="9cb34-118">After obtaining the module, the application should export the **CleanupCredentialCache** function implemented by the SSP by calling the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function, passing the module returned by **GetModuleHandle** and **CleanupCredentialCache** as input parameters.</span></span>

<span data-ttu-id="9cb34-119">Como todos os outros aspectos da API do WinINet, essa função não pode ser chamada com segurança de em DllMain ou os construtores e destruidores de objetos globais.</span><span class="sxs-lookup"><span data-stu-id="9cb34-119">Like all other aspects of the WinINet API, this function cannot be safely called from within DllMain or the constructors and destructors of global objects.</span></span>

> [!Note]  
> <span data-ttu-id="9cb34-120">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="9cb34-120">WinINet does not support server implementations.</span></span> <span data-ttu-id="9cb34-121">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="9cb34-121">In addition, it should not be used from a service.</span></span> <span data-ttu-id="9cb34-122">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="9cb34-122">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9cb34-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cb34-123">Requirements</span></span>



| <span data-ttu-id="9cb34-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cb34-124">Requirement</span></span> | <span data-ttu-id="9cb34-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9cb34-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cb34-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cb34-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9cb34-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9cb34-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                                 |
| <span data-ttu-id="9cb34-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cb34-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9cb34-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9cb34-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                       |
| <span data-ttu-id="9cb34-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9cb34-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cb34-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cb34-131"><dt>MSNSSPC.dll; </dt> <dt>MSAPSSPC.dll</dt></span></span> </dl> |



 

