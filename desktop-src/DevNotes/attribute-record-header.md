---
description: Representa um registro de atributo.
ms.assetid: f9d9458c-b179-441c-9f62-ff0ac2f75329
title: Estrutura de ATTRIBUTE_RECORD_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ATTRIBUTE_RECORD_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae710ca04f11cb70c1bad9b5e6fec25f8fb5e94f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826129"
---
# <a name="attribute_record_header-structure"></a><span data-ttu-id="3da28-103">Estrutura de cabeçalho de \_ registro de atributo \_</span><span class="sxs-lookup"><span data-stu-id="3da28-103">ATTRIBUTE\_RECORD\_HEADER structure</span></span>

<span data-ttu-id="3da28-104">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="3da28-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="3da28-105">Representa um registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-105">Represents an attribute record.</span></span>

## <a name="syntax"></a><span data-ttu-id="3da28-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3da28-106">Syntax</span></span>


```C++
typedef struct _ATTRIBUTE_RECORD_HEADER {
  ATTRIBUTE_TYPE_CODE TypeCode;
  ULONG               RecordLength;
  UCHAR               FormCode;
  UCHAR               NameLength;
  USHORT              NameOffset;
  USHORT              Flags;
  USHORT              Instance;
  union {
    struct {
      ULONG  ValueLength;
      USHORT ValueOffset;
      UCHAR  Reserved[2];
    } Resident;
    struct {
      VCN      LowestVcn;
      VCN      HighestVcn;
      USHORT   MappingPairsOffset;
      UCHAR    Reserved[6];
      LONGLONG AllocatedLength;
      LONGLONG FileSize;
      LONGLONG ValidDataLength;
      LONGLONG TotalAllocated;
    } Nonresident;
  } Form;
} ATTRIBUTE_RECORD_HEADER, *PATTRIBUTE_RECORD_HEADER;
```



## <a name="members"></a><span data-ttu-id="3da28-107">Membros</span><span class="sxs-lookup"><span data-stu-id="3da28-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="3da28-108">**TypeCode**</span><span class="sxs-lookup"><span data-stu-id="3da28-108">**TypeCode**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-109">O código do tipo de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-109">The attribute type code.</span></span>



