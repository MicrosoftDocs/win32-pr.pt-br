---
description: Essa classe é a classe de tipo de evento para eventos de e/s de divisão. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 0eb1f712-8b1c-4de1-b701-5c7dbabb0f55
title: Classe SplitIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SplitIo_Info
- SplitIo_Info.ParentIrp
- SplitIo_Info.ChildIrp
api_type:
- NA
api_location: ''
ms.openlocfilehash: 469c8f04664f72b88e5a4378cb318b52f32fba24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836870"
---
# <a name="splitio_info-class"></a><span data-ttu-id="98330-104">Classe de informações de SplitIo \_</span><span class="sxs-lookup"><span data-stu-id="98330-104">SplitIo\_Info class</span></span>

<span data-ttu-id="98330-105">Essa classe é a classe de tipo de evento para eventos de e/s de divisão.</span><span class="sxs-lookup"><span data-stu-id="98330-105">This class is the event type class for split IO events.</span></span>

<span data-ttu-id="98330-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="98330-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="98330-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98330-107">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"VolMgr"}]
class SplitIo_Info : SplitIo
{
  uint32 ParentIrp;
  uint32 ChildIrp;
};
```

## <a name="members"></a><span data-ttu-id="98330-108">Membros</span><span class="sxs-lookup"><span data-stu-id="98330-108">Members</span></span>

<span data-ttu-id="98330-109">A classe **SplitIo \_ info** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="98330-109">The **SplitIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="98330-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98330-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98330-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="98330-111">Properties</span></span>

<span data-ttu-id="98330-112">A classe **SplitIo \_ info** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="98330-112">The **SplitIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98330-113">**ChildIrp**</span><span class="sxs-lookup"><span data-stu-id="98330-113">**ChildIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98330-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98330-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98330-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98330-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98330-116">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="98330-116">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="98330-117">Pacote de solicitação de e/s filho.</span><span class="sxs-lookup"><span data-stu-id="98330-117">Child IO request packet.</span></span>

</dd> <dt>

<span data-ttu-id="98330-118">**ParentIrp**</span><span class="sxs-lookup"><span data-stu-id="98330-118">**ParentIrp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98330-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98330-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98330-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="98330-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98330-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="98330-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="98330-122">Pacote de solicitação de es pai.</span><span class="sxs-lookup"><span data-stu-id="98330-122">Parent IO request packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98330-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="98330-123">Remarks</span></span>

<span data-ttu-id="98330-124">Indica que o Gerenciador de volumes divide o IRP em dois IRPs.</span><span class="sxs-lookup"><span data-stu-id="98330-124">Indicates that the volume manager split the IRP into two IRPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="98330-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98330-125">Requirements</span></span>



| <span data-ttu-id="98330-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="98330-126">Requirement</span></span> | <span data-ttu-id="98330-127">Valor</span><span class="sxs-lookup"><span data-stu-id="98330-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98330-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98330-128">Minimum supported client</span></span><br/> | <span data-ttu-id="98330-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="98330-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="98330-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="98330-130">Minimum supported server</span></span><br/> | <span data-ttu-id="98330-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="98330-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




