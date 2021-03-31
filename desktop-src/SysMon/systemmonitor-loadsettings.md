---
title: Método SystemMonitor. Configurations
description: Adiciona os contadores no arquivo de modelo HTML ao monitor do sistema.
ms.assetid: 3f88e590-df2b-4861-8ee6-a08f8742e6ad
keywords:
- Método LoadSettings SysMon
- Método LoadSettings SysMon, objeto SystemMonitor
- Objeto SystemMonitor Sysmon, método Configurations
topic_type:
- apiref
api_name:
- SystemMonitor.LoadSettings
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e412ebfe97035c4847391a7cc9166cf512897bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369641"
---
# <a name="systemmonitorloadsettings-method"></a><span data-ttu-id="1cac9-106">Método SystemMonitor. Configurations</span><span class="sxs-lookup"><span data-stu-id="1cac9-106">SystemMonitor.LoadSettings method</span></span>

<span data-ttu-id="1cac9-107">Adiciona os contadores no arquivo de modelo HTML ao monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="1cac9-107">Adds the counters in the HTML template file to the System Monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cac9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cac9-108">Syntax</span></span>


```VB
SystemMonitor.LoadSettings( _
  ByVal SettingsFileName As String _
)
```



## <a name="parameters"></a><span data-ttu-id="1cac9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cac9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cac9-110">*SettingsFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cac9-110">*SettingsFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cac9-111">Cadeia de caracteres HTML que especifica os contadores a serem adicionados ao monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="1cac9-111">HTML string that specifies the counters to add to the System Monitor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cac9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cac9-112">Return value</span></span>

<span data-ttu-id="1cac9-113">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1cac9-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cac9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cac9-114">Remarks</span></span>

<span data-ttu-id="1cac9-115">Para salvar os contadores atuais no monitor do sistema em um arquivo HTML, chame o método [**SystemMonitor. SaveAs**](systemmonitor-saveas.md) .</span><span class="sxs-lookup"><span data-stu-id="1cac9-115">To save the current counters in the System Monitor to an HTML file, call the [**SystemMonitor.SaveAs**](systemmonitor-saveas.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cac9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cac9-116">Requirements</span></span>



| <span data-ttu-id="1cac9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cac9-117">Requirement</span></span> | <span data-ttu-id="1cac9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1cac9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cac9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cac9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1cac9-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1cac9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1cac9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cac9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1cac9-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1cac9-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1cac9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1cac9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cac9-124"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1cac9-124"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cac9-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1cac9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cac9-126">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="1cac9-126">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