| <span data-ttu-id="3da28-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3da28-110">Value</span></span>                                                                                                                                                                                                                                           | <span data-ttu-id="3da28-111">Significado</span><span class="sxs-lookup"><span data-stu-id="3da28-111">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_STANDARD_INFORMATION"></span><span id="_standard_information"></span><dl> <span data-ttu-id="3da28-112"><dt>**$Standard \_ INFORMAÇÕES**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-112"><dt>**$STANDARD\_INFORMATION**</dt> <dt>0x10</dt></span></span> </dl> | <span data-ttu-id="3da28-113">Atributos de arquivo (como somente leitura e arquivo), carimbos de data/hora (como criação de arquivo e última modificação) e a contagem de vínculos físicos.</span><span class="sxs-lookup"><span data-stu-id="3da28-113">File attributes (such as read-only and archive), time stamps (such as file creation and last modified), and the hard link count.</span></span><br/> |
| <span id="_ATTRIBUTE_LIST"></span><span id="_attribute_list"></span><dl> <span data-ttu-id="3da28-114"><dt>**$Attribute \_ LISTA**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-114"><dt>**$ATTRIBUTE\_LIST**</dt> <dt>0x20</dt></span></span> </dl>                   | <span data-ttu-id="3da28-115">Uma lista de atributos que compõem o arquivo e a referência de arquivo do registro de arquivo MFT no qual cada atributo está localizado.</span><span class="sxs-lookup"><span data-stu-id="3da28-115">A list of attributes that make up the file and the file reference of the MFT file record in which each attribute is located.</span></span><br/>     |
| <span id="_FILE_NAME"></span><span id="_file_name"></span><dl> <span data-ttu-id="3da28-116"><dt>**$File \_ NOME**</dt> <dt>0x30</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-116"><dt>**$FILE\_NAME**</dt> <dt>0x30</dt></span></span> </dl>                                  | <span data-ttu-id="3da28-117">O nome do arquivo, em caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="3da28-117">The name of the file, in Unicode characters.</span></span><br/>                                                                                     |
| <span id="_OBJECT_ID"></span><span id="_object_id"></span><dl> <span data-ttu-id="3da28-118"><dt>**$Object \_ ID**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-118"><dt>**$OBJECT\_ID**</dt> <dt>0x40</dt></span></span> </dl>                                  | <span data-ttu-id="3da28-119">Um identificador de objeto de 64 bytes atribuído pelo serviço de rastreamento de link.</span><span class="sxs-lookup"><span data-stu-id="3da28-119">An 64-byte object identifier assigned by the link-tracking service.</span></span><br/>                                                              |
| <span id="_VOLUME_NAME"></span><span id="_volume_name"></span><dl> <span data-ttu-id="3da28-120"><dt>**$Volume \_ NOME**</dt> <dt>0x60</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-120"><dt>**$VOLUME\_NAME**</dt> <dt>0x60</dt></span></span> </dl>                            | <span data-ttu-id="3da28-121">Rótulo do volume.</span><span class="sxs-lookup"><span data-stu-id="3da28-121">The volume label.</span></span> <span data-ttu-id="3da28-122">Presente no arquivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="3da28-122">Present in the $Volume file.</span></span><br/>                                                                                   |
| <span id="_VOLUME_INFORMATION"></span><span id="_volume_information"></span><dl> <span data-ttu-id="3da28-123"><dt>**$Volume \_**</dt> <dt>0X70</dt> de informações</span><span class="sxs-lookup"><span data-stu-id="3da28-123"><dt>**$VOLUME\_INFORMATION**</dt> <dt>0x70</dt></span></span> </dl>       | <span data-ttu-id="3da28-124">As informações de volume.</span><span class="sxs-lookup"><span data-stu-id="3da28-124">The volume information.</span></span> <span data-ttu-id="3da28-125">Presente no arquivo de $Volume.</span><span class="sxs-lookup"><span data-stu-id="3da28-125">Present in the $Volume file.</span></span><br/>                                                                             |
| <span id="_DATA"></span><span id="_data"></span><dl> <span data-ttu-id="3da28-126"><dt>**$Data**</dt> <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-126"><dt>**$DATA**</dt> <dt>0x80</dt></span></span> </dl>                                                  | <span data-ttu-id="3da28-127">O conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="3da28-127">The contents of the file.</span></span><br/>                                                                                                        |
| <span id="_INDEX_ROOT"></span><span id="_index_root"></span><dl> <span data-ttu-id="3da28-128"><dt>**$Index \_**</dt> <dt>0x90</dt> raiz</span><span class="sxs-lookup"><span data-stu-id="3da28-128"><dt>**$INDEX\_ROOT**</dt> <dt>0x90</dt></span></span> </dl>                               | <span data-ttu-id="3da28-129">Usado para implementar a alocação de nome de arquivo para diretórios grandes.</span><span class="sxs-lookup"><span data-stu-id="3da28-129">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_INDEX_ALLOCATION"></span><span id="_index_allocation"></span><dl> <span data-ttu-id="3da28-130"><dt>**$Index \_**</dt> <dt>0XA0</dt> de alocação</span><span class="sxs-lookup"><span data-stu-id="3da28-130"><dt>**$INDEX\_ALLOCATION**</dt> <dt>0xA0</dt></span></span> </dl>             | <span data-ttu-id="3da28-131">Usado para implementar a alocação de nome de arquivo para diretórios grandes.</span><span class="sxs-lookup"><span data-stu-id="3da28-131">Used to implement filename allocation for large directories.</span></span><br/>                                                                     |
| <span id="_BITMAP"></span><span id="_bitmap"></span><dl> <span data-ttu-id="3da28-132"><dt>**$Bitmap**</dt> <dt>0xb0</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-132"><dt>**$BITMAP**</dt> <dt>0xB0</dt></span></span> </dl>                                            | <span data-ttu-id="3da28-133">Um índice de bitmap para um diretório grande.</span><span class="sxs-lookup"><span data-stu-id="3da28-133">A bitmap index for a large directory.</span></span><br/>                                                                                            |
| <span id="_REPARSE_POINT"></span><span id="_reparse_point"></span><dl> <span data-ttu-id="3da28-134"><dt>**$REPARSE \_**</dt> <dt>0XC0</dt> do ponto</span><span class="sxs-lookup"><span data-stu-id="3da28-134"><dt>**$REPARSE\_POINT**</dt> <dt>0xC0</dt></span></span> </dl>                      | <span data-ttu-id="3da28-135">Os dados do ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="3da28-135">The reparse point data.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="3da28-136">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="3da28-136">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-137">O tamanho do registro de atributo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-137">The size of the attribute record, in bytes.</span></span> <span data-ttu-id="3da28-138">Esse valor reflete o tamanho necessário para a variante de registro e é sempre arredondado para o limite de quadword mais próximo.</span><span class="sxs-lookup"><span data-stu-id="3da28-138">This value reflects the required size for the record variant and is always rounded to the nearest quadword boundary.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-139">**FormCode**</span><span class="sxs-lookup"><span data-stu-id="3da28-139">**FormCode**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-140">O código de formulário de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-140">The attribute form code.</span></span>



