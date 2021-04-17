---
description: Abre um link simbólico existente.
ms.assetid: 37684707-4f65-4904-8bfc-d0679ebbd924
title: Função NtOpenSymbolicLinkObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenSymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3cd5091fe19631079ff3c51d9d6ba7777970a854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811246"
---
# <a name="ntopensymboliclinkobject-function"></a><span data-ttu-id="0bd53-103">Função NtOpenSymbolicLinkObject</span><span class="sxs-lookup"><span data-stu-id="0bd53-103">NtOpenSymbolicLinkObject function</span></span>

<span data-ttu-id="0bd53-104">\[Essa função pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="0bd53-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="0bd53-105">Abre um link simbólico existente.</span><span class="sxs-lookup"><span data-stu-id="0bd53-105">Opens an existing symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bd53-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bd53-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtOpenSymbolicLinkObject(
  _Out_ PHANDLE            LinkHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="0bd53-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bd53-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bd53-108">*LinkHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0bd53-108">*LinkHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd53-109">Um identificador para o objeto de link simbólico aberto recentemente.</span><span class="sxs-lookup"><span data-stu-id="0bd53-109">A handle to the newly opened symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="0bd53-110">*DesiredAccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bd53-110">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd53-111">Uma [**\_ máscara de acesso**](../secauthz/access-mask.md) que especifica o acesso solicitado ao objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="0bd53-111">An [**ACCESS\_MASK**](../secauthz/access-mask.md) that specifies the requested access to the directory object.</span></span> <span data-ttu-id="0bd53-112">É comum usar a leitura genérica para \_ que o identificador possa ser passado para a função [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) .</span><span class="sxs-lookup"><span data-stu-id="0bd53-112">It is typical to use GENERIC\_READ so the handle can be passed to the [**NtQueryDirectoryObject**](ntquerydirectoryobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0bd53-113">*Objetoattributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0bd53-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bd53-114">Os atributos para o objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="0bd53-114">The attributes for the directory object.</span></span> <span data-ttu-id="0bd53-115">Para inicializar a estrutura de **\_ atributos de objeto** , use a macro **InitializeObjectAttributes** .</span><span class="sxs-lookup"><span data-stu-id="0bd53-115">To initialize the **OBJECT\_ATTRIBUTES** structure, use the **InitializeObjectAttributes** macro.</span></span> <span data-ttu-id="0bd53-116">Se o chamador não estiver em execução em um contexto de thread do sistema, ele deverá especificar o sinalizador **obj \_ kernel \_ Handle** ao inicializar a estrutura.</span><span class="sxs-lookup"><span data-stu-id="0bd53-116">If the caller is not running in a system thread context, it must specify the **OBJ\_KERNEL\_HANDLE** flag when initializing the structure.</span></span> <span data-ttu-id="0bd53-117">Para obter mais informações, consulte a documentação para esses itens na documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="0bd53-117">For more information, see the documentation for these items in the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bd53-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0bd53-118">Return value</span></span>

<span data-ttu-id="0bd53-119">A função retorna o **status \_ êxito** ou um status de erro.</span><span class="sxs-lookup"><span data-stu-id="0bd53-119">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bd53-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bd53-120">Remarks</span></span>

<span data-ttu-id="0bd53-121">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0bd53-121">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bd53-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0bd53-122">Requirements</span></span>



| <span data-ttu-id="0bd53-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bd53-123">Requirement</span></span> | <span data-ttu-id="0bd53-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0bd53-124">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd53-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0bd53-125">DLL</span></span><br/> | <dl> <span data-ttu-id="0bd53-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bd53-126"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bd53-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0bd53-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bd53-128">**NtQueryDirectoryObject**</span><span class="sxs-lookup"><span data-stu-id="0bd53-128">**NtQueryDirectoryObject**</span></span>](ntquerydirectoryobject.md)
</dt> </dl>

 

 
