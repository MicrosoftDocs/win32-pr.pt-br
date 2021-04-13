---
title: Método getstringproperty da classe Win32_RDSHServer
description: Recupera um valor de propriedade da cadeia de caracteres de um \_ objeto RDSHServer do Win32.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455946"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="fd66a-106">Método getstringproperty da classe Win32 \_ RDSHServer</span><span class="sxs-lookup"><span data-stu-id="fd66a-106">GetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="fd66a-107">Recupera um valor de propriedade da cadeia de caracteres de um objeto [**\_ RDSHServer do Win32**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="fd66a-107">Retrieves a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd66a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd66a-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="fd66a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd66a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd66a-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd66a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd66a-111">A chave que identifica a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="fd66a-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="fd66a-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="fd66a-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd66a-113">Recebe o valor da propriedade recuperada.</span><span class="sxs-lookup"><span data-stu-id="fd66a-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd66a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd66a-114">Return value</span></span>

<span data-ttu-id="fd66a-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="fd66a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd66a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd66a-116">Requirements</span></span>



| <span data-ttu-id="fd66a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd66a-117">Requirement</span></span> | <span data-ttu-id="fd66a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fd66a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd66a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd66a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fd66a-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fd66a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fd66a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fd66a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fd66a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fd66a-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fd66a-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd66a-123">Namespace</span></span><br/>                | <span data-ttu-id="fd66a-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="fd66a-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fd66a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fd66a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd66a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd66a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd66a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fd66a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd66a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd66a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fd66a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd66a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd66a-130">**\_RDSHServer Win32**</span><span class="sxs-lookup"><span data-stu-id="fd66a-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