| <span data-ttu-id="3da28-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3da28-141">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="3da28-142">Significado</span><span class="sxs-lookup"><span data-stu-id="3da28-142">Meaning</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="RESIDENT_FORM"></span><span id="resident_form"></span><dl> <span data-ttu-id="3da28-143"><dt>**Residente \_ na FORMULÁRIO**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-143"><dt>**RESIDENT\_FORM**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="3da28-144">O valor está contido no registro de arquivo e imediatamente segue o cabeçalho de registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-144">The value is contained in the file record and immediately follows the attribute record header.</span></span><br/> |
| <span id="NONRESIDENT_FORM"></span><span id="nonresident_form"></span><dl> <span data-ttu-id="3da28-145">Não <dt>**residente \_ FORMULÁRIO**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="3da28-145"><dt>**NONRESIDENT\_FORM**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="3da28-146">O valor está contido em outros setores no disco.</span><span class="sxs-lookup"><span data-stu-id="3da28-146">The value is contained in other sectors on the disk.</span></span><br/>                                           |



 

</dd> <dt>

<span data-ttu-id="3da28-147">**NameLength**</span><span class="sxs-lookup"><span data-stu-id="3da28-147">**NameLength**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-148">O tamanho do nome de atributo opcional, em caracteres, ou 0 se não houver nenhum nome de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-148">The size of the optional attribute name, in characters, or 0 if there is no attribute name.</span></span> <span data-ttu-id="3da28-149">O comprimento máximo do nome de atributo é de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="3da28-149">The maximum attribute name length is 255 characters.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-150">**NameOffset**</span><span class="sxs-lookup"><span data-stu-id="3da28-150">**NameOffset**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-151">O deslocamento do nome do atributo desde o início do registro de atributo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-151">The offset of the attribute name from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="3da28-152">Se o membro **NameLength** for 0, esse membro será indefinido.</span><span class="sxs-lookup"><span data-stu-id="3da28-152">If the **NameLength** member is 0, this member is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-153">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="3da28-153">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-154">Os sinalizadores de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-154">The attribute flags.</span></span>

<dl> <dt>

<span data-ttu-id="3da28-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**Atributo \_ \_ \_ Máscara de compactação de sinalizador** (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="3da28-155"><span id="ATTRIBUTE_FLAG_COMPRESSION_MASK"></span><span id="attribute_flag_compression_mask"></span>**ATTRIBUTE\_FLAG\_COMPRESSION\_MASK** (0x00FF)</span></span>
</dt> <dt>

<span data-ttu-id="3da28-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**Atributo \_ SINALIZAr \_ esparso** (0x8000)</span><span class="sxs-lookup"><span data-stu-id="3da28-156"><span id="ATTRIBUTE_FLAG_SPARSE"></span><span id="attribute_flag_sparse"></span>**ATTRIBUTE\_FLAG\_SPARSE** (0x8000)</span></span>
</dt> <dt>

