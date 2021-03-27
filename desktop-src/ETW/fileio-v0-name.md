---
description: A classe de nome de V0 de FileIo \_ \_ é uma versão mais antiga da classe de tipo de evento para eventos de e/s de arquivo. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: dcbe37f2-6df0-41a5-b85f-dcd06cbd5901
title: Classe FileIo_V0_Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo_V0_Name
- FileIo_V0_Name.FileObject
- FileIo_V0_Name.FileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6e88d1b9b5b36815b1a833062c30e804e4db744a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662797"
---
# <a name="fileio_v0_name-class"></a><span data-ttu-id="f48d3-104">Classe de nome de \_ V0 FileIo \_</span><span class="sxs-lookup"><span data-stu-id="f48d3-104">FileIo\_V0\_Name class</span></span>

<span data-ttu-id="f48d3-105">A classe de **\_ \_ nome de V0 de FileIo** é uma versão mais antiga da classe de tipo de evento para eventos de e/s de arquivo.</span><span class="sxs-lookup"><span data-stu-id="f48d3-105">The **FileIo\_V0\_Name** class is an older version of the event type class for file I/O events.</span></span>

<span data-ttu-id="f48d3-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="f48d3-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f48d3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f48d3-107">Syntax</span></span>

``` syntax
[EventType(0), EventTypeName("Name")]
class FileIo_V0_Name : FileIo_V0
{
  uint32 FileObject;
  string FileName;
};
```

## <a name="members"></a><span data-ttu-id="f48d3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f48d3-108">Members</span></span>

<span data-ttu-id="f48d3-109">A classe de **\_ \_ nome V0 do FileIo** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f48d3-109">The **FileIo\_V0\_Name** class has these types of members:</span></span>

-   [<span data-ttu-id="f48d3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f48d3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f48d3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f48d3-111">Properties</span></span>

<span data-ttu-id="f48d3-112">A classe de **\_ \_ nome V0 de FileIo** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f48d3-112">The **FileIo\_V0\_Name** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f48d3-113">FileName</span><span class="sxs-lookup"><span data-stu-id="f48d3-113">FileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f48d3-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f48d3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f48d3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f48d3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f48d3-116">Qualificadores: WmiDataId (2), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="f48d3-116">Qualifiers: WmiDataId(2), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="f48d3-117">Caminho completo do arquivo, não incluindo a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="f48d3-117">Full path to the file, not including the drive letter.</span></span>

</dd> <dt>

<span data-ttu-id="f48d3-118">FileObject</span><span class="sxs-lookup"><span data-stu-id="f48d3-118">FileObject</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f48d3-119">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f48d3-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f48d3-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f48d3-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f48d3-121">Qualificadores: WmiDataId (1), ponteiro</span><span class="sxs-lookup"><span data-stu-id="f48d3-121">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f48d3-122">Corresponda o valor desse ponteiro ao valor do ponteiro **FileObject** em um evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) para determinar o tipo de operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="f48d3-122">Match the value of this pointer to the **FileObject** pointer value in a [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event to determine the type of I/O operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f48d3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f48d3-123">Remarks</span></span>

<span data-ttu-id="f48d3-124">**Windows Server 2003:** Para recuperar a letra da unidade para o caminho do nome do arquivo, use o valor da propriedade **FileObject** para mapear para o evento [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="f48d3-124">**Windows Server 2003:** To retrieve the drive letter for the file name path, use the **FileObject** property value to map to the corresponding [**DiskIo\_TypeGroup1**](diskio-typegroup1.md) event.</span></span> <span data-ttu-id="f48d3-125">No evento **DiskIo \_ TypeGroup1** , use os valores de propriedade **DiskNumber** e **ByteOffset** para mapear para o evento [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) correspondente.</span><span class="sxs-lookup"><span data-stu-id="f48d3-125">From the **DiskIo\_TypeGroup1** event, use the **DiskNumber** and **ByteOffset** property values to map to the corresponding [**SystemConfig\_LogDisk**](systemconfig-logdisk.md) event.</span></span> <span data-ttu-id="f48d3-126">A propriedade **DriveLetterString** contém a letra da unidade.</span><span class="sxs-lookup"><span data-stu-id="f48d3-126">The **DriveLetterString** property contains the drive letter.</span></span>

## <a name="requirements"></a><span data-ttu-id="f48d3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f48d3-127">Requirements</span></span>



| <span data-ttu-id="f48d3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f48d3-128">Requirement</span></span> | <span data-ttu-id="f48d3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="f48d3-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f48d3-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f48d3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f48d3-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f48d3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f48d3-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f48d3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f48d3-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f48d3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f48d3-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="f48d3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48d3-135">**\_V0 FileIo**</span><span class="sxs-lookup"><span data-stu-id="f48d3-135">**FileIo\_V0**</span></span>](fileio-v0.md)
</dt> </dl>

 

 




