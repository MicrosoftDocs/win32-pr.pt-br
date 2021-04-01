---
description: Representa o cabeçalho de multisetor.
ms.assetid: 0fad0e93-b940-4b52-be16-c5f177884dfb
title: Estrutura de MULTI_SECTOR_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MULTI_SECTOR_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: ab21e17b83ae25286d2775d9dbd97dfd4cf493bc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646245"
---
# <a name="multi_sector_header-structure"></a><span data-ttu-id="2550d-103">Estrutura de cabeçalho de vários \_ setores \_</span><span class="sxs-lookup"><span data-stu-id="2550d-103">MULTI\_SECTOR\_HEADER structure</span></span>

<span data-ttu-id="2550d-104">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="2550d-104">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="2550d-105">Representa o cabeçalho de multisetor.</span><span class="sxs-lookup"><span data-stu-id="2550d-105">Represents the multisector header.</span></span>

## <a name="syntax"></a><span data-ttu-id="2550d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2550d-106">Syntax</span></span>


```C++
typedef struct _MULTI_SECTOR_HEADER {
  UCHAR  Signature[4];
  USHORT UpdateSequenceArrayOffset;
  USHORT UpdateSequenceArraySize;
} MULTI_SECTOR_HEADER, *PMULTI_SECTOR_HEADER;
```



## <a name="members"></a><span data-ttu-id="2550d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2550d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="2550d-108">**Signature**</span><span class="sxs-lookup"><span data-stu-id="2550d-108">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="2550d-109">A assinatura.</span><span class="sxs-lookup"><span data-stu-id="2550d-109">The signature.</span></span> <span data-ttu-id="2550d-110">Esse valor é uma conveniência para o usuário.</span><span class="sxs-lookup"><span data-stu-id="2550d-110">This value is a convenience to the user.</span></span>

</dd> <dt>

<span data-ttu-id="2550d-111">**UpdateSequenceArrayOffset**</span><span class="sxs-lookup"><span data-stu-id="2550d-111">**UpdateSequenceArrayOffset**</span></span>
</dt> <dd>

<span data-ttu-id="2550d-112">O deslocamento para a matriz de sequência de atualização, desde o início desta estrutura.</span><span class="sxs-lookup"><span data-stu-id="2550d-112">The offset to the update sequence array, from the start of this structure.</span></span> <span data-ttu-id="2550d-113">A matriz de sequência de atualização deve terminar antes do último valor USHORT no primeiro setor.</span><span class="sxs-lookup"><span data-stu-id="2550d-113">The update sequence array must end before the last USHORT value in the first sector.</span></span>

</dd> <dt>

<span data-ttu-id="2550d-114">**UpdateSequenceArraySize**</span><span class="sxs-lookup"><span data-stu-id="2550d-114">**UpdateSequenceArraySize**</span></span>
</dt> <dd>

<span data-ttu-id="2550d-115">O tamanho da matriz de sequência de atualização, em bytes.</span><span class="sxs-lookup"><span data-stu-id="2550d-115">The size of the update sequence array, in bytes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2550d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2550d-116">Remarks</span></span>

<span data-ttu-id="2550d-117">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="2550d-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="2550d-118">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="2550d-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

<span data-ttu-id="2550d-119">O cabeçalho multisetor e a matriz de sequência de atualização fornecem detecção de transferências de vários setores incompletas para dispositivos que têm um tamanho de setor físico maior ou igual ao número de sequência Stride (512) ou que não transferem os setores fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="2550d-119">The multisector header and update sequence array provide detection of incomplete multisector transfers for devices that either have a physical sector size greater than or equal to the sequence number stride (512) or that do not transfer sectors out of order.</span></span> <span data-ttu-id="2550d-120">Se existir um dispositivo que tenha um tamanho de setor menor do que o stride do número de sequência e, às vezes, transferir os setores fora de ordem, a matriz de sequência de atualização não fornecerá a detecção absoluta de transferências incompletas.</span><span class="sxs-lookup"><span data-stu-id="2550d-120">If a device exists that has a sector size smaller than the sequence number stride and it sometimes transfers sectors out of order, then the update sequence array will not provide absolute detection of incomplete transfers.</span></span> <span data-ttu-id="2550d-121">O stride do número de sequência é definido como um número pequeno o suficiente para fornecer proteção absoluta para todos os discos rígidos conhecidos.</span><span class="sxs-lookup"><span data-stu-id="2550d-121">The sequence number stride is set to a small enough number to provide absolute protection for all known hard disks.</span></span> <span data-ttu-id="2550d-122">Ele não está definido como menor ou pode haver excesso de tempo de execução ou sobrecarga de espaço.</span><span class="sxs-lookup"><span data-stu-id="2550d-122">It is not set any smaller or there might be excessive run time or space overhead.</span></span>

