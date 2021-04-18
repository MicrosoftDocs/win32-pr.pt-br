---
title: Método setint32property da classe Win32_RDSHCollection
description: Atualiza um valor da propriedade Integer de um \_ objeto RDSHCollection do Win32.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Método setint32property Serviços de Área de Trabalho Remota
- Método setint32property Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método setint32property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788028"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="33182-106">Método setint32property da classe Win32 \_ RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="33182-106">SetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="33182-107">Atualiza um valor da propriedade Integer de um objeto [**\_ RDSHCollection do Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="33182-107">Updates an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="33182-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33182-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="33182-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33182-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33182-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33182-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33182-111">A chave que identifica a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="33182-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="33182-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="33182-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33182-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="33182-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33182-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33182-114">Return value</span></span>

<span data-ttu-id="33182-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="33182-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="33182-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33182-116">Requirements</span></span>



| <span data-ttu-id="33182-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="33182-117">Requirement</span></span> | <span data-ttu-id="33182-118">Valor</span><span class="sxs-lookup"><span data-stu-id="33182-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="33182-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33182-119">Minimum supported client</span></span><br/> | <span data-ttu-id="33182-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="33182-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="33182-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33182-121">Minimum supported server</span></span><br/> | <span data-ttu-id="33182-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="33182-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="33182-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="33182-123">Namespace</span></span><br/>                | <span data-ttu-id="33182-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="33182-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="33182-125">MOF</span><span class="sxs-lookup"><span data-stu-id="33182-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33182-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33182-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="33182-127">DLL</span><span class="sxs-lookup"><span data-stu-id="33182-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33182-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33182-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="33182-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="33182-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33182-130">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="33182-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





