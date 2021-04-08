---
description: Contém as informações de reconhecimento do sistema de arquivos em disco armazenadas no setor de inicialização de volumes (setor de disco lógico zero).
ms.assetid: d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac
title: Estrutura de FILE_SYSTEM_RECOGNITION_STRUCTURE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_SYSTEM_RECOGNITION_STRUCTURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c542b2b9ee1cd1696c7c95797c7df20aa02180cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010781"
---
# <a name="file_system_recognition_structure-structure"></a><span data-ttu-id="dc2d3-103">\_Estrutura da \_ estrutura de reconhecimento do sistema de arquivos \_</span><span class="sxs-lookup"><span data-stu-id="dc2d3-103">FILE\_SYSTEM\_RECOGNITION\_STRUCTURE structure</span></span>

<span data-ttu-id="dc2d3-104">Contém as informações de reconhecimento do sistema de arquivos em disco armazenadas no setor de inicialização do volume (setor de disco lógico zero).</span><span class="sxs-lookup"><span data-stu-id="dc2d3-104">Contains the on-disk file system recognition information stored in the volume's boot sector (logical disk sector zero).</span></span>

<span data-ttu-id="dc2d3-105">Esta é uma estrutura de dados definida internamente não disponível em um cabeçalho público e é fornecida aqui para desenvolvedores de sistema de arquivos que desejam aproveitar o reconhecimento do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-105">This is an internally-defined data structure not available in a public header and is provided here for file system developers who want to take advantage of file system recognition.</span></span> <span data-ttu-id="dc2d3-106">Para obter mais informações, consulte [reconhecimento do sistema de arquivos](file-system-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="dc2d3-106">For more information, see [File System Recognition](file-system-recognition.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2d3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc2d3-107">Syntax</span></span>


```C++
typedef struct _FILE_SYSTEM_RECOGNITION_STRUCTURE {
  UCHAR  Jmp[3];
  UCHAR  FsName[8];
  UCHAR  MustBeZero[5];
  ULONG  Identifier;
  USHORT Length;
  USHORT Checksum;
} FILE_SYSTEM_RECOGNITION_STRUCTURE;
```



## <a name="members"></a><span data-ttu-id="dc2d3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="dc2d3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc2d3-109">**JMP**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-109">**Jmp**</span></span>
</dt> <dd>

<span data-ttu-id="dc2d3-110">A instrução JMP.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-110">The JMP instruction.</span></span> <span data-ttu-id="dc2d3-111">Esse membro de dados não está incluído no valor contido no membro de dados de **soma de verificação** .</span><span class="sxs-lookup"><span data-stu-id="dc2d3-111">This data member is not included in the value contained in the **Checksum** data member.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d3-112">**FsName**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-112">**FsName**</span></span>
</dt> <dd>

<span data-ttu-id="dc2d3-113">O nome do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-113">The file system name.</span></span> <span data-ttu-id="dc2d3-114">Essa é uma sequência de 8 caracteres ASCII que representa o nome legível não localizável do sistema de arquivos com o qual o volume é formatado.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-114">This is a sequence of 8 ASCII characters that represents the nonlocalizable human-readable name of the file system the volume is formatted with.</span></span>

<span data-ttu-id="dc2d3-115">Essa cadeia de caracteres está no mesmo local que o nome do sistema de arquivos OEM em um disco com uma estrutura de bloco de parâmetros do BIOS (BPB) normal.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-115">This string is in the same place as the OEM file system name on a disk with a normal BIOS parameter block (BPB) structure.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d3-116">**MustBeZero**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-116">**MustBeZero**</span></span>
</dt> <dd>

<span data-ttu-id="dc2d3-117">Espaço reservado que contém todos os zeros.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-117">Reserved space that contains all zeros.</span></span>

<span data-ttu-id="dc2d3-118">Esse membro de dados se sobrepõe ao que normalmente são os seguintes membros de dados em um BPB:</span><span class="sxs-lookup"><span data-stu-id="dc2d3-118">This data member overlaps what normally are the following data members in a BPB:</span></span>

-   <span data-ttu-id="dc2d3-119">**BytesPerSector**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-119">**BytesPerSector**</span></span>
-   <span data-ttu-id="dc2d3-120">**SectorsPerCluster**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-120">**SectorsPerCluster**</span></span>
-   <span data-ttu-id="dc2d3-121">**ReservedSectorCount**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-121">**ReservedSectorCount**</span></span>

<span data-ttu-id="dc2d3-122">Como esses membros de dados são definidos como zero, isso deve ser suficiente para fazer com que o OSs anterior conclua que esse não é um BPB válido e, portanto, reconhece o volume.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-122">Because these data members are set to zero, this should be sufficient to cause earlier OSs to conclude that this is not a valid BPB and therefore recognize the volume.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d3-123">**Identificador**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-123">**Identifier**</span></span>
</dt> <dd>

<span data-ttu-id="dc2d3-124">Identificador de estrutura.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-124">A structure identifier.</span></span> <span data-ttu-id="dc2d3-125">Deve conter o valor 0x53525346 organizado em ordem de byte little-endian.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-125">Must contain the value 0x53525346 arranged in little-endian byte order.</span></span>

<span data-ttu-id="dc2d3-126">Neste ponto da estrutura, os dados são alinhados a 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="dc2d3-126">At this point in the structure, the data is aligned to 16 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d3-127">**Comprimento**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-127">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="dc2d3-128">O número de bytes nessa estrutura, desde o início até o fim, incluindo o membro de dados **JMP** .</span><span class="sxs-lookup"><span data-stu-id="dc2d3-128">The number of bytes in this structure, from the beginning to the end, including the **Jmp** data member.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d3-129">**Soma**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-129">**Checksum**</span></span>
</dt> <dd>

<span data-ttu-id="dc2d3-130">Uma soma de verificação de dois bytes calculada sobre os bytes começando no membro de dados **FsName** e terminando no último byte dessa estrutura, excluindo os membros de dados **JMP** e **checksum** .</span><span class="sxs-lookup"><span data-stu-id="dc2d3-130">A two-byte checksum calculated over the bytes starting at the **FsName** data member and ending at the last byte of this structure, excluding the **Jmp** and **Checksum** data members.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc2d3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc2d3-131">Requirements</span></span>



| <span data-ttu-id="dc2d3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc2d3-132">Requirement</span></span> | <span data-ttu-id="dc2d3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="dc2d3-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="dc2d3-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc2d3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dc2d3-135">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="dc2d3-135">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="dc2d3-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dc2d3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dc2d3-137">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="dc2d3-137">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dc2d3-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc2d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc2d3-139">Calculando uma soma de verificação de reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="dc2d3-139">Computing a File System Recognition Checksum</span></span>](computing-a-file-system-recognition-checksum.md)
</dt> <dt>

[<span data-ttu-id="dc2d3-140">Reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="dc2d3-140">File System Recognition</span></span>](file-system-recognition.md)
</dt> <dt>

[<span data-ttu-id="dc2d3-141">**\_informações de \_ reconhecimento do sistema de arquivos \_**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-141">**FILE\_SYSTEM\_RECOGNITION\_INFORMATION**</span></span>](/windows/desktop/api/WinIoCtl/ns-winioctl-file_system_recognition_information)
</dt> <dt>

[<span data-ttu-id="dc2d3-142">**\_reconhecimento do \_ sistema de arquivos de consulta fsctl \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dc2d3-142">**FSCTL\_QUERY\_FILE\_SYSTEM\_RECOGNITION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_file_system_recognition)
</dt> </dl>

 

