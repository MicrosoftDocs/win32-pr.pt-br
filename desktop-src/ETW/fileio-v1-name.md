---
description: Essa classe é a classe de tipo de evento para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: a4ee38df-af75-4aec-89ec-5a1c39302c82
title: Classe FileIo_V1_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V1_Name
- FileIo_V1_Name.FileObject
- FileIo_V1_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 617e0abeed095099996079211107d0720017514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011313"
---
# <a name="fileio_v1_name-class"></a><span data-ttu-id="5bb65-104">\_Classe de \_ nome FileIo v1</span><span class="sxs-lookup"><span data-stu-id="5bb65-104">FileIo\_V1\_Name class</span></span>

<span data-ttu-id="5bb65-105">Essa classe é a classe de tipo de evento para eventos de e/s de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5bb65-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="5bb65-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="5bb65-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bb65-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bb65-107">Syntax</span></span>

``` syntax
[EventType{0, 32}, EventTypeName{"Name", "FileCreate"}]
class FileIo_V1_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="5bb65-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5bb65-108">Members</span></span>

<span data-ttu-id="5bb65-109">A classe de **\_ \_ nome FileIo v1** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5bb65-109">The **FileIo\_V1\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="5bb65-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5bb65-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5bb65-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5bb65-111">Properties</span></span>

<span data-ttu-id="5bb65-112">A classe de **\_ \_ nome FileIo v1** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5bb65-112">The **FileIo\_V1\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5bb65-113">FileName</span><span class="sxs-lookup"><span data-stu-id="5bb65-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bb65-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5bb65-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5bb65-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bb65-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bb65-116">Qualificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5bb65-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5bb65-117">Caminho completo do arquivo, não incluindo a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="5bb65-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="5bb65-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="5bb65-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5bb65-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5bb65-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5bb65-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5bb65-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5bb65-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="5bb65-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5bb65-122">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="5bb65-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5bb65-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bb65-123">Remarks</span></span>

<span data-ttu-id="5bb65-124">**Windows Server 2003:** Para recuperar a letra da unidade para o caminho do nome do arquivo, use o valor da propriedade **FileObject** para mapear para o evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="5bb65-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="5bb65-125">No evento DiskIo \_ TypeGroup1, use os valores de propriedade **DiskNumber** e **ByteOffset** para mapear para o evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondente (**ByteOffset** Maps para **StartOffset**).</span><span class="sxs-lookup"><span data-stu-id="5bb65-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="5bb65-126">A propriedade **DriveLetterString** contém a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="5bb65-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bb65-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bb65-127">Requirements</span></span>



| <span data-ttu-id="5bb65-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bb65-128">Requirement</span></span> | <span data-ttu-id="5bb65-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5bb65-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5bb65-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bb65-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5bb65-131">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5bb65-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5bb65-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5bb65-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5bb65-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5bb65-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5bb65-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bb65-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bb65-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="5bb65-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




