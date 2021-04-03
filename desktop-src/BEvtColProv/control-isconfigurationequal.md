---
description: Compare o argumento com a configuração ativa do coletor.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Método IsConfigurationEqual da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646221"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a><span data-ttu-id="5fb38-103">Método IsConfigurationEqual da classe Control</span><span class="sxs-lookup"><span data-stu-id="5fb38-103">IsConfigurationEqual method of the Control class</span></span>

<span data-ttu-id="5fb38-104">Compare o argumento com a configuração ativa do coletor.</span><span class="sxs-lookup"><span data-stu-id="5fb38-104">Compare the argument with the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fb38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fb38-105">Syntax</span></span>


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a><span data-ttu-id="5fb38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fb38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fb38-107">*Configuração* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5fb38-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fb38-108">A configuração para comparar com a configuração ativa.</span><span class="sxs-lookup"><span data-stu-id="5fb38-108">The configuration to compare to the active configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fb38-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5fb38-109">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="5fb38-110">0</span><span class="sxs-lookup"><span data-stu-id="5fb38-110">0</span></span>

<span data-ttu-id="5fb38-111">Falha</span><span class="sxs-lookup"><span data-stu-id="5fb38-111">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="5fb38-112">1</span><span class="sxs-lookup"><span data-stu-id="5fb38-112">1</span></span>

<span data-ttu-id="5fb38-113">Sucesso</span><span class="sxs-lookup"><span data-stu-id="5fb38-113">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fb38-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fb38-114">Requirements</span></span>



| <span data-ttu-id="5fb38-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fb38-115">Requirement</span></span> | <span data-ttu-id="5fb38-116">Valor</span><span class="sxs-lookup"><span data-stu-id="5fb38-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fb38-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fb38-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5fb38-118">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5fb38-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5fb38-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fb38-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5fb38-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5fb38-120">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="5fb38-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fb38-121">Namespace</span></span><br/>                | <span data-ttu-id="5fb38-122">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="5fb38-122">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="5fb38-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5fb38-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fb38-124"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fb38-124"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fb38-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5fb38-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fb38-126"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fb38-126"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5fb38-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fb38-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fb38-128">**Control**</span><span class="sxs-lookup"><span data-stu-id="5fb38-128">**Control**</span></span>](control.md)
</dt> </dl>

 

 




