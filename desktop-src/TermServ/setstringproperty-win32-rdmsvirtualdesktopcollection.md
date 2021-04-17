---
title: Método setstringproperty da classe Win32_RDMSVirtualDesktopCollection (CertEnroll. h)
description: Atualiza uma propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- Método setstringproperty Serviços de Área de Trabalho Remota
- Método setstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método setstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758377"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="875f2-106">Método setstringproperty da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="875f2-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="875f2-107">Atualiza uma propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="875f2-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="875f2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="875f2-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="875f2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="875f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875f2-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="875f2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875f2-111">Uma chave que identifica a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="875f2-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="875f2-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="875f2-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="875f2-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="875f2-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875f2-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="875f2-114">Return value</span></span>

<span data-ttu-id="875f2-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="875f2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="875f2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="875f2-116">Requirements</span></span>



| <span data-ttu-id="875f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="875f2-117">Requirement</span></span> | <span data-ttu-id="875f2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="875f2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="875f2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="875f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="875f2-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="875f2-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="875f2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="875f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="875f2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="875f2-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="875f2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="875f2-123">Namespace</span></span><br/>                | <span data-ttu-id="875f2-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="875f2-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="875f2-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="875f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="875f2-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="875f2-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="875f2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="875f2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="875f2-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="875f2-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="875f2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="875f2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875f2-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="875f2-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="875f2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="875f2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875f2-132">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="875f2-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





