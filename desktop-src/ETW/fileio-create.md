---
description: Essa classe é a classe de tipo de evento para o evento de criação de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 83465072-3dae-4a39-8a36-1512025b79df
title: Classe FileIo_Create
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Create
- FileIo_Create.IrpPtr
- FileIo_Create.TTID
- FileIo_Create.FileObject
- FileIo_Create.CreateOptions
- FileIo_Create.FileAttributes
- FileIo_Create.ShareAccess
- FileIo_Create.OpenPath
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2f8a42e9dee1c49817d578ab73a221c013f69aef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967428"
---
# <a name="fileio_create-class"></a><span data-ttu-id="c9af9-104">\_Criar classe de FileIo</span><span class="sxs-lookup"><span data-stu-id="c9af9-104">FileIo\_Create class</span></span>

<span data-ttu-id="c9af9-105">Essa classe é a classe de tipo de evento para o evento de criação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c9af9-105">This class is the event type class for the file create event.</span></span>

<span data-ttu-id="c9af9-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="c9af9-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9af9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9af9-107">Syntax</span></span>

``` syntax
[EventType{64}, EventTypeName{"Create"}]
class FileIo_Create : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 CreateOptions;
  uint32 FileAttributes;
  uint32 ShareAccess;
  string OpenPath;
};
```

## <a name="members"></a><span data-ttu-id="c9af9-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c9af9-108">Members</span></span>

<span data-ttu-id="c9af9-109">A classe **FileIo \_ Create** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9af9-109">The **FileIo\_Create** class has these types of members:</span></span>

-   [<span data-ttu-id="c9af9-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9af9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9af9-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9af9-111">Properties</span></span>

<span data-ttu-id="c9af9-112">A classe **FileIo \_ Create** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c9af9-112">The **FileIo\_Create** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9af9-113">**Criaroptions**</span><span class="sxs-lookup"><span data-stu-id="c9af9-113">**CreateOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9af9-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-116">Qualificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="c9af9-116">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-117">Valores passados nos parâmetros *CreateOptions* e *createdisposiçãos* para a função [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="c9af9-117">Values passed in the *CreateOptions* and *CreateDispositions* parameters to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="c9af9-118">**FileAttributes**</span><span class="sxs-lookup"><span data-stu-id="c9af9-118">**FileAttributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9af9-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-121">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="c9af9-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-122">Valor passado no parâmetro *FileAttributes* para a função [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="c9af9-122">Value passed in the *FileAttributes* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="c9af9-123">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="c9af9-123">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9af9-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-126">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="c9af9-126">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-127">Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="c9af9-127">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="c9af9-128">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="c9af9-128">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9af9-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-131">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="c9af9-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-132">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="c9af9-132">IO request packet.</span></span> <span data-ttu-id="c9af9-133">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="c9af9-133">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="c9af9-134">**OpenPath**</span><span class="sxs-lookup"><span data-stu-id="c9af9-134">**OpenPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="c9af9-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-137">Qualificadores: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="c9af9-137">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-138">Caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c9af9-138">Path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="c9af9-139">**ShareAccess**</span><span class="sxs-lookup"><span data-stu-id="c9af9-139">**ShareAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-140">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9af9-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-142">Qualificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="c9af9-142">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-143">Valor passado no parâmetro *ShareAccess* para a função [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="c9af9-143">Value passed in the *ShareAccess* parameter to the [**NtCreateFile**](/windows/win32/api/winternl/nf-winternl-ntcreatefile) function.</span></span>

</dd> <dt>

<span data-ttu-id="c9af9-144">**TTID**</span><span class="sxs-lookup"><span data-stu-id="c9af9-144">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9af9-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c9af9-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9af9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9af9-147">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="c9af9-147">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c9af9-148">Identificador de thread do thread que está criando o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c9af9-148">Thread identifier of the thread that is creating the file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9af9-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9af9-149">Requirements</span></span>



| <span data-ttu-id="c9af9-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9af9-150">Requirement</span></span> | <span data-ttu-id="c9af9-151">Valor</span><span class="sxs-lookup"><span data-stu-id="c9af9-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c9af9-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9af9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c9af9-153">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9af9-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c9af9-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9af9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c9af9-155">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9af9-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9af9-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9af9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9af9-157">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="c9af9-157">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 
