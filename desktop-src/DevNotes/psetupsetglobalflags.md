---
description: Desabilita os recursos do.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: função pSetupSetGlobalFlags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747266"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="29c5a-103">função pSetupSetGlobalFlags</span><span class="sxs-lookup"><span data-stu-id="29c5a-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="29c5a-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="29c5a-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="29c5a-105">Desabilita os recursos do.</span><span class="sxs-lookup"><span data-stu-id="29c5a-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c5a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29c5a-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="29c5a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29c5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c5a-108">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="29c5a-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29c5a-109">Os sinalizadores usados para desabilitar a interface do usuário ou o backup automático.</span><span class="sxs-lookup"><span data-stu-id="29c5a-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="29c5a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="29c5a-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="29c5a-111">Significado</span><span class="sxs-lookup"><span data-stu-id="29c5a-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="29c5a-112"><dt>**PSPGF \_**</dt> <dt>0X004</dt> não interativa</span><span class="sxs-lookup"><span data-stu-id="29c5a-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="29c5a-113">Defina para desabilitar a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="29c5a-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="29c5a-114"><dt>**PSPGF \_ NENHUM \_**</dt> <dt>0x002</dt> de backup</span><span class="sxs-lookup"><span data-stu-id="29c5a-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="29c5a-115">Defina para desabilitar o backup automático.</span><span class="sxs-lookup"><span data-stu-id="29c5a-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c5a-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29c5a-116">Return value</span></span>

<span data-ttu-id="29c5a-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="29c5a-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29c5a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="29c5a-118">Remarks</span></span>

<span data-ttu-id="29c5a-119">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="29c5a-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c5a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29c5a-120">Requirements</span></span>



| <span data-ttu-id="29c5a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="29c5a-121">Requirement</span></span> | <span data-ttu-id="29c5a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="29c5a-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29c5a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="29c5a-123">DLL</span></span><br/> | <dl> <span data-ttu-id="29c5a-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29c5a-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
