---
description: Gera um conjunto de chaves de sessão de protocolo de protocolo SSL (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Função SslGenerateSessionKeys (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cf8e20008d2a77cae3a47728f4e38fff8ae0b09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787466"
---
# <a name="sslgeneratesessionkeys-function"></a><span data-ttu-id="a53e5-103">Função SslGenerateSessionKeys</span><span class="sxs-lookup"><span data-stu-id="a53e5-103">SslGenerateSessionKeys function</span></span>

<span data-ttu-id="a53e5-104">A função **SslGenerateSessionKeys** gera um conjunto de chaves de sessão de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="a53e5-104">The **SslGenerateSessionKeys** function generates a set of [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) session keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="a53e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a53e5-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a53e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a53e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a53e5-107">*hSslProvider* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a53e5-108">O identificador para a instância do provedor de protocolo SSL.</span><span class="sxs-lookup"><span data-stu-id="a53e5-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="a53e5-109">*hMasterKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a53e5-110">O identificador para o objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="a53e5-110">The handle to the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="a53e5-111">*phReadKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-111">*phReadKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a53e5-112">Um ponteiro para o identificador de chave de leitura retornado.</span><span class="sxs-lookup"><span data-stu-id="a53e5-112">A pointer to the returned read key handle.</span></span>

</dd> <dt>

<span data-ttu-id="a53e5-113">*phWriteKey* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-113">*phWriteKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a53e5-114">Um ponteiro para o identificador de chave de gravação retornado.</span><span class="sxs-lookup"><span data-stu-id="a53e5-114">A pointer to the returned write key handle.</span></span>

</dd> <dt>

<span data-ttu-id="a53e5-115">*pParameterList* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-115">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a53e5-116">Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contém informações usadas como parte da operação de troca de chaves.</span><span class="sxs-lookup"><span data-stu-id="a53e5-116">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="a53e5-117">O conjunto preciso de buffers depende do protocolo e do pacote de codificação usado.</span><span class="sxs-lookup"><span data-stu-id="a53e5-117">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="a53e5-118">No mínimo, a lista conterá buffers que contêm os valores aleatórios de cliente e servidor fornecidos.</span><span class="sxs-lookup"><span data-stu-id="a53e5-118">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="a53e5-119">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a53e5-120">Esse parâmetro é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="a53e5-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a53e5-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a53e5-121">Return value</span></span>

<span data-ttu-id="a53e5-122">Se a função for realizada com sucesso, ela retornará zero.</span><span class="sxs-lookup"><span data-stu-id="a53e5-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a53e5-123">Se a função falhar, ela retornará um valor de erro diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="a53e5-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a53e5-124">Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a53e5-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a53e5-125">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a53e5-125">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="a53e5-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="a53e5-126">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a53e5-127"><dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória</span><span class="sxs-lookup"><span data-stu-id="a53e5-127"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="a53e5-128">Não há memória suficiente disponível para alocar os buffers necessários.</span><span class="sxs-lookup"><span data-stu-id="a53e5-128">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="a53e5-129"><dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="a53e5-129"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="a53e5-130">Um dos identificadores fornecidos não é válido.</span><span class="sxs-lookup"><span data-stu-id="a53e5-130">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="a53e5-131"><dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="a53e5-131"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="a53e5-132">O parâmetro *phReadKey* ou *phWriteKey* é nulo.</span><span class="sxs-lookup"><span data-stu-id="a53e5-132">The *phReadKey* or *phWriteKey* parameter is null.</span></span><br/>            |



 

## <a name="requirements"></a><span data-ttu-id="a53e5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a53e5-133">Requirements</span></span>



| <span data-ttu-id="a53e5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a53e5-134">Requirement</span></span> | <span data-ttu-id="a53e5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a53e5-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a53e5-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a53e5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a53e5-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a53e5-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a53e5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a53e5-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a53e5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a53e5-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a53e5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="a53e5-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="a53e5-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a53e5-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a53e5-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a53e5-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a53e5-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

