---
description: Representa um atributo de nome de arquivo. Um arquivo tem um atributo de nome de arquivo para cada diretório no qual é inserido.
ms.assetid: 54458eee-b786-446c-80bd-213c13bdeb4a
title: Estrutura de FILE_NAME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILE_NAME
api_type:
- NA
api_location: ''
ms.openlocfilehash: 609725c21f0c0811a4222cd9dfd662b3e25673f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010089"
---
# <a name="file_name-structure"></a><span data-ttu-id="26954-104">Estrutura de nome de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="26954-104">FILE\_NAME structure</span></span>

<span data-ttu-id="26954-105">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="26954-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="26954-106">Representa um atributo de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="26954-106">Represents a file name attribute.</span></span> <span data-ttu-id="26954-107">Um arquivo tem um atributo de nome de arquivo para cada diretório no qual é inserido.</span><span class="sxs-lookup"><span data-stu-id="26954-107">A file has one file name attribute for every directory it is entered into.</span></span>

## <a name="syntax"></a><span data-ttu-id="26954-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26954-108">Syntax</span></span>


```C++
typedef struct _FILE_NAME {
  FILE_REFERENCE ParentDirectory;
  UCHAR          Reserved[0x38];
  UCHAR          FileNameLength;
  UCHAR          Flags;
  WCHAR          FileName[1];
} FILE_NAME, *PFILE_NAME;
```



## <a name="members"></a><span data-ttu-id="26954-109">Membros</span><span class="sxs-lookup"><span data-stu-id="26954-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="26954-110">**ParentDirectory**</span><span class="sxs-lookup"><span data-stu-id="26954-110">**ParentDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="26954-111">Uma referência de arquivo para o diretório que indexa para esse nome.</span><span class="sxs-lookup"><span data-stu-id="26954-111">A file reference to the directory that indexes to this name.</span></span> <span data-ttu-id="26954-112">Consulte [**\_ \_ referência de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="26954-112">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="26954-113">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="26954-113">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="26954-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="26954-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="26954-115">**FileNameLength**</span><span class="sxs-lookup"><span data-stu-id="26954-115">**FileNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="26954-116">O comprimento do nome do arquivo, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="26954-116">The length of the file name, in Unicode characters.</span></span>

</dd> <dt>

<span data-ttu-id="26954-117">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="26954-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="26954-118">Os sinalizadores de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="26954-118">The file name flags.</span></span>

<dl> <dt>

<span data-ttu-id="26954-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>Do **arquivo \_ NOME \_ NTFS** (0x01)</span><span class="sxs-lookup"><span data-stu-id="26954-119"><span id="FILE_NAME_NTFS"></span><span id="file_name_ntfs"></span>**FILE\_NAME\_NTFS** (0x01)</span></span>
</dt> <dt>

<span data-ttu-id="26954-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>Do **arquivo \_ NOME \_ dos** (0x02)</span><span class="sxs-lookup"><span data-stu-id="26954-120"><span id="FILE_NAME_DOS"></span><span id="file_name_dos"></span>**FILE\_NAME\_DOS** (0x02)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="26954-121">**FileName**</span><span class="sxs-lookup"><span data-stu-id="26954-121">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="26954-122">O primeiro caractere do nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="26954-122">The first character of the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26954-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="26954-123">Remarks</span></span>

<span data-ttu-id="26954-124">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="26954-124">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="26954-125">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="26954-125">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="26954-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="26954-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26954-127">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="26954-127">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
