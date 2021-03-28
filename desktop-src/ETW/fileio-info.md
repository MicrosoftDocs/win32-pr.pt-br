---
description: Essa classe é a classe de tipo de evento para o evento de informações de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 41ae1f8a-a90f-43d0-a848-a2c095f046d4
title: Classe FileIo_Info
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Info
- FileIo_Info.IrpPtr
- FileIo_Info.TTID
- FileIo_Info.FileObject
- FileIo_Info.FileKey
- FileIo_Info.ExtraInfo
- FileIo_Info.InfoClass
api_type:
- NA
api_location: ''
ms.openlocfilehash: 985986132abe432e1adefb51939b8ace1aa48c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968105"
---
# <a name="fileio_info-class"></a><span data-ttu-id="aa2bf-104">Classe de informações de FileIo \_</span><span class="sxs-lookup"><span data-stu-id="aa2bf-104">FileIo\_Info class</span></span>

<span data-ttu-id="aa2bf-105">Essa classe é a classe de tipo de evento para o evento de informações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-105">This class is the event type class for file information event.</span></span>

<span data-ttu-id="aa2bf-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa2bf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa2bf-107">Syntax</span></span>

``` syntax
[EventType{69, 70, 71, 74, 75}, EventTypeName{"SetInfo", "Delete", "Rename", "QueryInfo", "FSControl"}]
class FileIo_Info : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 ExtraInfo;
  uint32 InfoClass;
};
```

## <a name="members"></a><span data-ttu-id="aa2bf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="aa2bf-108">Members</span></span>

<span data-ttu-id="aa2bf-109">A classe de **\_ informações de FileIo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aa2bf-109">The **FileIo\_Info** class has these types of members:</span></span>

-   [<span data-ttu-id="aa2bf-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aa2bf-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa2bf-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aa2bf-111">Properties</span></span>

<span data-ttu-id="aa2bf-112">A classe de **\_ informações de FileIo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-112">The **FileIo\_Info** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa2bf-113">**ExtraInfo**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-113">**ExtraInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa2bf-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa2bf-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-116">Qualificadores: WmiDataId (5), ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa2bf-116">Qualifiers: WmiDataId(5), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aa2bf-117">Para solicitações FileDispositionInformation, esse campo contém a disposição solicitada.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-117">For FileDispositionInformation requests, this field contains the requested disposition.</span></span> <span data-ttu-id="aa2bf-118">Para solicitações FileEndOfFileInformation e FileAllocationInformation, esse campo contém o tamanho de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-118">For FileEndOfFileInformation and FileAllocationInformation requests, this field contains the specified file size.</span></span>

</dd> <dt>

<span data-ttu-id="aa2bf-119">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-119">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa2bf-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa2bf-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-122">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa2bf-122">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aa2bf-123">Para determinar o nome do arquivo, corresponda ao valor dessa propriedade à propriedade **FileObject** de um evento [**de \_ nome de FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="aa2bf-123">To determine the file name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="aa2bf-124">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-124">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa2bf-125">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa2bf-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-127">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa2bf-127">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aa2bf-128">Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-128">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="aa2bf-129">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-129">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa2bf-130">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa2bf-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-132">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="aa2bf-132">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="aa2bf-133">Classe de informações de arquivo solicitada.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-133">Requested file information class.</span></span>

</dd> <dt>

<span data-ttu-id="aa2bf-134">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-134">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa2bf-135">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa2bf-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-137">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa2bf-137">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aa2bf-138">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-138">IO request packet.</span></span> <span data-ttu-id="aa2bf-139">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-139">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="aa2bf-140">**TTID**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-140">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa2bf-141">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa2bf-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa2bf-143">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="aa2bf-143">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="aa2bf-144">Identificador de thread do thread que está executando a operação.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-144">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa2bf-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa2bf-145">Remarks</span></span>

<span data-ttu-id="aa2bf-146">Definir informações e eventos de informações de consulta indicam que os atributos de arquivo foram definidos ou consultados.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-146">Set information and query information events indicate that the file attributes were set or queried.</span></span> <span data-ttu-id="aa2bf-147">Um evento de controle do sistema de arquivos (FSControl) é registrado quando um comando FSCTL é emitido.</span><span class="sxs-lookup"><span data-stu-id="aa2bf-147">A file system control (FSControl) event is recorded when a FSCTL command is issued.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa2bf-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa2bf-148">Requirements</span></span>



| <span data-ttu-id="aa2bf-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa2bf-149">Requirement</span></span> | <span data-ttu-id="aa2bf-150">Valor</span><span class="sxs-lookup"><span data-stu-id="aa2bf-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa2bf-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa2bf-151">Minimum supported client</span></span><br/> | <span data-ttu-id="aa2bf-152">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa2bf-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aa2bf-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa2bf-153">Minimum supported server</span></span><br/> | <span data-ttu-id="aa2bf-154">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa2bf-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa2bf-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa2bf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa2bf-156">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="aa2bf-156">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




