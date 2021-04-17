---
description: Adiciona dados a um objeto hash especificado.
ms.assetid: 8E32BBC4-C2DD-4174-9FF1-9001E4A7D87B
title: Função A_SHAUpdate (SHA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- A_SHAUpdate
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a0f8ac49d8221538a168ade536e55766e209d3d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762026"
---
# <a name="a_shaupdate-function"></a><span data-ttu-id="deefb-103">Uma \_ função SHAUpdate</span><span class="sxs-lookup"><span data-stu-id="deefb-103">A\_SHAUpdate function</span></span>

<span data-ttu-id="deefb-104">Adiciona dados a um objeto hash especificado.</span><span class="sxs-lookup"><span data-stu-id="deefb-104">Adds data to a specified hash object.</span></span>

## <a name="syntax"></a><span data-ttu-id="deefb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="deefb-105">Syntax</span></span>


```C++
void RSA32API A_SHAUpdate(
  _Inout_ A_SHA_CTX     *Context,
  _Out_   UNSIGNED CHAR *Buffer,
          UNSIGNED INT  BufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="deefb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="deefb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="deefb-107">*Contexto* \[ do entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="deefb-107">*Context* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-108">O contexto do SHA.</span><span class="sxs-lookup"><span data-stu-id="deefb-108">The SHA context.</span></span>

</dd> <dt>

<span data-ttu-id="deefb-109">*Buffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="deefb-109">*Buffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="deefb-110">A tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="deefb-110">The hash table.</span></span>

</dd> <dt>

<span data-ttu-id="deefb-111">*BufferSize*</span><span class="sxs-lookup"><span data-stu-id="deefb-111">*BufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="deefb-112">O tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="deefb-112">The size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="deefb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="deefb-113">Return value</span></span>

<span data-ttu-id="deefb-114">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="deefb-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="deefb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="deefb-115">Remarks</span></span>

<span data-ttu-id="deefb-116">Essa função pode ser chamada várias vezes para computar o hash em fluxos de dados longos ou fluxos de dados descontínuos.</span><span class="sxs-lookup"><span data-stu-id="deefb-116">This function can be called multiple times to compute the hash on long data streams or discontinuous data streams.</span></span> <span data-ttu-id="deefb-117">A [**função \_ SHAFinal**](a-shafinal.md) deve ser chamada antes da recuperação do valor de hash.</span><span class="sxs-lookup"><span data-stu-id="deefb-117">The [**A\_SHAFinal**](a-shafinal.md) function must be called before retrieving the hash value.</span></span>

<span data-ttu-id="deefb-118">Essa função é muito semelhante a SHAUpdate, mas é chamada diretamente da biblioteca, em vez de ser roteada pela infraestrutura de criptografia.</span><span class="sxs-lookup"><span data-stu-id="deefb-118">This function is very similar to SHAUpdate, but is called directly from the library, rather than being routed through the cryptography infrastructure.</span></span> <span data-ttu-id="deefb-119">Para obter mais informações, consulte [provedores do Windows NTCryptographic](/previous-versions/tn-archive/cc723484(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="deefb-119">For more information, see [Windows NTCryptographic Providers](/previous-versions/tn-archive/cc723484(v=technet.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="deefb-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="deefb-120">Requirements</span></span>



| <span data-ttu-id="deefb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="deefb-121">Requirement</span></span> | <span data-ttu-id="deefb-122">Valor</span><span class="sxs-lookup"><span data-stu-id="deefb-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="deefb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="deefb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="deefb-124"><dt>Sha. h</dt></span><span class="sxs-lookup"><span data-stu-id="deefb-124"><dt>Sha.h</dt></span></span> </dl>     |
| <span data-ttu-id="deefb-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="deefb-125">Library</span></span><br/> | <dl> <span data-ttu-id="deefb-126"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deefb-126"><dt>Ntdll.dll</dt></span></span> </dl> |
| <span data-ttu-id="deefb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="deefb-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="deefb-128"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="deefb-128"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
