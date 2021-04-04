---
title: Método setstringproperty da classe Win32_RDSHServer (CertEnroll. h)
description: Atualiza um valor de propriedade de cadeia de caracteres de um \_ objeto Win32 RDSHServer.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Método setstringproperty Serviços de Área de Trabalho Remota
- Método setstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método setstringproperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d30812c0df943175f96c8ae43a4fe094725c74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085862"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="2188e-106">Método setstringproperty da classe Win32 \_ RDSHServer</span><span class="sxs-lookup"><span data-stu-id="2188e-106">SetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="2188e-107">Atualiza um valor de propriedade de cadeia de caracteres de um objeto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="2188e-107">Updates a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2188e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2188e-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="2188e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2188e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2188e-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2188e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2188e-111">A chave que identifica a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="2188e-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="2188e-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2188e-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2188e-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="2188e-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2188e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2188e-114">Return value</span></span>

<span data-ttu-id="2188e-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="2188e-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2188e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2188e-116">Requirements</span></span>



| <span data-ttu-id="2188e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2188e-117">Requirement</span></span> | <span data-ttu-id="2188e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2188e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2188e-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2188e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2188e-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2188e-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2188e-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2188e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2188e-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2188e-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2188e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2188e-123">Namespace</span></span><br/>                | <span data-ttu-id="2188e-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="2188e-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2188e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2188e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2188e-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="2188e-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="2188e-127">MOF</span><span class="sxs-lookup"><span data-stu-id="2188e-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2188e-128"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2188e-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2188e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2188e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2188e-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2188e-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2188e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="2188e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2188e-132">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="2188e-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





