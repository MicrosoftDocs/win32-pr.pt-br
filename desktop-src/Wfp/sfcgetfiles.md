---
description: Lista arquivos protegidos.
ms.assetid: 46a1ff83-afed-4ce3-bb62-551446efdb78
title: Função SfcGetFiles (sfcfiles. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SfcGetFiles
api_type:
- DllExport
api_location:
- Sfcfiles.dll
ms.openlocfilehash: 6b38b761372db656308e778fd96ea48607cf1f21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828818"
---
# <a name="sfcgetfiles-function"></a><span data-ttu-id="af889-103">Função SfcGetFiles</span><span class="sxs-lookup"><span data-stu-id="af889-103">SfcGetFiles function</span></span>

<span data-ttu-id="af889-104">\[Essa função está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="af889-104">\[This function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="af889-105">O suporte para essa função foi removido no Windows Vista e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="af889-105">Support for this function was removed in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="af889-106">Use as funções com suporte listadas em [funções WRP](wfp-functions.md) em vez disso.\]</span><span class="sxs-lookup"><span data-stu-id="af889-106">Use the supported functions listed in [WRP Functions](wfp-functions.md) instead.\]</span></span>

<span data-ttu-id="af889-107">Lista arquivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="af889-107">Lists protected files.</span></span>

## <a name="syntax"></a><span data-ttu-id="af889-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af889-108">Syntax</span></span>


```C++
NTSTATUS WINAPI SfcGetFiles(
  _Out_ PPROTECT_FILE_ENTRY ProtFileData,
  _Out_ PULONG              FileCount
);
```



## <a name="parameters"></a><span data-ttu-id="af889-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af889-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af889-110">*ProtFileData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="af889-110">*ProtFileData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af889-111">Um ponteiro para uma estrutura de [**\_ \_ entrada de arquivo PPROTECT**](pprotect-file-entry.md) que contém a lista de arquivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="af889-111">A pointer to a [**PPROTECT\_FILE\_ENTRY**](pprotect-file-entry.md) structure that contains the protected files list.</span></span>

</dd> <dt>

<span data-ttu-id="af889-112">*Contagem de FileCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="af889-112">*FileCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af889-113">Um ponteiro para um local que contém um valor ULONG que é o número de arquivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="af889-113">A pointer to a location containing a ULONG value that is the number of protected files.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af889-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af889-114">Return value</span></span>

<span data-ttu-id="af889-115">Se a função for bem-sucedida, o valor de retorno será \_ êxito no status.</span><span class="sxs-lookup"><span data-stu-id="af889-115">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span> <span data-ttu-id="af889-116">Se a função falhar, ela retornará o código de erro NTSTATUS apropriado.</span><span class="sxs-lookup"><span data-stu-id="af889-116">If the function fails, it returns the appropriate NTSTATUS error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="af889-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af889-117">Requirements</span></span>



| <span data-ttu-id="af889-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="af889-118">Requirement</span></span> | <span data-ttu-id="af889-119">Valor</span><span class="sxs-lookup"><span data-stu-id="af889-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="af889-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af889-120">Minimum supported client</span></span><br/> | <span data-ttu-id="af889-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="af889-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="af889-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af889-122">Minimum supported server</span></span><br/> | <span data-ttu-id="af889-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af889-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="af889-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="af889-124">End of client support</span></span><br/>    | <span data-ttu-id="af889-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="af889-125">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="af889-126">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="af889-126">End of server support</span></span><br/>    | <span data-ttu-id="af889-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="af889-127">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="af889-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="af889-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="af889-129"><dt>Sfcfiles. h</dt></span><span class="sxs-lookup"><span data-stu-id="af889-129"><dt>Sfcfiles.h</dt></span></span> </dl>   |
| <span data-ttu-id="af889-130">DLL</span><span class="sxs-lookup"><span data-stu-id="af889-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af889-131"><dt>Sfcfiles.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af889-131"><dt>Sfcfiles.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af889-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="af889-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af889-133">**\_entrada de arquivo PPROTECT \_**</span><span class="sxs-lookup"><span data-stu-id="af889-133">**PPROTECT\_FILE\_ENTRY**</span></span>](pprotect-file-entry.md)
</dt> </dl>

 

 




