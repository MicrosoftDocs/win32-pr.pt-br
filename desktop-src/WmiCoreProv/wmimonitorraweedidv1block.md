---
description: Representa os dados brutos de uma estrutura de dados de identificação de exibição estendida (E-EDID) avançada de uma associação padrão de eletrônicos de vídeo (VESA).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: Classe WmiMonitorRawEEdidV1Block
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815452"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="64097-103">Classe WmiMonitorRawEEdidV1Block</span><span class="sxs-lookup"><span data-stu-id="64097-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="64097-104">A classe WMI **WmiMonitorRawEEdidV1Block** representa os dados brutos de uma estrutura de dados de identificação de exibição estendida (VESA) avançada de uma associação de vídeo (e-EDID).</span><span class="sxs-lookup"><span data-stu-id="64097-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="64097-105">Essa estrutura de dados de 128 bytes contém informações que descrevem a configuração ideal para uma exibição.</span><span class="sxs-lookup"><span data-stu-id="64097-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="64097-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64097-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="64097-107">Membros</span><span class="sxs-lookup"><span data-stu-id="64097-107">Members</span></span>

<span data-ttu-id="64097-108">A classe **WmiMonitorRawEEdidV1Block** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="64097-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="64097-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64097-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64097-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="64097-110">Properties</span></span>

<span data-ttu-id="64097-111">A classe **WmiMonitorRawEEdidV1Block** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="64097-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="64097-112">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="64097-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64097-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="64097-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="64097-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64097-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64097-115">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="64097-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="64097-116">**Conteúdo**</span><span class="sxs-lookup"><span data-stu-id="64097-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64097-117">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="64097-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="64097-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64097-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64097-119">matriz de bytes de 128 que contém o conteúdo de bloco bruto.</span><span class="sxs-lookup"><span data-stu-id="64097-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="64097-120">**Id**</span><span class="sxs-lookup"><span data-stu-id="64097-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64097-121">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="64097-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="64097-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64097-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64097-123">Identidade do bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64097-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="64097-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="64097-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64097-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="64097-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64097-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64097-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64097-127">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="64097-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="64097-128">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="64097-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="64097-129">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="64097-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64097-130">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="64097-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="64097-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="64097-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="64097-132">Tipo de bloco de dados.</span><span class="sxs-lookup"><span data-stu-id="64097-132">Type of data block.</span></span> <span data-ttu-id="64097-133">A tabela a seguir lista os possíveis valores que podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="64097-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="64097-134">Valor</span><span class="sxs-lookup"><span data-stu-id="64097-134">Value</span></span>                                                                                 | <span data-ttu-id="64097-135">Significado</span><span class="sxs-lookup"><span data-stu-id="64097-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="64097-136"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="64097-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="64097-137">Não Inicializado</span><span class="sxs-lookup"><span data-stu-id="64097-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="64097-138"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="64097-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="64097-139">Bloco base EDID</span><span class="sxs-lookup"><span data-stu-id="64097-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="64097-140"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="64097-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="64097-141">Mapa de bloco EDID</span><span class="sxs-lookup"><span data-stu-id="64097-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="64097-142"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="64097-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="64097-143">Outro</span><span class="sxs-lookup"><span data-stu-id="64097-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64097-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64097-144">Requirements</span></span>



| <span data-ttu-id="64097-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="64097-145">Requirement</span></span> | <span data-ttu-id="64097-146">Valor</span><span class="sxs-lookup"><span data-stu-id="64097-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="64097-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64097-147">Minimum supported client</span></span><br/> | <span data-ttu-id="64097-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64097-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="64097-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64097-149">Minimum supported server</span></span><br/> | <span data-ttu-id="64097-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64097-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="64097-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="64097-151">Namespace</span></span><br/>                | <span data-ttu-id="64097-152">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="64097-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="64097-153">MOF</span><span class="sxs-lookup"><span data-stu-id="64097-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64097-154"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64097-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="64097-155">DLL</span><span class="sxs-lookup"><span data-stu-id="64097-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64097-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64097-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64097-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="64097-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64097-158">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="64097-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="64097-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="64097-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




