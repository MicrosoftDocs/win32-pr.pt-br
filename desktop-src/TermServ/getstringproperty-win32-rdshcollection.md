---
title: Método getstringproperty da classe Win32_RDSHCollection
description: Recupera um valor de propriedade da cadeia de caracteres de um \_ objeto RDSHCollection do Win32.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918138"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="c6f99-106">Método getstringproperty da classe Win32 \_ RDSHCollection</span><span class="sxs-lookup"><span data-stu-id="c6f99-106">GetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="c6f99-107">Recupera um valor de propriedade da cadeia de caracteres de um objeto [**\_ RDSHCollection do Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c6f99-107">Retrieves a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f99-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c6f99-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="c6f99-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c6f99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6f99-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c6f99-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f99-111">A chave que identifica a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="c6f99-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c6f99-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="c6f99-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c6f99-113">Recebe o valor da propriedade recuperada.</span><span class="sxs-lookup"><span data-stu-id="c6f99-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6f99-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c6f99-114">Return value</span></span>

<span data-ttu-id="c6f99-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="c6f99-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f99-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6f99-116">Requirements</span></span>



| <span data-ttu-id="c6f99-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f99-117">Requirement</span></span> | <span data-ttu-id="c6f99-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c6f99-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f99-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6f99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f99-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c6f99-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c6f99-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6f99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f99-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c6f99-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c6f99-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c6f99-123">Namespace</span></span><br/>                | <span data-ttu-id="c6f99-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="c6f99-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c6f99-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c6f99-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6f99-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6f99-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c6f99-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c6f99-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f99-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f99-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c6f99-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6f99-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f99-130">**\_RDSHCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="c6f99-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





