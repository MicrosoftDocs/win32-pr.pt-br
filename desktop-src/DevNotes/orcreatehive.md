---
description: Cria um hive de registro offline que contém uma única chave de raiz vazia.
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: Função ORCreateHive (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752169"
---
# <a name="orcreatehive-function"></a><span data-ttu-id="10c13-103">Função ORCreateHive</span><span class="sxs-lookup"><span data-stu-id="10c13-103">ORCreateHive function</span></span>

<span data-ttu-id="10c13-104">Cria um hive de registro offline que contém uma única chave de raiz vazia.</span><span class="sxs-lookup"><span data-stu-id="10c13-104">Creates an offline registry hive that contains a single empty root key.</span></span>

## <a name="syntax"></a><span data-ttu-id="10c13-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10c13-105">Syntax</span></span>


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="10c13-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10c13-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10c13-107">*phkResult* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="10c13-107">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10c13-108">Aponta para uma variável para receber um identificador para a chave raiz do hive do registro offline recém-criado.</span><span class="sxs-lookup"><span data-stu-id="10c13-108">Points to a variable to receive a handle to the root key of the newly created offline registry hive.</span></span> <span data-ttu-id="10c13-109">Se o hive não puder ser criado, a função definirá esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="10c13-109">If the hive cannot be created, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10c13-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10c13-110">Return value</span></span>

<span data-ttu-id="10c13-111">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="10c13-111">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="10c13-112">Se a função falhar, o valor de retorno será um código de erro diferente de zero definido em Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="10c13-112">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="10c13-113">Você pode usar a função [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) com a \_ mensagem de formato \_ do \_ sinalizador do sistema para obter uma descrição genérica do erro.</span><span class="sxs-lookup"><span data-stu-id="10c13-113">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="10c13-114">Se não houver memória suficiente para criar o hive do registro, a função retornará um erro de \_ \_ memória insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="10c13-114">If there is insufficient memory to create the registry hive, the function returns ERROR\_NOT\_ENOUGH\_MEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="10c13-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="10c13-115">Remarks</span></span>

<span data-ttu-id="10c13-116">A função **ORCreateHive** cria um hive de registro offline vazio na memória.</span><span class="sxs-lookup"><span data-stu-id="10c13-116">The **ORCreateHive** function creates an empty offline registry hive in memory.</span></span> <span data-ttu-id="10c13-117">Use as funções [**ORCreateKey**](orcreatekey.md) e [**ORSetValue**](orsetvalue.md) para adicionar chaves e definir seus valores.</span><span class="sxs-lookup"><span data-stu-id="10c13-117">Use the [**ORCreateKey**](orcreatekey.md) and [**ORSetValue**](orsetvalue.md) functions to add keys and set their values.</span></span>

## <a name="requirements"></a><span data-ttu-id="10c13-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10c13-118">Requirements</span></span>



| <span data-ttu-id="10c13-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10c13-119">Requirement</span></span> | <span data-ttu-id="10c13-120">Valor</span><span class="sxs-lookup"><span data-stu-id="10c13-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10c13-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="10c13-121">Redistributable</span></span><br/> | <span data-ttu-id="10c13-122">Biblioteca de registro offline do Windows versão 1,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="10c13-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="10c13-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="10c13-123">Header</span></span><br/>          | <dl> <span data-ttu-id="10c13-124"><dt>Offreg. h</dt></span><span class="sxs-lookup"><span data-stu-id="10c13-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="10c13-125">DLL</span><span class="sxs-lookup"><span data-stu-id="10c13-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="10c13-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10c13-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10c13-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="10c13-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10c13-128">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="10c13-128">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="10c13-129">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="10c13-129">**OROpenHive**</span></span>](oropenhive.md)
</dt> <dt>

[<span data-ttu-id="10c13-130">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="10c13-130">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="10c13-131">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="10c13-131">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
