---
title: Função DDCCISaveCurrentSettings
description: Salva as configurações atuais do monitor no armazenamento não volátil da exibição.
ms.assetid: 293b61d4-36d8-43f4-8800-4dbac3ab11b0
keywords:
- Configuração do monitor de função DDCCISaveCurrentSettings
topic_type:
- apiref
api_name:
- DDCCISaveCurrentSettings
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de590f63acc11ed49dfcdfab6505733da07b508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918250"
---
# <a name="ddccisavecurrentsettings-function"></a><span data-ttu-id="49278-104">Função DDCCISaveCurrentSettings</span><span class="sxs-lookup"><span data-stu-id="49278-104">DDCCISaveCurrentSettings function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49278-105">Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="49278-105">This function is used by the monitor configuration API to access functionality in the display driver.</span></span> <span data-ttu-id="49278-106">Os aplicativos não devem chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="49278-106">Applications should not call this function.</span></span>

 

<span data-ttu-id="49278-107">Salva as configurações atuais do monitor no armazenamento não volátil da exibição.</span><span class="sxs-lookup"><span data-stu-id="49278-107">Saves the current monitor settings to the display's nonvolatile storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="49278-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49278-108">Syntax</span></span>


```C++
NTSTATUS WINAPI DDCCISaveCurrentSettings(
   HANDLE hMonitor
);
```



## <a name="parameters"></a><span data-ttu-id="49278-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49278-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49278-110">*hMonitor*</span><span class="sxs-lookup"><span data-stu-id="49278-110">*hMonitor*</span></span> 
</dt> <dd>

<span data-ttu-id="49278-111">Um identificador para um monitor físico.</span><span class="sxs-lookup"><span data-stu-id="49278-111">A handle to a physical monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49278-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49278-112">Return value</span></span>

<span data-ttu-id="49278-113">Se o método for bem-sucedido, ele retornará o **status \_ êxito**.</span><span class="sxs-lookup"><span data-stu-id="49278-113">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="49278-114">Caso contrário, ele retorna um código de erro **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="49278-114">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="49278-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="49278-115">Remarks</span></span>

<span data-ttu-id="49278-116">Os aplicativos devem chamar [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) em vez de chamar essa função.</span><span class="sxs-lookup"><span data-stu-id="49278-116">Applications should call [**SaveCurrentSettings**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-savecurrentsettings) instead of calling this function.</span></span>

<span data-ttu-id="49278-117">Esta função não tem biblioteca de importação associada.</span><span class="sxs-lookup"><span data-stu-id="49278-117">This function has no associated import library.</span></span> <span data-ttu-id="49278-118">Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="49278-118">To call this function, you must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="49278-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49278-119">Requirements</span></span>



| <span data-ttu-id="49278-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="49278-120">Requirement</span></span> | <span data-ttu-id="49278-121">Valor</span><span class="sxs-lookup"><span data-stu-id="49278-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49278-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49278-122">Minimum supported client</span></span><br/> | <span data-ttu-id="49278-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49278-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="49278-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49278-124">Minimum supported server</span></span><br/> | <span data-ttu-id="49278-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49278-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="49278-126">DLL</span><span class="sxs-lookup"><span data-stu-id="49278-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49278-127"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49278-127"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49278-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="49278-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49278-129">Monitorar funções de configuração</span><span class="sxs-lookup"><span data-stu-id="49278-129">Monitor Configuration Functions</span></span>](monitor-configuration-functions.md)
</dt> </dl>

 

