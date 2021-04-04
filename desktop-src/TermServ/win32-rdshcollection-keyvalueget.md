---
title: Método KeyValueGet da classe Win32_RDSHCollection
description: Recupera o valor associado à chave especificada na coleção.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método KeyValueGet
- Método KeyValueGet Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824318"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="55da2-106">Método KeyValueGet da classe Win32 \_ RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="55da2-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="55da2-107">Recupera o valor associado à chave especificada na coleção.</span><span class="sxs-lookup"><span data-stu-id="55da2-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="55da2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55da2-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="55da2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55da2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55da2-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="55da2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55da2-111">A chave que identifica o valor que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="55da2-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="55da2-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="55da2-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55da2-113">Em caso de sucesso, retorna o valor associado à chave especificada.</span><span class="sxs-lookup"><span data-stu-id="55da2-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55da2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55da2-114">Requirements</span></span>



| <span data-ttu-id="55da2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="55da2-115">Requirement</span></span> | <span data-ttu-id="55da2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="55da2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="55da2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55da2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55da2-118">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="55da2-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="55da2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55da2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55da2-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="55da2-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="55da2-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="55da2-121">Namespace</span></span><br/>                | <span data-ttu-id="55da2-122">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="55da2-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="55da2-123">MOF</span><span class="sxs-lookup"><span data-stu-id="55da2-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55da2-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55da2-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="55da2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="55da2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55da2-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55da2-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="55da2-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="55da2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55da2-128">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="55da2-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





