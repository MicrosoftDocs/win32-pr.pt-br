---
description: Representa uma entrada na lista de atributos.
ms.assetid: daa0c97d-2ebe-4e14-b1f8-e4be3075b13e
title: Estrutura de ATTRIBUTE_LIST_ENTRY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_LIST_ENTRY
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67ee65a22c9e880c76d3b250c4859077f471b018
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826130"
---
# <a name="attribute_list_entry-structure"></a><span data-ttu-id="41d63-103">Estrutura de entrada da \_ lista de atributos \_</span><span class="sxs-lookup"><span data-stu-id="41d63-103">ATTRIBUTE\_LIST\_ENTRY structure</span></span>

<span data-ttu-id="41d63-104">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="41d63-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="41d63-105">Representa uma entrada na lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="41d63-105">Represents an entry in the attribute list.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d63-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41d63-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_LIST_ENTRY {
  ATTRIBUTE_TYPE_CODE   AttributeTypeCode;
  USHORT                RecordLength;
  UCHAR                 AttributeNameLength;
  UCHAR                 AttributeNameOffset;
  VCN                   LowestVcn;
  MFT_SEGMENT_REFERENCE SegmentReference;
  USHORT                Reserved;
  WCHAR                 AttributeName[1];
} ATTRIBUTE_LIST_ENTRY, *PATTRIBUTE_LIST_ENTRY;
```



## <a name="members"></a><span data-ttu-id="41d63-107">Membros</span><span class="sxs-lookup"><span data-stu-id="41d63-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="41d63-108">**AttributeTypeCode**</span><span class="sxs-lookup"><span data-stu-id="41d63-108">**AttributeTypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-109">O código do tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="41d63-109">The attribute type code.</span></span>



| <span data-ttu-id="41d63-110">Valor</span><span class="sxs-lookup"><span data-stu-id="41d63-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="41d63-111">Significado</span><span class="sxs-lookup"><span data-stu-id="41d63-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="41d63-112"><dt>**$Standard \_ INFORMAÇÕES**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="41d63-113">Atributos de arquivo (como somente leitura e arquivo), carimbos de data/hora (como criação de arquivo e última modificação) e a contagem de vínculos físicos.</span><span class="sxs-lookup"><span data-stu-id="41d63-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="41d63-114"><dt>**$Attribute \_ LISTA**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="41d63-115">Uma lista de atributos que compõem o arquivo e a referência de arquivo do registro de arquivo MFT no qual cada atributo está localizado.</span><span class="sxs-lookup"><span data-stu-id="41d63-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="41d63-116"><dt>**$File \_ NOME**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="41d63-117">O nome do arquivo, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="41d63-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="41d63-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="41d63-119">Um identificador de objeto de 16 bytes atribuído pelo serviço de rastreamento de link.</span><span class="sxs-lookup"><span data-stu-id="41d63-119">An 16-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="41d63-120"><dt>**$Volume \_ NOME**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="41d63-121">Rótulo do volume.</span><span class="sxs-lookup"><span data-stu-id="41d63-121">The volume label.</span></span> <span data-ttu-id="41d63-122">Presente no arquivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="41d63-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="41d63-123"><dt>**$Volume \_**</dt> <dt>0X70</dt> de informações</span><span class="sxs-lookup"><span data-stu-id="41d63-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="41d63-124">As informações de volume.</span><span class="sxs-lookup"><span data-stu-id="41d63-124">The volume information.</span></span> <span data-ttu-id="41d63-125">Presente no arquivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="41d63-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="41d63-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="41d63-127">O conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="41d63-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="41d63-128"><dt>**$Index \_**</dt> <dt>0x90</dt> raiz</span><span class="sxs-lookup"><span data-stu-id="41d63-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="41d63-129">Usado para implementar a alocação de nome de arquivo para diretórios grandes.</span><span class="sxs-lookup"><span data-stu-id="41d63-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="41d63-130"><dt>**$Index \_**</dt> <dt>0XA0</dt> de alocação</span><span class="sxs-lookup"><span data-stu-id="41d63-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="41d63-131">Usado para implementar a alocação de nome de arquivo para diretórios grandes.</span><span class="sxs-lookup"><span data-stu-id="41d63-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="41d63-132"><dt>**$Bitmap**</dt> <dt>0xb0</dt></span><span class="sxs-lookup"><span data-stu-id="41d63-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="41d63-133">Um índice de bitmap para um diretório grande.</span><span class="sxs-lookup"><span data-stu-id="41d63-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="41d63-134"><dt>**$REPARSE \_**</dt> <dt>0XC0</dt> do ponto</span><span class="sxs-lookup"><span data-stu-id="41d63-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="41d63-135">Os dados do ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="41d63-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="41d63-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="41d63-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-137">O tamanho dessa estrutura, mais o buffer de nome opcional, em bytes.</span><span class="sxs-lookup"><span data-stu-id="41d63-137">The size of this structure, plus the optional name buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="41d63-138">**AttributeNameLength**</span><span class="sxs-lookup"><span data-stu-id="41d63-138">**AttributeNameLength**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-139">O tamanho do nome do atributo opcional, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="41d63-139">The size of the optional attribute name, in characters.</span></span> <span data-ttu-id="41d63-140">Se existir um nome, esse valor será diferente de zero e a estrutura será seguida imediatamente por uma cadeia de caracteres Unicode do número especificado.</span><span class="sxs-lookup"><span data-stu-id="41d63-140">If a name exists, this value is nonzero and the structure is followed immediately by a Unicode string of the specified number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="41d63-141">**AttributeNameOffset**</span><span class="sxs-lookup"><span data-stu-id="41d63-141">**AttributeNameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="41d63-142">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="41d63-143">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="41d63-143">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-144">O VCN (número de cluster virtual) mais baixo para este atributo.</span><span class="sxs-lookup"><span data-stu-id="41d63-144">The lowest virtual cluster number (VCN) for this attribute.</span></span> <span data-ttu-id="41d63-145">Esse membro é zero, a menos que o atributo exija vários segmentos de registro de arquivo e, a menos que essa entrada seja uma referência a um segmento diferente do primeiro.</span><span class="sxs-lookup"><span data-stu-id="41d63-145">This member is zero unless the attribute requires multiple file record segments and unless this entry is a reference to a segment other than the first one.</span></span> <span data-ttu-id="41d63-146">Nesse caso, esse valor é o VCN mais baixo que é descrito pelo segmento referenciado.</span><span class="sxs-lookup"><span data-stu-id="41d63-146">In this case, this value is the lowest VCN that is described by the referenced segment.</span></span>

</dd> <dt>

<span data-ttu-id="41d63-147">**SegmentReference**</span><span class="sxs-lookup"><span data-stu-id="41d63-147">**SegmentReference**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-148">O segmento de tabela de arquivos mestre (MFT) no qual o atributo reside.</span><span class="sxs-lookup"><span data-stu-id="41d63-148">The master file table (MFT) segment in which the attribute resides.</span></span> <span data-ttu-id="41d63-149">Consulte [**\_ \_ referência de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="41d63-149">See [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="41d63-150">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="41d63-150">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-151">Reservado.</span><span class="sxs-lookup"><span data-stu-id="41d63-151">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="41d63-152">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="41d63-152">**AttributeName**</span></span>
</dt> <dd>

<span data-ttu-id="41d63-153">O início do nome de atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="41d63-153">The start of the optional attribute name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41d63-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="41d63-154">Remarks</span></span>

<span data-ttu-id="41d63-155">A lista de atributos é uma lista ordenada de estruturas de **\_ \_ entrada de lista de atributos** alinhados por quadword.</span><span class="sxs-lookup"><span data-stu-id="41d63-155">The attributes list is an ordered list of quadword-aligned **ATTRIBUTE\_LIST\_ENTRY** structures.</span></span> <span data-ttu-id="41d63-156">Essa lista é ordenada primeiro pelo código de tipo de atributo e, em seguida, pelo nome do atributo (se presente).</span><span class="sxs-lookup"><span data-stu-id="41d63-156">This list is ordered first by the attribute type code and then by the attribute name (if present).</span></span> <span data-ttu-id="41d63-157">Dois atributos não podem ter o mesmo código de tipo, nome e VCN mais baixo.</span><span class="sxs-lookup"><span data-stu-id="41d63-157">No two attributes can have the same type code, name, and lowest VCN.</span></span> <span data-ttu-id="41d63-158">Portanto, pode haver no máximo um atributo para cada código de tipo sem um nome.</span><span class="sxs-lookup"><span data-stu-id="41d63-158">Therefore, there can be at most one attribute for each type code without a name.</span></span>

<span data-ttu-id="41d63-159">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="41d63-159">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="41d63-160">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="41d63-160">Note that there is no associated header file for this structure.</span></span>

## <a name="see-also"></a><span data-ttu-id="41d63-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="41d63-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d63-162">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="41d63-162">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
