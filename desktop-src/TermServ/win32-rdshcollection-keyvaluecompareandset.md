---
title: Método KeyValueCompareAndSet da classe Win32_RDSHCollection
description: Compara a chave especificada na coleção com um termo; Se eles corresponderem, a chave será definida como um novo valor. Se a chave não existir, o método irá inserir a chave na coleção.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método KeyValueCompareAndSet
- Método KeyValueCompareAndSet Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824319"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="9ec53-107">Método KeyValueCompareAndSet da classe Win32 \_ RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="9ec53-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="9ec53-108">Compara a chave especificada na coleção com um termo; Se eles corresponderem, a chave será definida como um novo valor.</span><span class="sxs-lookup"><span data-stu-id="9ec53-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="9ec53-109">Se a chave não existir, o método irá inserir a chave na coleção.</span><span class="sxs-lookup"><span data-stu-id="9ec53-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec53-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9ec53-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="9ec53-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ec53-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec53-112">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ec53-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec53-113">A chave a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="9ec53-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-114">*NewValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ec53-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec53-115">O novo valor.</span><span class="sxs-lookup"><span data-stu-id="9ec53-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-116">*Termo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9ec53-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec53-117">A cadeia de caracteres para comparar a chave.</span><span class="sxs-lookup"><span data-stu-id="9ec53-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="9ec53-118">*Inicialvalue* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9ec53-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec53-119">Em caso de êxito ou falha, contém o valor inicial da chave.</span><span class="sxs-lookup"><span data-stu-id="9ec53-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ec53-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ec53-120">Remarks</span></span>

<span data-ttu-id="9ec53-121">Observe que esse método pode recuperar o valor da chave e, como tal, encapsula a funcionalidade de [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span><span class="sxs-lookup"><span data-stu-id="9ec53-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec53-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ec53-122">Requirements</span></span>



| <span data-ttu-id="9ec53-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ec53-123">Requirement</span></span> | <span data-ttu-id="9ec53-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9ec53-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec53-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ec53-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec53-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9ec53-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9ec53-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ec53-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec53-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9ec53-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="9ec53-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ec53-129">Namespace</span></span><br/>                | <span data-ttu-id="9ec53-130">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="9ec53-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9ec53-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9ec53-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ec53-132"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ec53-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ec53-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9ec53-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ec53-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ec53-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9ec53-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9ec53-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec53-136">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="9ec53-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





