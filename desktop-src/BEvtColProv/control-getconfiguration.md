---
description: Leia a configuração ativa do coletor.
ms.assetid: ea26142d-5dcd-466d-b9df-5349f58a190f
ms.tgt_platform: multiple
title: Método GetConfiguration da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.GetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 5adfedb833043ffc56da09c7bdab95c1c4698587
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920141"
---
# <a name="getconfiguration-method-of-the-control-class"></a><span data-ttu-id="d5dfd-103">Método GetConfiguration da classe Control</span><span class="sxs-lookup"><span data-stu-id="d5dfd-103">GetConfiguration method of the Control class</span></span>

<span data-ttu-id="d5dfd-104">Leia a configuração ativa do coletor.</span><span class="sxs-lookup"><span data-stu-id="d5dfd-104">Read the active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5dfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5dfd-105">Syntax</span></span>


```mof
Uint32 GetConfiguration(
  [out] Uint32 TimestampLow,
  [out] Uint32 TimestampHigh
);
```



## <a name="parameters"></a><span data-ttu-id="d5dfd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5dfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5dfd-107">*TimestampLow* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5dfd-107">*TimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dfd-108">Quando esse método retorna, esse parâmetro contém os bits de ordem inferior de um carimbo de data/hora que indica quando a configuração foi definida.</span><span class="sxs-lookup"><span data-stu-id="d5dfd-108">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> <dt>

<span data-ttu-id="d5dfd-109">*TimestampHigh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5dfd-109">*TimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5dfd-110">Quando esse método retorna, esse parâmetro contém os bits de ordem superior de um carimbo de data/hora que indica quando a configuração foi definida.</span><span class="sxs-lookup"><span data-stu-id="d5dfd-110">When this method returns, this parameter contains the high-order bits of a timestamp that indicates when the configuration was set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5dfd-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d5dfd-111">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="d5dfd-112">0</span><span class="sxs-lookup"><span data-stu-id="d5dfd-112">0</span></span>

<span data-ttu-id="d5dfd-113">Falha</span><span class="sxs-lookup"><span data-stu-id="d5dfd-113">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="d5dfd-114">1</span><span class="sxs-lookup"><span data-stu-id="d5dfd-114">1</span></span>

<span data-ttu-id="d5dfd-115">Sucesso</span><span class="sxs-lookup"><span data-stu-id="d5dfd-115">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5dfd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5dfd-116">Requirements</span></span>



| <span data-ttu-id="d5dfd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5dfd-117">Requirement</span></span> | <span data-ttu-id="d5dfd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d5dfd-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5dfd-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5dfd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d5dfd-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d5dfd-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d5dfd-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5dfd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d5dfd-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d5dfd-122">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="d5dfd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5dfd-123">Namespace</span></span><br/>                | <span data-ttu-id="d5dfd-124">Raiz \\ do Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="d5dfd-124">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="d5dfd-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d5dfd-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5dfd-126"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfd-126"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5dfd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d5dfd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5dfd-128"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5dfd-128"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d5dfd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5dfd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5dfd-130">**Control**</span><span class="sxs-lookup"><span data-stu-id="d5dfd-130">**Control**</span></span>](control.md)
</dt> </dl>

 

 




