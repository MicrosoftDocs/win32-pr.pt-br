---
description: A função InetGetAutodial retorna as configurações de discagem automática do registro.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: Função InetGetAutodial
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756326"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="4489f-103">Função InetGetAutodial</span><span class="sxs-lookup"><span data-stu-id="4489f-103">InetGetAutodial function</span></span>

<span data-ttu-id="4489f-104">\[Essa função não tem suporte e pode ser alterada ou indisponível em versões futuras do Windows.</span><span class="sxs-lookup"><span data-stu-id="4489f-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="4489f-105">\]</span><span class="sxs-lookup"><span data-stu-id="4489f-105">\]</span></span>

<span data-ttu-id="4489f-106">A função **InetGetAutodial** retorna as configurações de discagem automática do registro.</span><span class="sxs-lookup"><span data-stu-id="4489f-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="4489f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4489f-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="4489f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4489f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4489f-109">*lpfEnable* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4489f-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4489f-110">Indica se a AutoDiscagem está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4489f-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="4489f-111">Um valor **true** no retorno indica que A discagem automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4489f-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="4489f-112">*lpszEntryName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="4489f-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4489f-113">No retorno, contém o nome da entrada do catálogo telefônico que está definida para a discagem automática.</span><span class="sxs-lookup"><span data-stu-id="4489f-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="4489f-114">*cbEntryNameSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4489f-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4489f-115">Tamanho do buffer alocado pelo chamador para o nome de entrada do catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="4489f-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4489f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4489f-116">Return value</span></span>

<span data-ttu-id="4489f-117">Essa função pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="4489f-117">This function can return one of these values.</span></span>



| <span data-ttu-id="4489f-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4489f-118">Return code</span></span>                                                                                                | <span data-ttu-id="4489f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="4489f-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4489f-120"><dt>**êxito do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4489f-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="4489f-121">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4489f-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="4489f-122"><dt>**ERROS de \_ argumentos inválidos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4489f-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="4489f-123">*lpfEnable* ou *lpszEntryName* contém um ponteiro **nulo** ou o valor de *cbEntryNameSize* é zero.</span><span class="sxs-lookup"><span data-stu-id="4489f-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="4489f-124"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4489f-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="4489f-125">Memória insuficiente para alocar buffers internos.</span><span class="sxs-lookup"><span data-stu-id="4489f-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="4489f-126"><dt>**ERRO \_ de \_ buffer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="4489f-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="4489f-127">*cbEntryNameSize* não indica que o buffer apontado por *lpszEntryName* é grande o suficiente para receber o nome da entrada do catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="4489f-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4489f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="4489f-128">Remarks</span></span>

<span data-ttu-id="4489f-129">Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4489f-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4489f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4489f-130">Requirements</span></span>



| <span data-ttu-id="4489f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4489f-131">Requirement</span></span> | <span data-ttu-id="4489f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="4489f-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4489f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4489f-133">DLL</span></span><br/> | <dl> <span data-ttu-id="4489f-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4489f-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
