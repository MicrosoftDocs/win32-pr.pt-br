---
description: Não há suporte para a função RKeyOpenKeyService.
ms.assetid: 3af18cf7-bc98-4ebc-a62c-7234e9fbddaa
title: Função RKeyOpenKeyService (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyOpenKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: ce905594d1ed088eb72dc59a1fa6beec576384ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810508"
---
# <a name="rkeyopenkeyservice-function"></a><span data-ttu-id="be873-103">Função RKeyOpenKeyService</span><span class="sxs-lookup"><span data-stu-id="be873-103">RKeyOpenKeyService function</span></span>

<span data-ttu-id="be873-104">Não há suporte para a função **RKeyOpenKeyService** .</span><span class="sxs-lookup"><span data-stu-id="be873-104">The **RKeyOpenKeyService** function is not supported.</span></span>

<span data-ttu-id="be873-105">**Windows Server 2003:** A função **RKeyOpenKeyService** estabelece uma conexão com um computador remoto e abre um identificador de serviço de chave.</span><span class="sxs-lookup"><span data-stu-id="be873-105">**Windows Server 2003:** The **RKeyOpenKeyService** function establishes a connection to a remote computer and opens a key service handle.</span></span> <span data-ttu-id="be873-106">O identificador de serviço de chave pode ser usado subsequentemente pela função [**RKeyPFXInstall**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="be873-106">The key service handle can subsequently be used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span> <span data-ttu-id="be873-107">Observe que esse comportamento foi alterado com o Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="be873-107">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="be873-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be873-108">Syntax</span></span>


```C++
ULONG RKeyOpenKeyService(
  _In_    LPSTR          pszMachineName,
  _In_    KEYSVC_TYPE    OwnerType,
  _In_    LPWSTR         pwszOwnerName,
  _In_    void           *pAuthentication,
  _Inout_ void           *pReserved,
  _Out_   KEYSVCC_HANDLE *phKeySvcCli
);
```



## <a name="parameters"></a><span data-ttu-id="be873-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be873-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be873-110">*pszMachineName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be873-110">*pszMachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-111">Ponteiro longo para uma cadeia de caracteres terminada em nulo que representa o computador em que o identificador de serviço de chave será aberto.</span><span class="sxs-lookup"><span data-stu-id="be873-111">Long pointer to a null-terminated string that represents the computer where the key service handle will be opened.</span></span>

</dd> <dt>

<span data-ttu-id="be873-112">*OwnerType* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be873-112">*OwnerType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-113">[**KEYSVC \_ Digite**](keysvc-type.md) o valor que representa o tipo de chave.</span><span class="sxs-lookup"><span data-stu-id="be873-113">[**KEYSVC\_TYPE**](keysvc-type.md) value that represents the key type.</span></span> <span data-ttu-id="be873-114">O único valor com suporte é **KeySvcMachine**.</span><span class="sxs-lookup"><span data-stu-id="be873-114">The only supported value is **KeySvcMachine**.</span></span>

</dd> <dt>

<span data-ttu-id="be873-115">*pwszOwnerName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be873-115">*pwszOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="be873-116">Reserved.</span></span> <span data-ttu-id="be873-117">Defina esse valor como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="be873-117">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="be873-118">*pAuthentication* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be873-118">*pAuthentication* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-119">Um ponteiro para um **void** que representa as configurações de autenticação.</span><span class="sxs-lookup"><span data-stu-id="be873-119">A pointer to a **void** that represents the authentication settings.</span></span> <span data-ttu-id="be873-120">Esse ponteiro pode apontar para um valor de zero ou o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="be873-120">This pointer can point to a value of zero or the following value.</span></span>



| <span data-ttu-id="be873-121">Valor</span><span class="sxs-lookup"><span data-stu-id="be873-121">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="be873-122">Significado</span><span class="sxs-lookup"><span data-stu-id="be873-122">Meaning</span></span>                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="RKEYSVC_CONNECT_SECURE_ONLY"></span><span id="rkeysvc_connect_secure_only"></span><dl> <span data-ttu-id="be873-123"><dt>**RKEYSVC \_ CONECTAR \_ \_ somente segurança**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="be873-123"><dt>**RKEYSVC\_CONNECT\_SECURE\_ONLY**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="be873-124">O cliente requer autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="be873-124">The client requires mutual authentication.</span></span> <span data-ttu-id="be873-125">Se esse valor for especificado, haverá falha no fallback para NTLM.</span><span class="sxs-lookup"><span data-stu-id="be873-125">If this value is specified, fallback to NTLM will fail.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="be873-126">*preservado* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="be873-126">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="be873-127">Reserved.</span></span> <span data-ttu-id="be873-128">Defina esse valor como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="be873-128">Set this value to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="be873-129">*phKeySvcCli* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="be873-129">*phKeySvcCli* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be873-130">Um ponteiro para um [**\_ identificador de KEYSVCC**](keysvcc-handle.md) que recebe o identificador de serviço de chave aberto.</span><span class="sxs-lookup"><span data-stu-id="be873-130">A pointer to a [**KEYSVCC\_HANDLE**](keysvcc-handle.md) that receives the opened key service handle.</span></span> <span data-ttu-id="be873-131">Quando você terminar de usar o identificador, libere o recurso chamando a função [**RKeyCloseKeyService**](rkeyclosekeyservice.md) .</span><span class="sxs-lookup"><span data-stu-id="be873-131">When you have finished using the handle, free the resource by calling the [**RKeyCloseKeyService**](rkeyclosekeyservice.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be873-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be873-132">Return value</span></span>

<span data-ttu-id="be873-133">Se a função for bem-sucedida, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="be873-133">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="be873-134">Se a função falhar, o valor de retorno será um **ULONG** que indica o erro.</span><span class="sxs-lookup"><span data-stu-id="be873-134">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="be873-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be873-135">Requirements</span></span>



| <span data-ttu-id="be873-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="be873-136">Requirement</span></span> | <span data-ttu-id="be873-137">Valor</span><span class="sxs-lookup"><span data-stu-id="be873-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be873-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be873-138">Minimum supported client</span></span><br/> | <span data-ttu-id="be873-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="be873-139">None supported</span></span><br/>                                                             |
| <span data-ttu-id="be873-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be873-140">Minimum supported server</span></span><br/> | <span data-ttu-id="be873-141">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be873-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be873-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be873-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="be873-143"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="be873-143"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be873-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="be873-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be873-145">**RKeyCloseKeyService**</span><span class="sxs-lookup"><span data-stu-id="be873-145">**RKeyCloseKeyService**</span></span>](rkeyclosekeyservice.md)
</dt> <dt>

[<span data-ttu-id="be873-146">**RKeyPFXInstall**</span><span class="sxs-lookup"><span data-stu-id="be873-146">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




