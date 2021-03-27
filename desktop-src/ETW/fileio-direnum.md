---
description: Essa classe é a classe de tipo de evento para o diretório enumerar e eventos de notificação de diretório. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 08458385-6066-4523-a053-aceb5e5d6f10
title: Classe FileIo_DirEnum
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_DirEnum
- FileIo_DirEnum.IrpPtr
- FileIo_DirEnum.TTID
- FileIo_DirEnum.FileObject
- FileIo_DirEnum.FileKey
- FileIo_DirEnum.Length
- FileIo_DirEnum.InfoClass
- FileIo_DirEnum.FileIndex
- FileIo_DirEnum.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 12f8fd8b4629ac11e7316caae0690982c210e4bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967427"
---
# <a name="fileio_direnum-class"></a><span data-ttu-id="1a3ba-104">\_Classe DirEnum FileIo</span><span class="sxs-lookup"><span data-stu-id="1a3ba-104">FileIo\_DirEnum class</span></span>

<span data-ttu-id="1a3ba-105">Essa classe é a classe de tipo de evento para o diretório enumerar e eventos de notificação de diretório.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-105">This class is the event type class for the enumerate directory and directory notification events.</span></span>

<span data-ttu-id="1a3ba-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a3ba-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a3ba-107">Syntax</span></span>

``` syntax
[EventType{72, 77}, EventTypeName{"DirEnum", "DirNotify"}]
class FileIo_DirEnum : FileIo
{
  uint32 IrpPtr;
  uint32 TTID;
  uint32 FileObject;
  uint32 FileKey;
  uint32 Length;
  uint32 InfoClass;
  uint32 FileIndex;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="1a3ba-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1a3ba-108">Members</span></span>

<span data-ttu-id="1a3ba-109">A classe **FileIo \_ DirEnum** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1a3ba-109">The **FileIo\_DirEnum** class has these types of members:</span></span>

-   [<span data-ttu-id="1a3ba-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a3ba-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a3ba-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1a3ba-111">Properties</span></span>

<span data-ttu-id="1a3ba-112">A classe **FileIo \_ DirEnum** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-112">The **FileIo\_DirEnum** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a3ba-113">**FileIndex**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-113">**FileIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-116">Qualificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="1a3ba-116">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-117">Índice de arquivo do qual continuar a enumeração de diretório.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-117">File index from which to continue directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-118">**FileKey**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-118">**FileKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-121">Qualificadores: WmiDataId (4), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1a3ba-121">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-122">Para determinar o nome do diretório, corresponda ao valor dessa propriedade à propriedade **FileObject** de um evento [**de \_ nome de FileIo**](fileio-name.md) .</span><span class="sxs-lookup"><span data-stu-id="1a3ba-122">To determine the directory name, match the value of this property to the **FileObject** property of a [**FileIo\_Name**](fileio-name.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-123">**FileName**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-123">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-126">Qualificadores: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="1a3ba-126">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-127">Padrão especificado para enumeração de diretório.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-127">Pattern specified for directory enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-128">**FileObject**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-128">**FileObject**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-131">Qualificadores: WmiDataId (3), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1a3ba-131">Qualifiers: WmiDataId(3), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-132">Identificador que pode ser usado para correlacionar operações para a mesma instância de objeto de arquivo aberta entre eventos de criação e fechamento de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-132">Identifier that can be used for correlating operations to the same opened file object instance between file create and close events.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-133">**InfoClass**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-133">**InfoClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-136">Qualificadores: WmiDataId (6), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1a3ba-136">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-137">Classe de informações de enumeração de diretório solicitada.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-137">Requested directory enumeration information class.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-138">**IrpPtr**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-138">**IrpPtr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-141">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1a3ba-141">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-142">Pacote de solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-142">IO request packet.</span></span> <span data-ttu-id="1a3ba-143">Essa propriedade identifica a atividade de e/s.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-143">This property identifies the IO activity.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-144">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-144">**Length**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-145">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-147">Qualificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="1a3ba-147">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-148">Tamanho do buffer de consulta, em bytes.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-148">Size of the query buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1a3ba-149">**TTID**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-149">**TTID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a3ba-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1a3ba-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a3ba-152">Qualificadores: WmiDataId (2), ponteiro</span><span class="sxs-lookup"><span data-stu-id="1a3ba-152">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="1a3ba-153">Identificador de thread do thread que está executando a operação.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-153">Thread identifier of the thread that is performing the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a3ba-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a3ba-154">Remarks</span></span>

<span data-ttu-id="1a3ba-155">Os eventos de enumeração de diretório e de notificação de diretório são registrados quando um diretório é enumerado ou uma notificação de alteração de diretório é enviada para os ouvintes registrados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-155">Directory enumeration and directory notification events are recorded when a directory is enumerated or a directory change notification is sent to registered listeners, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a3ba-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a3ba-156">Requirements</span></span>



| <span data-ttu-id="1a3ba-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a3ba-157">Requirement</span></span> | <span data-ttu-id="1a3ba-158">Valor</span><span class="sxs-lookup"><span data-stu-id="1a3ba-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a3ba-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a3ba-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1a3ba-160">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a3ba-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a3ba-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a3ba-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1a3ba-162">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a3ba-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a3ba-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a3ba-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a3ba-164">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="1a3ba-164">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




