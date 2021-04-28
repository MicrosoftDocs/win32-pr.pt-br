---
description: Classe FileIo_Name-essa classe é a classe de tipo de evento para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: ed72daa3-06c0-46f1-bb9d-c0b343228f28
title: Classe FileIo_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_Name
- FileIo_Name.FileObject
- FileIo_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9fabfbcfa318ad809b5cb2f66d72f19abf21112d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106584"
---
# <a name="fileio_name-class"></a><span data-ttu-id="75a49-104">\_Classe de nome FileIo</span><span class="sxs-lookup"><span data-stu-id="75a49-104">FileIo\_Name class</span></span>

<span data-ttu-id="75a49-105">Essa classe é a classe de tipo de evento para eventos de e/s de arquivo.</span><span class="sxs-lookup"><span data-stu-id="75a49-105">This class is the event type class for file I/O events.</span></span>

<span data-ttu-id="75a49-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="75a49-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="75a49-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75a49-107">Syntax</span></span>

``` syntax
[EventType{0, 32, 35, 36}, EventTypeName{"Name", "FileCreate", "FileDelete", "FileRundown"}]
class FileIo_Name : FileIo
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="75a49-108">Membros</span><span class="sxs-lookup"><span data-stu-id="75a49-108">Members</span></span>

<span data-ttu-id="75a49-109">A classe de **\_ nome FileIo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="75a49-109">The **FileIo\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="75a49-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75a49-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75a49-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75a49-111">Properties</span></span>

<span data-ttu-id="75a49-112">A classe de **\_ nome FileIo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="75a49-112">The **FileIo\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75a49-113">FileName</span><span class="sxs-lookup"><span data-stu-id="75a49-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75a49-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="75a49-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75a49-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75a49-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75a49-116">Qualificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="75a49-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="75a49-117">Caminho completo do arquivo, não incluindo a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="75a49-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="75a49-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="75a49-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75a49-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75a49-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="75a49-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="75a49-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75a49-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="75a49-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="75a49-122">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="75a49-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75a49-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="75a49-123">Remarks</span></span>

<span data-ttu-id="75a49-124">**Windows Server 2003:** Para recuperar a letra da unidade para o caminho do nome do arquivo, use o valor da propriedade **FileObject** para mapear para o evento [DiskIo \_ TypeGroup1](diskio-typegroup1.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="75a49-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [DiskIo\_TypeGroup1](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="75a49-125">No evento DiskIo \_ TypeGroup1, use os valores de propriedade **DiskNumber** e **ByteOffset** para mapear para o evento [SystemConfig \_ LogDisk](systemconfig-logdisk.md) correspondente (**ByteOffset** Maps para **StartOffset**).</span><span class="sxs-lookup"><span data-stu-id="75a49-125">From the DiskIo\_TypeGroup1 event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [SystemConfig\_LogDisk](systemconfig-logdisk.md) event (**ByteOffset** maps to **StartOffset**).</span></span> <span data-ttu-id="75a49-126">A propriedade **DriveLetterString** contém a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="75a49-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="75a49-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75a49-127">Requirements</span></span>



| <span data-ttu-id="75a49-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="75a49-128">Requirement</span></span> | <span data-ttu-id="75a49-129">Valor</span><span class="sxs-lookup"><span data-stu-id="75a49-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75a49-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75a49-130">Minimum supported client</span></span><br/> | <span data-ttu-id="75a49-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75a49-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75a49-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="75a49-132">Minimum supported server</span></span><br/> | <span data-ttu-id="75a49-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75a49-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75a49-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="75a49-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75a49-135">**FileIo**</span><span class="sxs-lookup"><span data-stu-id="75a49-135">**FileIo**</span></span>](fileio.md)
</dt> </dl>

 

 




