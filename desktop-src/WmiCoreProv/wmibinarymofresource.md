---
description: O provedor de classe WDM define a classe WMIBinaryMofResource no \\ \\ namespace raiz WMI para dar suporte à tarefa de manter o controle do status dos dados no repositório WMI.
ms.assetid: 57416a36-5b3a-4d04-808c-09adc597c47a
title: Classe WMIBinaryMofResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WMIBinaryMofResource
- WMIBinaryMofResource.HighDateTime
- WMIBinaryMofResource.LowDateTime
- WMIBinaryMofResource.MofProcessed
- WMIBinaryMofResource.Name
api_type:
- Schema
api_location:
- Root\WMI
ms.openlocfilehash: 715436ef19308c811e5486926b3cd7e59ee9de0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827495"
---
# <a name="wmibinarymofresource-class"></a><span data-ttu-id="7870b-103">Classe WMIBinaryMofResource</span><span class="sxs-lookup"><span data-stu-id="7870b-103">WMIBinaryMofResource class</span></span>

<span data-ttu-id="7870b-104">O provedor de classe WDM define a classe **WMIBinaryMofResource** no \\ \\ namespace raiz WMI para dar suporte à tarefa de manter o controle do status dos dados no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="7870b-104">The WDM class provider defines the **WMIBinaryMofResource** class in the \\root\\wmi namespace to support the task of keeping track of the status of data in the WMI repository.</span></span>

## <a name="syntax"></a><span data-ttu-id="7870b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7870b-105">Syntax</span></span>

``` syntax
class WMIBinaryMofResource
{
  uint32  HighDateTime;
  uint32  LowDateTime;
  boolean MofProcessed;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="7870b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7870b-106">Members</span></span>

<span data-ttu-id="7870b-107">A classe **WMIBinaryMofResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7870b-107">The **WMIBinaryMofResource** class has these types of members:</span></span>

-   [<span data-ttu-id="7870b-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7870b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7870b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7870b-109">Properties</span></span>

<span data-ttu-id="7870b-110">A classe **WMIBinaryMofResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7870b-110">The **WMIBinaryMofResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7870b-111">**HighDateTime**</span><span class="sxs-lookup"><span data-stu-id="7870b-111">**HighDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7870b-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7870b-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7870b-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7870b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7870b-114">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7870b-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7870b-115">Metade alta do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="7870b-115">High half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="7870b-116">**LowDateTime**</span><span class="sxs-lookup"><span data-stu-id="7870b-116">**LowDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7870b-117">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7870b-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7870b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7870b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7870b-119">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7870b-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7870b-120">Metade baixa do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="7870b-120">Low half of the date-time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="7870b-121">**MofProcessed**</span><span class="sxs-lookup"><span data-stu-id="7870b-121">**MofProcessed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7870b-122">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7870b-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7870b-123">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7870b-123">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7870b-124">Sinalizador que indica se o arquivo. mof foi totalmente processado.</span><span class="sxs-lookup"><span data-stu-id="7870b-124">Flag indicating whether the .mof file was fully processed.</span></span>

</dd> <dt>

<span data-ttu-id="7870b-125">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7870b-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7870b-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7870b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7870b-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7870b-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7870b-128">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7870b-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7870b-129">Nome do driver habilitado para WDM que tem um arquivo MOF binário compilado com êxito no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="7870b-129">Name of the WDM enabled driver that has a binary MOF file successfully compiled in the WMI repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7870b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7870b-130">Remarks</span></span>

<span data-ttu-id="7870b-131">O provedor de classe WDM cria uma instância de **WMIBinaryMofResource** para cada driver WDM que fornece um arquivo MOF binário.</span><span class="sxs-lookup"><span data-stu-id="7870b-131">The WDM class provider creates an instance of **WMIBinaryMofResource** for each WDM driver that supplies a binary MOF file.</span></span>

<span data-ttu-id="7870b-132">Sempre que o WMI Inicializa o provedor, o provedor compara o carimbo de data/hora com o carimbo de data/hora do arquivo de imagem do driver.</span><span class="sxs-lookup"><span data-stu-id="7870b-132">Whenever WMI initializes the provider, the provider compares the timestamp with the timestamp of the driver image file.</span></span> <span data-ttu-id="7870b-133">Se os carimbos de data/hora forem diferentes, o WMI recompilará o arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="7870b-133">If the timestamps differ, WMI re-compiles the MOF file.</span></span>

## <a name="requirements"></a><span data-ttu-id="7870b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7870b-134">Requirements</span></span>



| <span data-ttu-id="7870b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7870b-135">Requirement</span></span> | <span data-ttu-id="7870b-136">Valor</span><span class="sxs-lookup"><span data-stu-id="7870b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7870b-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7870b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7870b-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7870b-138">Windows XP</span></span><br/>                                                              |
| <span data-ttu-id="7870b-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7870b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7870b-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7870b-140">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="7870b-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="7870b-141">Namespace</span></span><br/>                | <span data-ttu-id="7870b-142">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="7870b-142">Root\\WMI</span></span><br/>                                                               |
| <span data-ttu-id="7870b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="7870b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7870b-144"><dt>WMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7870b-144"><dt>Wmi.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7870b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7870b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7870b-146">Provedor WDM</span><span class="sxs-lookup"><span data-stu-id="7870b-146">WDM Provider</span></span>](wdm-provider.md)
</dt> </dl>

 

