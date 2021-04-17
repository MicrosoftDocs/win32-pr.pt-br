---
title: Método getstringproperty da classe Win32_RDMSVirtualDesktopCollection
description: Recupera uma propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753524"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="6d0eb-106">Método getstringproperty da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="6d0eb-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="6d0eb-107">Recupera uma propriedade de cadeia de caracteres de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0eb-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d0eb-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="6d0eb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d0eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0eb-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6d0eb-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0eb-111">Uma chave que identifica a propriedade a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6d0eb-112">*Valor* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="6d0eb-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0eb-113">Uma cadeia de caracteres que recebe o valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0eb-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d0eb-114">Return value</span></span>

<span data-ttu-id="6d0eb-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d0eb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d0eb-116">Requirements</span></span>



| <span data-ttu-id="6d0eb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d0eb-117">Requirement</span></span> | <span data-ttu-id="6d0eb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6d0eb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0eb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d0eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d0eb-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6d0eb-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6d0eb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d0eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d0eb-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d0eb-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6d0eb-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d0eb-123">Namespace</span></span><br/>                | <span data-ttu-id="6d0eb-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="6d0eb-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6d0eb-125">MOF</span><span class="sxs-lookup"><span data-stu-id="6d0eb-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d0eb-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d0eb-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d0eb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6d0eb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d0eb-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d0eb-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6d0eb-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d0eb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0eb-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="6d0eb-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