<span data-ttu-id="3da28-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**Atributo \_ SINALIZAr \_ criptografado** (0x4000)</span><span class="sxs-lookup"><span data-stu-id="3da28-157"><span id="ATTRIBUTE_FLAG_ENCRYPTED"></span><span id="attribute_flag_encrypted"></span>**ATTRIBUTE\_FLAG\_ENCRYPTED** (0x4000)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3da28-158">**Instância**</span><span class="sxs-lookup"><span data-stu-id="3da28-158">**Instance**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-159">A instância exclusiva para esse atributo no registro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3da28-159">The unique instance for this attribute in the file record.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-160">**Isolada**</span><span class="sxs-lookup"><span data-stu-id="3da28-160">**Form**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-161">Se o membro **FormCode** for \_ um formulário residente, a União será uma estrutura **residente** .</span><span class="sxs-lookup"><span data-stu-id="3da28-161">If the **FormCode** member is RESIDENT\_FORM, the union is a **Resident** structure.</span></span> <span data-ttu-id="3da28-162">Se **FormCode** for \_ um formulário não residente, Union será uma estrutura não **residente** .</span><span class="sxs-lookup"><span data-stu-id="3da28-162">If **FormCode** is NONRESIDENT\_FORM, the union is a **Nonresident** structure.</span></span>

<dl> <dt>

<span data-ttu-id="3da28-163">**Ponteiro**</span><span class="sxs-lookup"><span data-stu-id="3da28-163">**Resident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da28-164">**ValueLength**</span><span class="sxs-lookup"><span data-stu-id="3da28-164">**ValueLength**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-165">O tamanho do valor do atributo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-165">The size of the attribute value, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-166">**ValueOffset**</span><span class="sxs-lookup"><span data-stu-id="3da28-166">**ValueOffset**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-167">O deslocamento para o valor do início do registro de atributo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-167">The offset to the value from the start of the attribute record, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-168">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3da28-168">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-169">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3da28-169">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3da28-170">**Não residente**</span><span class="sxs-lookup"><span data-stu-id="3da28-170">**Nonresident**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3da28-171">**LowestVcn**</span><span class="sxs-lookup"><span data-stu-id="3da28-171">**LowestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-172">O número mais baixo do cluster virtual (VCN) coberto por este registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-172">The lowest virtual cluster number (VCN) covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-173">**HighestVcn**</span><span class="sxs-lookup"><span data-stu-id="3da28-173">**HighestVcn**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-174">O VCN mais alto coberto por este registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-174">The highest VCN covered by this attribute record.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-175">**MappingPairsOffset**</span><span class="sxs-lookup"><span data-stu-id="3da28-175">**MappingPairsOffset**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-176">O deslocamento para a matriz de pares de mapeamento desde o início do registro de atributo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-176">The offset to the mapping pairs array from the start of the attribute record, in bytes.</span></span> <span data-ttu-id="3da28-177">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="3da28-177">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-178">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="3da28-178">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-179">Reservado.</span><span class="sxs-lookup"><span data-stu-id="3da28-179">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-180">**AllocatedLength**</span><span class="sxs-lookup"><span data-stu-id="3da28-180">**AllocatedLength**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-181">O tamanho alocado do arquivo, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-181">The allocated size of the file, in bytes.</span></span> <span data-ttu-id="3da28-182">Esse valor é um múltiplo par do tamanho do cluster.</span><span class="sxs-lookup"><span data-stu-id="3da28-182">This value is an even multiple of the cluster size.</span></span> <span data-ttu-id="3da28-183">Esse membro não será válido se o membro **LowestVcn** for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3da28-183">This member is not valid if the **LowestVcn** member is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-184">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="3da28-184">**FileSize**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-185">O tamanho do arquivo (byte mais alto que pode ser lido mais 1), em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-185">The file size (highest byte that can be read plus 1), in bytes.</span></span> <span data-ttu-id="3da28-186">Esse membro não será válido se **LowestVcn** for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3da28-186">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-187">**ValidDataLength**</span><span class="sxs-lookup"><span data-stu-id="3da28-187">**ValidDataLength**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-188">O comprimento de dados válido (mais alto byte inicializado mais 1), em bytes.</span><span class="sxs-lookup"><span data-stu-id="3da28-188">The valid data length (highest initialized byte plus 1), in bytes.</span></span> <span data-ttu-id="3da28-189">Esse valor é arredondado para o limite de cluster mais próximo.</span><span class="sxs-lookup"><span data-stu-id="3da28-189">This value is rounded to the nearest cluster boundary.</span></span> <span data-ttu-id="3da28-190">Esse membro não será válido se **LowestVcn** for diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="3da28-190">This member is not valid if **LowestVcn** is nonzero.</span></span>

