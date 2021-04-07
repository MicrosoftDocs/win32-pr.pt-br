---
title: Método KeyValueDelete da classe Win32_RDSHCollection
description: Exclui a chave especificada (e o valor associado) da coleção.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método KeyValueDelete
- Método KeyValueDelete Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método KeyValueDelete
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918308"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="475a6-106">Método KeyValueDelete da classe Win32 \_ RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="475a6-106">KeyValueDelete method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="475a6-107">Exclui a chave especificada (e o valor associado) da coleção.</span><span class="sxs-lookup"><span data-stu-id="475a6-107">Deletes the specified key (and associated value) from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="475a6-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="475a6-108">Syntax</span></span>


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="475a6-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="475a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475a6-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="475a6-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="475a6-111">A chave a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="475a6-111">The key to delete.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="475a6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="475a6-112">Requirements</span></span>



| <span data-ttu-id="475a6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="475a6-113">Requirement</span></span> | <span data-ttu-id="475a6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="475a6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="475a6-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="475a6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="475a6-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="475a6-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="475a6-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="475a6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="475a6-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="475a6-118">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="475a6-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="475a6-119">Namespace</span></span><br/>                | <span data-ttu-id="475a6-120">\\RDMs cimv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="475a6-120">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="475a6-121">MOF</span><span class="sxs-lookup"><span data-stu-id="475a6-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="475a6-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="475a6-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="475a6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="475a6-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="475a6-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="475a6-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="475a6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="475a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="475a6-126">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="475a6-126">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





