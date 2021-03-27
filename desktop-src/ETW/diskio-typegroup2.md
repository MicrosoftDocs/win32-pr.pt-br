---
description: Essa classe é a classe de tipo de evento que marca o início dos eventos de leitura, gravação e liberação de e/s de disco. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 96543ef9-cc2b-4d9a-86a8-f2458439e4d8
title: Classe DiskIo_TypeGroup2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo_TypeGroup2
- DiskIo_TypeGroup2.Irp
- DiskIo_TypeGroup2.IssuingThreadId
api_type:
- NA
api_location: ''
ms.openlocfilehash: ea08f32106c935be628bcdcd22e39ab92a0566e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501392"
---
# <a name="diskio_typegroup2-class"></a><span data-ttu-id="497db-104">\_Classe DiskIo TypeGroup2</span><span class="sxs-lookup"><span data-stu-id="497db-104">DiskIo\_TypeGroup2 class</span></span>

<span data-ttu-id="497db-105">Essa classe é a classe de tipo de evento que marca o início dos eventos de leitura, gravação e liberação de e/s de disco.</span><span class="sxs-lookup"><span data-stu-id="497db-105">This class is the event type class that marks the beginning of the disk I/O read, write, and flush events.</span></span>

<span data-ttu-id="497db-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="497db-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="497db-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="497db-107">Syntax</span></span>

``` syntax
[EventType{12, 13, 15}, EventTypeName{"ReadInit", "WriteInit", "FlushInit"}]
class DiskIo_TypeGroup2 : DiskIo
{
  uint32 Irp;
  uint32 IssuingThreadId;
};
```

## <a name="members"></a><span data-ttu-id="497db-108">Membros</span><span class="sxs-lookup"><span data-stu-id="497db-108">Members</span></span>

<span data-ttu-id="497db-109">A classe **DiskIo \_ TypeGroup2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="497db-109">The **DiskIo\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="497db-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="497db-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="497db-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="497db-111">Properties</span></span>

<span data-ttu-id="497db-112">A classe **DiskIo \_ TypeGroup2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="497db-112">The **DiskIo\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="497db-113">**IRP**</span><span class="sxs-lookup"><span data-stu-id="497db-113">**Irp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="497db-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="497db-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="497db-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="497db-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="497db-116">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**ponteiro**](event-tracing-mof-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="497db-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1), [**Pointer**](event-tracing-mof-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="497db-117">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="497db-117">I/O request packet.</span></span> <span data-ttu-id="497db-118">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="497db-118">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="497db-119">**IssuingThreadId**</span><span class="sxs-lookup"><span data-stu-id="497db-119">**IssuingThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="497db-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="497db-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="497db-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="497db-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="497db-122">Qualificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="497db-122">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="497db-123">O identificador do thread emissor.</span><span class="sxs-lookup"><span data-stu-id="497db-123">The identifier of the issuing thread.</span></span>

<span data-ttu-id="497db-124">**Windows server 2008 R2, Windows server 2008, Windows 7 e Windows Vista:** Não há suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="497db-124">**Windows Server 2008 R2, Windows Server 2008, Windows 7 and Windows Vista:** This property is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="497db-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="497db-125">Requirements</span></span>



| <span data-ttu-id="497db-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="497db-126">Requirement</span></span> | <span data-ttu-id="497db-127">Valor</span><span class="sxs-lookup"><span data-stu-id="497db-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="497db-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="497db-128">Minimum supported client</span></span><br/> | <span data-ttu-id="497db-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="497db-129">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="497db-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="497db-130">Minimum supported server</span></span><br/> | <span data-ttu-id="497db-131">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="497db-131">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="497db-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="497db-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="497db-133">**DiskIo**</span><span class="sxs-lookup"><span data-stu-id="497db-133">**DiskIo**</span></span>](diskio.md)
</dt> </dl>

 

 