</dd> <dt>

<span data-ttu-id="3da28-191">**TotalAllocated**</span><span class="sxs-lookup"><span data-stu-id="3da28-191">**TotalAllocated**</span></span>
</dt> <dd>

<span data-ttu-id="3da28-192">O total alocado para o arquivo (a soma dos clusters alocados).</span><span class="sxs-lookup"><span data-stu-id="3da28-192">The total allocated for the file (the sum of the allocated clusters).</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3da28-193">Comentários</span><span class="sxs-lookup"><span data-stu-id="3da28-193">Remarks</span></span>

<span data-ttu-id="3da28-194">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3da28-194">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="3da28-195">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="3da28-195">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="3da28-196">Os registros de atributo são sempre alinhados em um limite de quadword.</span><span class="sxs-lookup"><span data-stu-id="3da28-196">Attribute records are always aligned on a quadword boundary.</span></span>

<span data-ttu-id="3da28-197">Se o atributo não for residente, o cabeçalho de registro de atributo conterá uma lista de informações de recuperação que fornece um mapeamento entre o VCN e o número de cluster lógico (LCN) para o atributo.</span><span class="sxs-lookup"><span data-stu-id="3da28-197">If the attribute is nonresident, the attribute record header contains a list of retrieval information that provides a mapping between VCN and logical cluster number (LCN) for the attribute.</span></span> <span data-ttu-id="3da28-198">Se as informações de recuperação não couberem no segmento de arquivo base, elas poderão ser armazenadas em um segmento de registro de arquivo externo por si só.</span><span class="sxs-lookup"><span data-stu-id="3da28-198">If the retrieval information does not fit in the base file segment, it can be stored in an external file record segment by itself.</span></span> <span data-ttu-id="3da28-199">Se ainda não couber em um segmento de registro de arquivo externo, há uma provisão na lista de atributos para conter várias entradas para um atributo que requer informações adicionais de recuperação.</span><span class="sxs-lookup"><span data-stu-id="3da28-199">If it still does not fit into one external file record segment, there is a provision in the attribute list to contain multiple entries for an attribute that requires additional retrieval information.</span></span>

<span data-ttu-id="3da28-200">A matriz de pares de mapeamento é armazenada em um formato compactado e pressupõe que as informações sejam descompactadas e armazenadas em cache pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="3da28-200">The mapping pairs array is stored in a compressed form and assumes that the information is decompressed and cached by the system.</span></span> <span data-ttu-id="3da28-201">Ele consiste em uma série de pares NextVcn/CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="3da28-201">It consists of a series of NextVcn/CurrentLcn pairs.</span></span> <span data-ttu-id="3da28-202">Por exemplo, se um arquivo tiver uma única execução de 8 clusters começando no LCN 128 e o arquivo iniciar em LowestVcn 0, a matriz de pares de mapeamento terá apenas uma entrada, que é NextVcn = 8 e CurrentLcn = 128.</span><span class="sxs-lookup"><span data-stu-id="3da28-202">For example, if a file has a single run of 8 clusters starting at LCN 128 and the file starts at LowestVcn 0, then the mapping pairs array has just one entry, which is NextVcn=8 and CurrentLcn=128.</span></span> <span data-ttu-id="3da28-203">A matriz é um fluxo de bytes que armazena as alterações nas variáveis de trabalho quando processadas sequencialmente.</span><span class="sxs-lookup"><span data-stu-id="3da28-203">The array is a byte stream that stores the changes to the working variables when processed sequentially.</span></span> <span data-ttu-id="3da28-204">O fluxo de bytes deve ser interpretado como um fluxo de percurso de terminação zero, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3da28-204">The byte stream is to be interpreted as a zero-terminated stream of triples, as follows:</span></span>

