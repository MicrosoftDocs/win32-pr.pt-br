---
title: Método setint32property da classe Win32_RDSHServer
description: Atualiza um valor da propriedade Integer de um \_ objeto RDSHServer do Win32.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Método setint32property Serviços de Área de Trabalho Remota
- Método setint32property Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método setint32property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644599"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="27df9-106">Método setint32property da classe Win32 \_ RDSHServer</span><span class="sxs-lookup"><span data-stu-id="27df9-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="27df9-107">Atualiza um valor da propriedade Integer de um objeto [**\_ RDSHServer do Win32**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="27df9-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="27df9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="27df9-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="27df9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27df9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27df9-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="27df9-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27df9-111">A chave que identifica a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="27df9-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="27df9-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="27df9-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27df9-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="27df9-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27df9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27df9-114">Return value</span></span>

<span data-ttu-id="27df9-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="27df9-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="27df9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27df9-116">Requirements</span></span>



| <span data-ttu-id="27df9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="27df9-117">Requirement</span></span> | <span data-ttu-id="27df9-118">Valor</span><span class="sxs-lookup"><span data-stu-id="27df9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="27df9-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27df9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="27df9-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="27df9-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="27df9-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27df9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="27df9-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27df9-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="27df9-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="27df9-123">Namespace</span></span><br/>                | <span data-ttu-id="27df9-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="27df9-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="27df9-125">MOF</span><span class="sxs-lookup"><span data-stu-id="27df9-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27df9-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27df9-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="27df9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="27df9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27df9-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27df9-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="27df9-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="27df9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27df9-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="27df9-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





