---
description: Contém o atributo de informações padrão. Esse atributo está presente em cada registro de arquivo base e deve ser residente.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Estrutura de STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010081"
---
# <a name="standard_information-structure"></a><span data-ttu-id="b50e6-104">\_Estrutura de informações padrão</span><span class="sxs-lookup"><span data-stu-id="b50e6-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="b50e6-105">\[Essa estrutura é válida somente para a versão 3 de volumes NTFS; Ele pode ser alterado em versões futuras.\]</span><span class="sxs-lookup"><span data-stu-id="b50e6-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="b50e6-106">Contém o atributo de informações padrão.</span><span class="sxs-lookup"><span data-stu-id="b50e6-106">Contains the standard information attribute.</span></span> <span data-ttu-id="b50e6-107">Esse atributo está presente em cada registro de arquivo base e deve ser residente.</span><span class="sxs-lookup"><span data-stu-id="b50e6-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="b50e6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b50e6-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="b50e6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="b50e6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="b50e6-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="b50e6-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="b50e6-111">Reservado.</span><span class="sxs-lookup"><span data-stu-id="b50e6-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="b50e6-112">**OwnerId**</span><span class="sxs-lookup"><span data-stu-id="b50e6-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="b50e6-113">O identificador do proprietário do arquivo, do índice de segurança.</span><span class="sxs-lookup"><span data-stu-id="b50e6-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="b50e6-114">**Securityid**</span><span class="sxs-lookup"><span data-stu-id="b50e6-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="b50e6-115">O identificador de segurança do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b50e6-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b50e6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b50e6-116">Remarks</span></span>

<span data-ttu-id="b50e6-117">Observe que não há nenhum arquivo de cabeçalho associado para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="b50e6-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="b50e6-118">Essa definição de estrutura é válida somente para a versão principal 3 e secundária 0 ou 1, conforme relatado [**pelo \_ fsctl \_ obter \_ \_ dados de volume NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="b50e6-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="b50e6-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b50e6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b50e6-120">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="b50e6-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
