---
description: Recupera informações sobre o objeto de diretório especificado.
ms.assetid: a2c67c4d-4753-4d47-a404-31d067a78bf4
title: Função NtQueryDirectoryObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 99567d4784b121631089e723e1bd736e60a9cf54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750132"
---
# <a name="ntquerydirectoryobject-function"></a><span data-ttu-id="1d803-103">Função NtQueryDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="1d803-103">NtQueryDirectoryObject function</span></span>

<span data-ttu-id="1d803-104">\[Essa função pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="1d803-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="1d803-105">Recupera informações sobre o objeto de diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="1d803-105">Retrieves information about the specified directory object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d803-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d803-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQueryDirectoryObject(
  _In_      HANDLE  DirectoryHandle,
  _Out_opt_ PVOID   Buffer,
  _In_      ULONG   Length,
  _In_      BOOLEAN ReturnSingleEntry,
  _In_      BOOLEAN RestartScan,
  _Inout_   PULONG  Context,
  _Out_opt_ PULONG  ReturnLength
);
```



## <a name="parameters"></a><span data-ttu-id="1d803-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d803-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d803-108">*DirectoryHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d803-108">*DirectoryHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-109">Um identificador para o objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="1d803-109">A handle to the directory object.</span></span>

</dd> <dt>

<span data-ttu-id="1d803-110">*Buffer* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1d803-110">*Buffer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-111">Um ponteiro para um buffer que recebe as informações do diretório.</span><span class="sxs-lookup"><span data-stu-id="1d803-111">A pointer to a buffer that receives the directory information.</span></span> <span data-ttu-id="1d803-112">Esse buffer recebe uma ou mais estruturas de **\_ \_ informações de diretório de objeto** , a última sendo **NULL**, seguida por cadeias de caracteres que contêm os nomes das entradas de diretório.</span><span class="sxs-lookup"><span data-stu-id="1d803-112">This buffer receives one or more **OBJECT\_DIRECTORY\_INFORMATION** structures, the last one being **NULL**, followed by strings that contain the names of the directory entries.</span></span> <span data-ttu-id="1d803-113">Para obter mais informações, consulte Comentários.</span><span class="sxs-lookup"><span data-stu-id="1d803-113">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1d803-114">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d803-114">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-115">O tamanho do buffer de saída fornecido pelo usuário, em bytes.</span><span class="sxs-lookup"><span data-stu-id="1d803-115">The size of the user-supplied output buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1d803-116">*ReturnSingleEntry* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d803-116">*ReturnSingleEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-117">Indica se a função deve retornar apenas uma única entrada.</span><span class="sxs-lookup"><span data-stu-id="1d803-117">Indicates whether the function should return only a single entry.</span></span>

</dd> <dt>

<span data-ttu-id="1d803-118">*RestartScan* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1d803-118">*RestartScan* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-119">Indica se é para reiniciar a verificação ou continuar a enumeração usando as informações passadas no parâmetro de *contexto* .</span><span class="sxs-lookup"><span data-stu-id="1d803-119">Indicates whether to restart the scan or continue the enumeration using the information passed in the *Context* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="1d803-120">*Contexto* \[ do entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1d803-120">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-121">O contexto de enumeração.</span><span class="sxs-lookup"><span data-stu-id="1d803-121">The enumeration context.</span></span>

</dd> <dt>

<span data-ttu-id="1d803-122">*ReturnLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1d803-122">*ReturnLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1d803-123">Um ponteiro para uma variável que recebe o comprimento das informações de diretório retornadas no buffer de saída, em bytes.</span><span class="sxs-lookup"><span data-stu-id="1d803-123">A pointer to a variable that receives the length of the directory information returned in the output buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d803-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d803-124">Return value</span></span>

<span data-ttu-id="1d803-125">A função retorna o **status \_ êxito** ou um status de erro.</span><span class="sxs-lookup"><span data-stu-id="1d803-125">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d803-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d803-126">Remarks</span></span>

<span data-ttu-id="1d803-127">A seguir está a definição da estrutura **de \_ \_ informações do diretório de objeto** .</span><span class="sxs-lookup"><span data-stu-id="1d803-127">The following is the definition of the **OBJECT\_DIRECTORY\_INFORMATION** structure.</span></span>

``` syntax
typedef struct _OBJECT_DIRECTORY_INFORMATION {
    UNICODE_STRING Name;
    UNICODE_STRING TypeName;
} OBJECT_DIRECTORY_INFORMATION, *POBJECT_DIRECTORY_INFORMATION;
```

<span data-ttu-id="1d803-128">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1d803-128">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d803-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d803-129">Requirements</span></span>



| <span data-ttu-id="1d803-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d803-130">Requirement</span></span> | <span data-ttu-id="1d803-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1d803-131">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1d803-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1d803-132">DLL</span></span><br/> | <dl> <span data-ttu-id="1d803-133"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d803-133"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d803-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d803-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d803-135">**NtOpenDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="1d803-135">**NtOpenDirectoryObject**</span></span>](ntopendirectoryobject.md)
</dt> </dl>

 

 
