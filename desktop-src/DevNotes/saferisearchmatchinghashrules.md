---
description: Obtém o nível de uma regra de identificação de hash que corresponde ao hash especificado.
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: Função SaferiSearchMatchingHashRules
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457106"
---
# <a name="saferisearchmatchinghashrules-function"></a><span data-ttu-id="2237a-103">Função SaferiSearchMatchingHashRules</span><span class="sxs-lookup"><span data-stu-id="2237a-103">SaferiSearchMatchingHashRules function</span></span>

<span data-ttu-id="2237a-104">Obtém o nível de uma regra de identificação de hash que corresponde ao hash especificado.</span><span class="sxs-lookup"><span data-stu-id="2237a-104">Gets the level of a hash identification rule that matches the specified hash.</span></span>

<span data-ttu-id="2237a-105">Esta função não tem biblioteca de importação associada e não está declarada em um cabeçalho público.</span><span class="sxs-lookup"><span data-stu-id="2237a-105">This function has no associated import library and is not declared in a public header.</span></span> <span data-ttu-id="2237a-106">Você deve definir um ponteiro de função com a assinatura dessa função, e deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Advapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="2237a-106">You must define a function pointer with the signature of this function, and you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Advapi32.dll.</span></span>

<span data-ttu-id="2237a-107">É recomendável usar a função [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) para avaliar as diretivas de restrição de software.</span><span class="sxs-lookup"><span data-stu-id="2237a-107">We recommend using the [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) function to evaluate software restriction policies.</span></span>

## <a name="syntax"></a><span data-ttu-id="2237a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2237a-108">Syntax</span></span>


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a><span data-ttu-id="2237a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2237a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2237a-110">*HashAlgorithm* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2237a-110">*HashAlgorithm* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2237a-111">O identificador do algoritmo usado para criar o hash.</span><span class="sxs-lookup"><span data-stu-id="2237a-111">The identifier of the algorithm used to create the hash.</span></span>

</dd> <dt>

<span data-ttu-id="2237a-112">*pHashBytes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2237a-112">*pHashBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2237a-113">Um ponteiro para uma matriz de bytes que contém o hash.</span><span class="sxs-lookup"><span data-stu-id="2237a-113">A pointer to an array of bytes that contains the hash.</span></span>

</dd> <dt>

<span data-ttu-id="2237a-114">*dwHashSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2237a-114">*dwHashSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2237a-115">O tamanho, em bytes, da matriz *pHashBytes* .</span><span class="sxs-lookup"><span data-stu-id="2237a-115">The size, in bytes, of the *pHashBytes* array.</span></span>

</dd> <dt>

<span data-ttu-id="2237a-116">*dwOriginalImageSize* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2237a-116">*dwOriginalImageSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2237a-117">O tamanho, em bytes, da imagem original da qual o hash foi computado.</span><span class="sxs-lookup"><span data-stu-id="2237a-117">The size, in bytes, of the original image from which the hash was computed.</span></span>

</dd> <dt>

<span data-ttu-id="2237a-118">*pdwFoundLevel* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2237a-118">*pdwFoundLevel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2237a-119">Um ponteiro para o identificador de nível para a regra de identificação de hash correspondente.</span><span class="sxs-lookup"><span data-stu-id="2237a-119">A pointer to the level identifier for the matching hash identification rule.</span></span>

</dd> <dt>

<span data-ttu-id="2237a-120">*pdwSaferFlags*</span><span class="sxs-lookup"><span data-stu-id="2237a-120">*pdwSaferFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="2237a-121">Reservado.</span><span class="sxs-lookup"><span data-stu-id="2237a-121">Reserved.</span></span> <span data-ttu-id="2237a-122">Defina esse valor como zero.</span><span class="sxs-lookup"><span data-stu-id="2237a-122">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2237a-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2237a-123">Return value</span></span>

<span data-ttu-id="2237a-124">**True** se a função for bem-sucedida; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="2237a-124">**TRUE** if the function is successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2237a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2237a-125">Requirements</span></span>



| <span data-ttu-id="2237a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2237a-126">Requirement</span></span> | <span data-ttu-id="2237a-127">Valor</span><span class="sxs-lookup"><span data-stu-id="2237a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2237a-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2237a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2237a-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2237a-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2237a-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2237a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2237a-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2237a-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2237a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2237a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2237a-133"><dt>Advapi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2237a-133"><dt>Advapi32.dll</dt></span></span> </dl> |



 

 
