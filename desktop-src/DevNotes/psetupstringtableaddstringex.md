---
description: Adiciona uma cadeia de caracteres e dados extras a uma tabela.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: função pSetupStringTableAddStringEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750396"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="ca9a2-103">função pSetupStringTableAddStringEx</span><span class="sxs-lookup"><span data-stu-id="ca9a2-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="ca9a2-104">\[Essa função não está disponível no Windows Vista ou no Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="ca9a2-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="ca9a2-105">Adiciona uma cadeia de caracteres e dados extras a uma tabela.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca9a2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca9a2-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="ca9a2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca9a2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca9a2-108">*STRINGTABLE* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca9a2-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9a2-109">Um ponteiro para a tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="ca9a2-110">*Cadeia de caracteres* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ca9a2-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9a2-111">Um ponteiro para a cadeia de caracteres a ser adicionada à tabela.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="ca9a2-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="ca9a2-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9a2-113">O valor desse parâmetro pode ser `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .</span><span class="sxs-lookup"><span data-stu-id="ca9a2-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="ca9a2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ca9a2-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="ca9a2-115">Significado</span><span class="sxs-lookup"><span data-stu-id="ca9a2-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="ca9a2-116"><dt>**STRTAB \_ 0x001 \_ diferencia maiúsculas de minúsculas**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ca9a2-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="ca9a2-117">A cadeia de caracteres diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="ca9a2-118"><dt>**STRTAB \_ NOVO \_ EXTRADATA**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="ca9a2-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="ca9a2-119">Há dados extras.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="ca9a2-120">*ExtraData* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ca9a2-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9a2-121">Um ponteiro opcional para um objeto de dados extra.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="ca9a2-122">*ExtraDataSize* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ca9a2-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ca9a2-123">O tamanho dos dados adicionais.</span><span class="sxs-lookup"><span data-stu-id="ca9a2-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca9a2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca9a2-124">Remarks</span></span>

<span data-ttu-id="ca9a2-125">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="ca9a2-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca9a2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca9a2-126">Requirements</span></span>



| <span data-ttu-id="ca9a2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca9a2-127">Requirement</span></span> | <span data-ttu-id="ca9a2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ca9a2-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca9a2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ca9a2-129">DLL</span></span><br/> | <dl> <span data-ttu-id="ca9a2-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca9a2-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
