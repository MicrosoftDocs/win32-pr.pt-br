---
title: Função DDCCIGetCapabilitiesString
description: Obtém uma cadeia de caracteres que descreve os recursos de um monitor.
ms.assetid: 54041126-b710-4448-a9f0-9b644d6b8186
keywords:
- Configuração do monitor de função DDCCIGetCapabilitiesString
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesString
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a49a6d7672ee505b4095afd3c6603c719679f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750830"
---
# <a name="ddccigetcapabilitiesstring-function"></a><span data-ttu-id="204c6-104">Função DDCCIGetCapabilitiesString</span><span class="sxs-lookup"><span data-stu-id="204c6-104">DDCCIGetCapabilitiesString function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="204c6-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="204c6-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="204c6-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="204c6-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="204c6-107">Obtém uma cadeia de caracteres que descreve os recursos de um monitor.</span><span class="sxs-lookup"><span data-stu-id="204c6-107">Gets a string that describes the capabilities of a monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="204c6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="204c6-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesString(
  _In_  HANDLE hMonitor,
  _Out_ LPSTR  pszString,
  _In_  DWORD  dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="204c6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="204c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="204c6-110">*HMONITOR* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="204c6-110">*hMonitor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="204c6-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="204c6-111">A handle to a physical monitor.</span></span>

</dd> <dt>

<span data-ttu-id="204c6-112">*pszString* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="204c6-112">*pszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="204c6-113">Um ponteiro para um buffer que recebe a cadeia de caracteres de recursos.</span><span class="sxs-lookup"><span data-stu-id="204c6-113">A pointer to a buffer that receives the capabilities string.</span></span> <span data-ttu-id="204c6-114">Para obter o comprimento da cadeia de caracteres de recursos, chame [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span><span class="sxs-lookup"><span data-stu-id="204c6-114">To get the length of the capabilities string, call [**DDCCIGetCapabilitiesStringLength**](ddccigetcapabilitiesstringlength.md).</span></span>

</dd> <dt>

<span data-ttu-id="204c6-115">*dwLength* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="204c6-115">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="204c6-116">O tamanho do buffer *pszString* , em caracteres, incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="204c6-116">The size of the *pszString* buffer, in characters, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="204c6-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="204c6-117">Return value</span></span>

<span data-ttu-id="204c6-118">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="204c6-118">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="204c6-119">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="204c6-119">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="204c6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="204c6-120">Remarks</span></span>

<span data-ttu-id="204c6-121">Os aplicativos devem chamar [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="204c6-121">Applications should call [**CapabilitiesRequestAndCapabilitiesReply**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-capabilitiesrequestandcapabilitiesreply) instead of calling this function.</span></span>

<span data-ttu-id="204c6-122">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="204c6-122">This function has no associated import library.</span></span> <span data-ttu-id="204c6-123">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="204c6-123">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="204c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="204c6-124">Requirements</span></span>



| <span data-ttu-id="204c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="204c6-125">Requirement</span></span> | <span data-ttu-id="204c6-126">Valor</span><span class="sxs-lookup"><span data-stu-id="204c6-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="204c6-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="204c6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="204c6-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="204c6-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="204c6-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="204c6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="204c6-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="204c6-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="204c6-131">DLL</span><span class="sxs-lookup"><span data-stu-id="204c6-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="204c6-132"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="204c6-132"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="204c6-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="204c6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="204c6-134">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="204c6-134">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

