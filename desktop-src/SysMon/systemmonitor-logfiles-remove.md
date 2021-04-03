---
title: Método LogFiles. Remove
description: Remove a instância LogFileItem especificada da coleção.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Remover o método SysMon
- Remover método SysMon, classe LogFiles
- Classe LogFiles SysMon, método remove
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645008"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="b32b6-106">Método LogFiles. Remove</span><span class="sxs-lookup"><span data-stu-id="b32b6-106">LogFiles.Remove method</span></span>

<span data-ttu-id="b32b6-107">Remove a instância [**LogFileItem**](logfileitem.md) especificada da coleção.</span><span class="sxs-lookup"><span data-stu-id="b32b6-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b32b6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b32b6-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="b32b6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b32b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b32b6-110">*índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="b32b6-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b32b6-111">Índice de inteiro do arquivo de log a ser removido da coleção.</span><span class="sxs-lookup"><span data-stu-id="b32b6-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="b32b6-112">O índice é baseado em um.</span><span class="sxs-lookup"><span data-stu-id="b32b6-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b32b6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b32b6-113">Return value</span></span>

<span data-ttu-id="b32b6-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b32b6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b32b6-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b32b6-115">Remarks</span></span>

<span data-ttu-id="b32b6-116">**Antes do Windows Vista:** Você não poderá remover arquivos de log da [**coleção de arquivos de log**](systemmonitor-logfiles.md) se o valor de [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) for definido como sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="b32b6-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="b32b6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b32b6-117">Requirements</span></span>



| <span data-ttu-id="b32b6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b32b6-118">Requirement</span></span> | <span data-ttu-id="b32b6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b32b6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b32b6-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b32b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b32b6-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b32b6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b32b6-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b32b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b32b6-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b32b6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b32b6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="b32b6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b32b6-125"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="b32b6-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b32b6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b32b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b32b6-127">arquivos de log</span><span class="sxs-lookup"><span data-stu-id="b32b6-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="b32b6-128">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="b32b6-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="b32b6-129">**arquivos de log**</span><span class="sxs-lookup"><span data-stu-id="b32b6-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