<span data-ttu-id="2550d-123">A matriz de sequência de atualização consiste em uma matriz de *n* valores **UShort** , em que *n* é o tamanho da estrutura que está sendo protegida dividida pelo Stride do número de sequência.</span><span class="sxs-lookup"><span data-stu-id="2550d-123">The update sequence array consists of an array of *n* **USHORT** values, where *n* is the size of the structure being protected divided by the sequence number stride.</span></span> <span data-ttu-id="2550d-124">A primeira palavra contém o número de sequência de atualização, que é um contador cíclico do número de vezes que a estrutura que contém foi gravada no disco.</span><span class="sxs-lookup"><span data-stu-id="2550d-124">The first word contains the update sequence number, which is a cyclical counter of the number of times the containing structure has been written to disk.</span></span> <span data-ttu-id="2550d-125">Em seguida, estão os *n* valores **UShort** salvos que foram substituídos pelo número de sequência de atualização na última vez em que a estrutura que a contém foi gravada no disco.</span><span class="sxs-lookup"><span data-stu-id="2550d-125">Next are the *n* saved **USHORT** values that were overwritten by the update sequence number the last time the containing structure was written to disk.</span></span>

<span data-ttu-id="2550d-126">Cada vez que a estrutura protegida está prestes a ser gravada no disco, a última palavra em cada Stride de número de sequência é salva em sua respectiva posição na matriz de números de sequência e, em seguida, é substituída pelo próximo número de sequência de atualização.</span><span class="sxs-lookup"><span data-stu-id="2550d-126">Each time the protected structure is about to be written to disk, the last word in each sequence number stride is saved to its respective position in the sequence number array, then it is overwritten with the next update sequence number.</span></span> <span data-ttu-id="2550d-127">Após a gravação, ou sempre que a estrutura for lida, a palavra salva da matriz de números de sequência será restaurada para sua posição real na estrutura.</span><span class="sxs-lookup"><span data-stu-id="2550d-127">After the write, or whenever the structure is read, the saved word from the sequence number array is restored to its actual position in the structure.</span></span> <span data-ttu-id="2550d-128">Antes de restaurar as palavras salvas em leituras, todos os números de sequência no final de cada Stride são comparados com o número de sequência real no início da matriz.</span><span class="sxs-lookup"><span data-stu-id="2550d-128">Before restoring the saved words on reads, all the sequence numbers at the end of each stride are compared with the actual sequence number at the start of the array.</span></span> <span data-ttu-id="2550d-129">Se qualquer uma dessas comparações não for igual, uma transferência de multisetor com falha será detectada.</span><span class="sxs-lookup"><span data-stu-id="2550d-129">If any of these comparisons are not equal, then a failed multisector transfer has been detected.</span></span>

<span data-ttu-id="2550d-130">O tamanho da matriz é determinado pelo tamanho da estrutura que a contém.</span><span class="sxs-lookup"><span data-stu-id="2550d-130">The size of the array is determined by the size of the containing structure.</span></span> <span data-ttu-id="2550d-131">A matriz de sequência de atualização deve ser incluída no final do cabeçalho da estrutura que está sendo protegida devido a seu tamanho variável.</span><span class="sxs-lookup"><span data-stu-id="2550d-131">The update sequence array should be included at the end of the header of the structure it is protecting because of its variable size.</span></span> <span data-ttu-id="2550d-132">O usuário deve garantir que o espaço correto seja reservado para a estrutura recipiente: (tamanho da estrutura/512 + 1) \* sizeof (UShort).</span><span class="sxs-lookup"><span data-stu-id="2550d-132">The user must ensure that the correct space is reserved for the containing structure: (size of structure / 512 + 1) \* sizeof(USHORT).</span></span>

## <a name="see-also"></a><span data-ttu-id="2550d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2550d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2550d-134">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="2550d-134">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
