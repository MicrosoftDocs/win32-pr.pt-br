---
description: Estrutura usada pela função SfcGetFiles.
ms.assetid: 958167e3-3eb3-406a-85bf-ffe2851a95a1
title: Estrutura de PPROTECT_FILE_ENTRY (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PPROTECT_FILE_ENTRY
api_type:
- HeaderDef
api_location:
- Sfcfiles.h
ms.openlocfilehash: 98cda570a3677560d51800d58822d93a942847c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771553"
---
# <a name="pprotect_file_entry-structure"></a><span data-ttu-id="dd11f-103">Estrutura de entrada de \_ arquivo PPROTECT \_</span><span class="sxs-lookup"><span data-stu-id="dd11f-103">PPROTECT\_FILE\_ENTRY structure</span></span>

<span data-ttu-id="dd11f-104">\[Essa estrutura está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="dd11f-104">\[This structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dd11f-105">O suporte para essa estrutura foi removido no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="dd11f-105">Support for this structure was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="dd11f-106">Use as funções com suporte listadas em [funções WRP](wfp-functions.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="dd11f-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="dd11f-107">Estrutura usada pela função [**SfcGetFiles**](sfcgetfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="dd11f-107">Structure used by the [**SfcGetFiles**](sfcgetfiles.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd11f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd11f-108">Syntax</span></span>


```C++
typedef struct _PPROTECT_FILE_ENTRY {
  PWSTR SourceFileName;
  PWSTR FileName;
  PWSTR InfName;
} PPROTECT_FILE_ENTRY, *PPPROTECT_FILE_ENTRY;
```



## <a name="members"></a><span data-ttu-id="dd11f-109">Membros</span><span class="sxs-lookup"><span data-stu-id="dd11f-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="dd11f-110">**SourceFileName**</span><span class="sxs-lookup"><span data-stu-id="dd11f-110">**SourceFileName**</span></span>
</dt> <dd>

<span data-ttu-id="dd11f-111">Ponteiro para um valor de cadeia de caracteres que contém o nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="dd11f-111">Pointer to a string value containing the filename of the source file.</span></span> <span data-ttu-id="dd11f-112">Isso será **nulo** se o arquivo não for renomeado na instalação.</span><span class="sxs-lookup"><span data-stu-id="dd11f-112">This will be **NULL** if the file is not renamed on installation.</span></span>

</dd> <dt>

<span data-ttu-id="dd11f-113">**FileName**</span><span class="sxs-lookup"><span data-stu-id="dd11f-113">**FileName**</span></span>
</dt> <dd>

<span data-ttu-id="dd11f-114">Ponteiro para o valor de cadeia de caracteres que contém o nome de arquivo de destino mais o caminho completo para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="dd11f-114">Pointer to string value containing the destination filename plus the full path to the file.</span></span>

</dd> <dt>

<span data-ttu-id="dd11f-115">**InfName**</span><span class="sxs-lookup"><span data-stu-id="dd11f-115">**InfName**</span></span>
</dt> <dd>

<span data-ttu-id="dd11f-116">Ponteiro para o valor da cadeia de caracteres que contém o nome do arquivo INF que fornece informações de layout.</span><span class="sxs-lookup"><span data-stu-id="dd11f-116">Pointer to string value containing the filename of the INF file which provides layout information.</span></span> <span data-ttu-id="dd11f-117">Esse parâmetro pode ser **nulo** ao usar o layout padrão.</span><span class="sxs-lookup"><span data-stu-id="dd11f-117">This parameter may be **NULL** when using the default layout.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd11f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd11f-118">Requirements</span></span>



| <span data-ttu-id="dd11f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd11f-119">Requirement</span></span> | <span data-ttu-id="dd11f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="dd11f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd11f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd11f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dd11f-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dd11f-122">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dd11f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dd11f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dd11f-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dd11f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dd11f-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="dd11f-125">End of client support</span></span><br/>    | <span data-ttu-id="dd11f-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dd11f-126">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="dd11f-127">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="dd11f-127">End of server support</span></span><br/>    | <span data-ttu-id="dd11f-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dd11f-128">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="dd11f-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd11f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd11f-130"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd11f-130"><dt>Sfcfiles.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd11f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd11f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd11f-132">**SfcGetFiles**</span><span class="sxs-lookup"><span data-stu-id="dd11f-132">**SfcGetFiles**</span></span>](sfcgetfiles.md)
</dt> </dl>

 

 




