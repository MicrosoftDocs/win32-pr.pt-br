---
description: Recupera o destino de um link simbólico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: Função NtQuerySymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751952"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="7511b-103">Função NtQuerySymbolicLinkObject</span><span class="sxs-lookup"><span data-stu-id="7511b-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="7511b-104">\[Essa função pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="7511b-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="7511b-105">Recupera o destino de um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="7511b-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="7511b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7511b-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="7511b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7511b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7511b-108">*LinkHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7511b-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7511b-109">Um identificador para o objeto de vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="7511b-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="7511b-110">*LinkTarget* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="7511b-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7511b-111">Um ponteiro para uma cadeia de caracteres Unicode inicializada que recebe o destino do link simbólico.</span><span class="sxs-lookup"><span data-stu-id="7511b-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="7511b-112">O **MaximumLength** e os membros do **buffer** devem ser definidos se a chamada falhar.</span><span class="sxs-lookup"><span data-stu-id="7511b-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="7511b-113">*ReturnedLength* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="7511b-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7511b-114">Um ponteiro para uma variável que recebe o comprimento da cadeia de caracteres Unicode retornado no parâmetro *LinkTarget* .</span><span class="sxs-lookup"><span data-stu-id="7511b-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="7511b-115">Se a função retornar **o \_ buffer de status \_ muito \_ pequeno**, essa variável receberá o tamanho de buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="7511b-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7511b-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7511b-116">Return value</span></span>

<span data-ttu-id="7511b-117">A função retorna o **status \_ êxito** ou um status de erro.</span><span class="sxs-lookup"><span data-stu-id="7511b-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="7511b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7511b-118">Remarks</span></span>

<span data-ttu-id="7511b-119">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="7511b-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="7511b-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7511b-120">Requirements</span></span>



| <span data-ttu-id="7511b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7511b-121">Requirement</span></span> | <span data-ttu-id="7511b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7511b-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7511b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7511b-123">DLL</span></span><br/> | <dl> <span data-ttu-id="7511b-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7511b-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7511b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7511b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7511b-126">**NtOpenSymbolicLinkObject**</span><span class="sxs-lookup"><span data-stu-id="7511b-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