<span data-ttu-id="3da28-205">contagem byte = *v* + (*l* \* 16)</span><span class="sxs-lookup"><span data-stu-id="3da28-205">count byte = *v* + (*l* \* 16)</span></span>

<span data-ttu-id="3da28-206">em que *v* é o número de bytes de VCN de ordem baixa alterados e *l* é o número de bytes de LCN de ordem baixa alterados.</span><span class="sxs-lookup"><span data-stu-id="3da28-206">where *v* is the number of changed low-order VCN bytes and *l* is the number of changed low-order LCN bytes.</span></span>

<span data-ttu-id="3da28-207">O algoritmo de descompactação é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="3da28-207">The decompression algorithm is as follows:</span></span>

1.  <span data-ttu-id="3da28-208">Inicialize NextVcn `Attribute->LowestVcn` e CurrentLcn como 0.</span><span class="sxs-lookup"><span data-stu-id="3da28-208">Initialize NextVcn to `Attribute->LowestVcn` and CurrentLcn to 0.</span></span>
2.  <span data-ttu-id="3da28-209">Inicialize o ponteiro de fluxo de bytes para `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset` .</span><span class="sxs-lookup"><span data-stu-id="3da28-209">Initialize the byte stream pointer to `(PCHAR)Attribute + Attribute->AttributeForm->Nonresident->MappingPairsOffset`.</span></span>
3.  <span data-ttu-id="3da28-210">Defina CurrentVcn como NextVcn.</span><span class="sxs-lookup"><span data-stu-id="3da28-210">Set CurrentVcn to NextVcn.</span></span>
4.  <span data-ttu-id="3da28-211">Leia o próximo byte do fluxo.</span><span class="sxs-lookup"><span data-stu-id="3da28-211">Read the next byte from the stream.</span></span> <span data-ttu-id="3da28-212">Se for 0, interrompa; caso contrário, extraia o *v* e o *l* conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3da28-212">If it is 0, then break; else extract *v* and *l* as previously described.</span></span>
5.  <span data-ttu-id="3da28-213">Interprete os próximos *v* bytes como uma quantidade assinada, com o byte de ordem inferior primeiro.</span><span class="sxs-lookup"><span data-stu-id="3da28-213">Interpret the next *v* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="3da28-214">Desembale o registro de ti estendido em 64 bits e adicione-o a NextVcn.</span><span class="sxs-lookup"><span data-stu-id="3da28-214">Unpack it sign-extended into 64 bits and add it to NextVcn.</span></span>
6.  <span data-ttu-id="3da28-215">Interprete os próximos *l* bytes como uma quantidade assinada, com o byte de ordem inferior primeiro.</span><span class="sxs-lookup"><span data-stu-id="3da28-215">Interpret the next *l* bytes as a signed quantity, with the low-order byte first.</span></span> <span data-ttu-id="3da28-216">Desembale o registro de ti estendido em 64 bits e adicione-o a CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="3da28-216">Unpack it sign-extended into 64 bits and add it to CurrentLcn.</span></span> <span data-ttu-id="3da28-217">Se isso produzir um CurrentLcn de 0, o VCNs de CurrentVcn para NextVcn – 1 não será alocado.</span><span class="sxs-lookup"><span data-stu-id="3da28-217">If this produces a CurrentLcn of 0, then the VCNs from CurrentVcn to NextVcn–1 are unallocated.</span></span>
7.  <span data-ttu-id="3da28-218">Atualize as informações de mapeamento em cache de CurrentVcn, NextVcn e CurrentLcn.</span><span class="sxs-lookup"><span data-stu-id="3da28-218">Update the cached mapping information from CurrentVcn, NextVcn, and CurrentLcn.</span></span>
8.  <span data-ttu-id="3da28-219">Vá para a etapa 3.</span><span class="sxs-lookup"><span data-stu-id="3da28-219">Go to step 3.</span></span>

## <a name="see-also"></a><span data-ttu-id="3da28-220">Confira também</span><span class="sxs-lookup"><span data-stu-id="3da28-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3da28-221">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="3da28-221">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
