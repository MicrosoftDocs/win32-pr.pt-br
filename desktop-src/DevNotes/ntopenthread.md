---
description: Abre um identificador para um objeto de thread com o acesso especificado.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Função NtOpenThread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751752"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="1f0e0-103">Função NtOpenThread</span><span class="sxs-lookup"><span data-stu-id="1f0e0-103">NtOpenThread function</span></span>

<span data-ttu-id="1f0e0-104">\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="1f0e0-105">Em vez disso, use a função [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]</span><span class="sxs-lookup"><span data-stu-id="1f0e0-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="1f0e0-106">Abre um identificador para um objeto de thread com o acesso especificado.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f0e0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f0e0-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="1f0e0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f0e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f0e0-109">*ThreadHandle* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1f0e0-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0e0-110">Um ponteiro para uma variável que recebe o identificador de objeto de thread.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="1f0e0-111">*DesiredAccess* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f0e0-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0e0-112">Um tipo de dados de [**\_ máscara de acesso**](../secauthz/access-mask-format.md) que fornece os tipos de acesso desejados para o objeto de thread.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="1f0e0-113">*Objetoattributes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f0e0-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0e0-114">Um ponteiro para uma estrutura de [ \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) .</span><span class="sxs-lookup"><span data-stu-id="1f0e0-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="1f0e0-115">O membro **objectname** desta estrutura deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="1f0e0-116">**Windows Server 2003 e Windows XP:** O membro **objectname** desta estrutura pode apontar para um nome de objeto.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="1f0e0-117">Se **objectname** não for NULL, o parâmetro *CLIENTID* deverá ser nulo.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="1f0e0-118">*ClientID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f0e0-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f0e0-119">Um ponteiro para uma estrutura de **\_ ID do cliente** que identifica o thread cujo thread deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="1f0e0-120">**Windows Server 2003 e Windows XP:** Um ponteiro para uma estrutura de **\_ ID do cliente** que identifica o thread cujo thread deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="1f0e0-121">Este parâmetro pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-121">This parameter can be NULL.</span></span> <span data-ttu-id="1f0e0-122">Se esse parâmetro não for nulo, o membro **objectname** da estrutura apontada pelo parâmetro *objectAttributes* deverá ser nulo.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f0e0-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f0e0-123">Return value</span></span>

<span data-ttu-id="1f0e0-124">Retorna um **NTSTATUS** ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="1f0e0-125">Os formulários e o significado dos códigos de erro **NTSTATUS** são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0e0-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f0e0-126">Remarks</span></span>

<span data-ttu-id="1f0e0-127">Esta função não tem nenhum arquivo de cabeçalho associado.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-127">This function has no associated header file.</span></span> <span data-ttu-id="1f0e0-128">A biblioteca de importação associada, ntdll. lib, está disponível no WDK.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="1f0e0-129">Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="1f0e0-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f0e0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f0e0-130">Requirements</span></span>



| <span data-ttu-id="1f0e0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f0e0-131">Requirement</span></span> | <span data-ttu-id="1f0e0-132">Valor</span><span class="sxs-lookup"><span data-stu-id="1f0e0-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f0e0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1f0e0-133">DLL</span></span><br/> | <dl> <span data-ttu-id="1f0e0-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f0e0-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
