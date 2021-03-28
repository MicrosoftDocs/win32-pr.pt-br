---
description: Essa classe é a classe de tipo de evento para eventos de operação de arquivo simples. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 5b6374e0-b39a-4d5a-acbd-25b410f1ba52
title: Classe FileIo_SimpleOp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_SimpleOp
- FileIo_SimpleOp.IrpPtr
- FileIo_SimpleOp.TTID
- FileIo_SimpleOp.FileObject
- FileIo_SimpleOp.FileKey
api_type:
- NA
api_location: ''
ms.openlocfilehash: f7ff09830653278c9b37cfefa81b182b0f1dc054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968103"
---
# <a name="fileio_simpleop-class"></a><span data-ttu-id="4928c-104">\_Classe SimpleOp FileIo</span><span class="sxs-lookup"><span data-stu-id="4928c-104">FileIo\_SimpleOp class</span></span>

<span data-ttu-id="4928c-105">Essa classe é a classe de tipo de evento para eventos de operação de arquivo simples.</span><span class="sxs-lookup"><span data-stu-id="4928c-105">This class is the event type class for simple file operation events.</span></span>

<span data-ttu-id="4928c-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="4928c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4928c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4928c-107">Syntax</span></span>

``` syntax
[EventType{65, 66, 73}, EventTypeName{"Cleanup", "Close", "Flush"}]
class FileIo_SimpleOp : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
};
```

## <a name="members"></a><span data-ttu-id="4928c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4928c-108">Members</span></span>

<span data-ttu-id="4928c-109">A classe **FileIo \_ SimpleOp** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4928c-109">The **FileIo\_SimpleOp** class has these types of members:</span></span>

-   [<span data-ttu-id="4928c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4928c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4928c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4928c-111">Properties</span></span>

<span data-ttu-id="4928c-112">A classe **FileIo \_ SimpleOp** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="4928c-112">The **FileIo\_SimpleOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4928c-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="4928c-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4928c-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4928c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4928c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4928c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4928c-116">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="4928c-116">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4928c-117">Para determinar o nome do arquivo, corresponda ao valor dessa propriedade à propriedade **FileObject** de um evento [**de \_ nome de FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="4928c-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="4928c-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="4928c-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4928c-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4928c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4928c-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4928c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4928c-121">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="4928c-121">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4928c-122">Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4928c-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="4928c-123">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="4928c-123">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4928c-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4928c-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4928c-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4928c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4928c-126">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="4928c-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4928c-127">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="4928c-127">IO request packet.</span></span> <span data-ttu-id="4928c-128">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="4928c-128">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="4928c-129">**TTID**</span><span class="sxs-lookup"><span data-stu-id="4928c-129">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4928c-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4928c-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4928c-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4928c-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4928c-132">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="4928c-132">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4928c-133">Identificador de thread do thread que está executando a operação.</span><span class="sxs-lookup"><span data-stu-id="4928c-133">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4928c-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="4928c-134">Remarks</span></span>

<span data-ttu-id="4928c-135">O evento de limpeza é registrado quando o último identificador do arquivo é fechado.</span><span class="sxs-lookup"><span data-stu-id="4928c-135">The Cleanup event is logged when the last handle to the file is closed.</span></span> <span data-ttu-id="4928c-136">O evento Close especifica que um objeto de arquivo está sendo liberado.</span><span class="sxs-lookup"><span data-stu-id="4928c-136">The Close event specifies that a file object is being freed.</span></span> <span data-ttu-id="4928c-137">O evento flush especifica quando os buffers de arquivo são totalmente liberados para o disco.</span><span class="sxs-lookup"><span data-stu-id="4928c-137">The Flush event specifies when the file buffers are fully flushed to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="4928c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4928c-138">Requirements</span></span>



| <span data-ttu-id="4928c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="4928c-139">Requirement</span></span> | <span data-ttu-id="4928c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="4928c-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4928c-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4928c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4928c-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4928c-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4928c-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4928c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4928c-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4928c-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4928c-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="4928c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4928c-146">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="4928c-146">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




