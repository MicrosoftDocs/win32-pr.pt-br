---
title: Método setstringproperty da classe Win32_RDSHCollection (CertEnroll. h)
description: Atualiza um valor de propriedade de cadeia de caracteres de um \_ objeto Win32 RDSHCollection.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- Método setstringproperty Serviços de Área de Trabalho Remota
- Método setstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método setstringproperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769376"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="2d627-106">Método setstringproperty da classe Win32 \_ RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="2d627-106">SetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="2d627-107">Atualiza um valor de propriedade de cadeia de caracteres de um objeto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2d627-107">Updates a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d627-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d627-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="2d627-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d627-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d627-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d627-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d627-111">A chave que identifica a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="2d627-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="2d627-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2d627-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d627-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2d627-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d627-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d627-114">Return value</span></span>

<span data-ttu-id="2d627-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2d627-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d627-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d627-116">Requirements</span></span>



| <span data-ttu-id="2d627-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d627-117">Requirement</span></span> | <span data-ttu-id="2d627-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2d627-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d627-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d627-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2d627-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2d627-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2d627-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d627-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2d627-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2d627-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2d627-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2d627-123">Namespace</span></span><br/>                | <span data-ttu-id="2d627-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="2d627-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2d627-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d627-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d627-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d627-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="2d627-127">MOF</span><span class="sxs-lookup"><span data-stu-id="2d627-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2d627-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2d627-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2d627-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2d627-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d627-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d627-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2d627-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d627-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d627-132">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2d627-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





