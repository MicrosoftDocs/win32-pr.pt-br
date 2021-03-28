---
description: Essa classe é a classe de tipo de evento para eventos de leitura e gravação de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 88c380fb-e043-40ab-aa74-550bce43c52b
title: Classe FileIo_ReadWrite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_ReadWrite
- FileIo_ReadWrite.Offset
- FileIo_ReadWrite.IrpPtr
- FileIo_ReadWrite.TTID
- FileIo_ReadWrite.FileObject
- FileIo_ReadWrite.FileKey
- FileIo_ReadWrite.IoSize
- FileIo_ReadWrite.IoFlags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c684444ea35efe0fee9c38b15be8fe7e45e9a102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968104"
---
# <a name="fileio_readwrite-class"></a><span data-ttu-id="d6a63-104">\_Classe FileIo ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6a63-104">FileIo\_ReadWrite class</span></span>

<span data-ttu-id="d6a63-105">Essa classe é a classe de tipo de evento para eventos de leitura e gravação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d6a63-105">This class is the event type class for file read and write events.</span></span>

<span data-ttu-id="d6a63-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="d6a63-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6a63-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6a63-107">Syntax</span></span>

``` syntax
[EventType{67, 68}, EventTypeName{"Read", "Write"}]
class FileIo_ReadWrite : FileIo
{
  uint64 Offset;
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 IoSize;
  uint32 IoFlags;
};
```

## <a name="members"></a><span data-ttu-id="d6a63-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d6a63-108">Members</span></span>

<span data-ttu-id="d6a63-109">A classe **FileIo \_ ReadWrite** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d6a63-109">The **FileIo\_ReadWrite** class has these types of members:</span></span>

-   [<span data-ttu-id="d6a63-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d6a63-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6a63-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d6a63-111">Properties</span></span>

<span data-ttu-id="d6a63-112">A classe **FileIo \_ ReadWrite** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d6a63-112">The **FileIo\_ReadWrite** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6a63-113">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="d6a63-113">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6a63-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-116">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="d6a63-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-117">Para determinar o nome do arquivo, corresponda ao valor dessa propriedade à propriedade **FileObject** de um evento [**de \_ nome de FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="d6a63-117">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="d6a63-118">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="d6a63-118">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6a63-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-121">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="d6a63-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-122">Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d6a63-122">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="d6a63-123">**IoFlags**</span><span class="sxs-lookup"><span data-stu-id="d6a63-123">**IoFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6a63-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-126">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="d6a63-126">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-127">Sinalizadores de pacote de solicitação de e/s especificados para esta operação.</span><span class="sxs-lookup"><span data-stu-id="d6a63-127">IO request packet flags specified for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6a63-128">**IoSize**</span><span class="sxs-lookup"><span data-stu-id="d6a63-128">**IoSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6a63-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-131">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="d6a63-131">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-132">Número de bytes solicitados.</span><span class="sxs-lookup"><span data-stu-id="d6a63-132">Number of bytes requested.</span></span>

</dd> <dt>

<span data-ttu-id="d6a63-133">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="d6a63-133">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6a63-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-136">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="d6a63-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-137">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="d6a63-137">IO request packet.</span></span> <span data-ttu-id="d6a63-138">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="d6a63-138">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="d6a63-139">**Deslocamento**</span><span class="sxs-lookup"><span data-stu-id="d6a63-139">**Offset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-140">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d6a63-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-142">Qualificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="d6a63-142">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-143">Iniciando o deslocamento do arquivo para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="d6a63-143">Starting file offset for the requested operation.</span></span>

</dd> <dt>

<span data-ttu-id="d6a63-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="d6a63-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6a63-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6a63-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d6a63-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6a63-147">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="d6a63-147">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d6a63-148">Identificador de thread do thread que está executando a operação.</span><span class="sxs-lookup"><span data-stu-id="d6a63-148">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6a63-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6a63-149">Requirements</span></span>



| <span data-ttu-id="d6a63-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6a63-150">Requirement</span></span> | <span data-ttu-id="d6a63-151">Valor</span><span class="sxs-lookup"><span data-stu-id="d6a63-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6a63-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6a63-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d6a63-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6a63-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6a63-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d6a63-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6a63-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6a63-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6a63-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6a63-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="d6a63-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




