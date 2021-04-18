---
title: Função CBCreateClientInstance (Cbclient. h)
description: Cria uma instância do cliente RPC do Conexão de Área de Trabalho Remota Broker.
ms.assetid: 700E47BC-C547-44AB-8607-B9797D542AA7
ms.tgt_platform: multiple
keywords:
- Função CBCreateClientInstance Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CBCreateClientInstance
api_location:
- Cbclient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2b30f2d236bcc90dfa4977f54d56a5d1717d18a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764749"
---
# <a name="cbcreateclientinstance-function"></a><span data-ttu-id="43e16-104">Função CBCreateClientInstance</span><span class="sxs-lookup"><span data-stu-id="43e16-104">CBCreateClientInstance function</span></span>

<span data-ttu-id="43e16-105">Cria uma instância do cliente RPC do Conexão de Área de Trabalho Remota Broker.</span><span class="sxs-lookup"><span data-stu-id="43e16-105">Creates an instance of the Remote Desktop Connection Broker RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e16-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43e16-106">Syntax</span></span>


```C++
HRESULT CBCreateClientInstance(
  _In_  DWORD                   Version,
  _Out_ IConnectionBrokerClient **ppCbClient
);
```



## <a name="parameters"></a><span data-ttu-id="43e16-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43e16-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e16-108">*Versão* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="43e16-108">*Version* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e16-109">Especifica a versão da interface de cliente do agente de Conexão de Área de Trabalho Remota que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="43e16-109">Specifies the version of the Remote Desktop Connection Broker client interface being requested.</span></span> <span data-ttu-id="43e16-110">Este deve ser o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="43e16-110">This must be the following value.</span></span>

<dt>

<span data-ttu-id="43e16-111">1</span><span class="sxs-lookup"><span data-stu-id="43e16-111">1</span></span>
</dt> <dd>

<span data-ttu-id="43e16-112">Versão 1 do cliente do agente de Conexão de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="43e16-112">Version 1 of the Remote Desktop Connection Broker client.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="43e16-113">*ppCbClient* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="43e16-113">*ppCbClient* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43e16-114">O endereço de um ponteiro de interface [**IConnectionBrokerClient**](iconnectionbrokerclient.md) que recebe o objeto de cliente do conexão de área de trabalho remota Broker.</span><span class="sxs-lookup"><span data-stu-id="43e16-114">The address of an [**IConnectionBrokerClient**](iconnectionbrokerclient.md) interface pointer that receives the Remote Desktop Connection Broker client object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e16-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43e16-115">Return value</span></span>

<span data-ttu-id="43e16-116">Se essa função for bem sucedido, ela retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="43e16-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43e16-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43e16-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e16-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e16-118">Requirements</span></span>



| <span data-ttu-id="43e16-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e16-119">Requirement</span></span> | <span data-ttu-id="43e16-120">Valor</span><span class="sxs-lookup"><span data-stu-id="43e16-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43e16-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43e16-121">Header</span></span><br/>  | <dl> <span data-ttu-id="43e16-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="43e16-122"><dt>Cbclient.h</dt></span></span> </dl>   |
| <span data-ttu-id="43e16-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43e16-123">Library</span></span><br/> | <dl> <span data-ttu-id="43e16-124"><dt>Cbclient. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43e16-124"><dt>Cbclient.lib</dt></span></span> </dl> |
| <span data-ttu-id="43e16-125">DLL</span><span class="sxs-lookup"><span data-stu-id="43e16-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="43e16-126"><dt>Cbclient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43e16-126"><dt>Cbclient.dll</dt></span></span> </dl> |



 

 





