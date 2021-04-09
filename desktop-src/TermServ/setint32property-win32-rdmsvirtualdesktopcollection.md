---
title: Método setint32property da classe Win32_RDMSVirtualDesktopCollection
description: Atualiza uma propriedade de inteiro de uma coleção de áreas de trabalho virtuais.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- Método setint32property Serviços de Área de Trabalho Remota
- Método setint32property Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método setint32property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086277"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="745c7-106">Método setint32property da classe Win32 \_ RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="745c7-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="745c7-107">Atualiza uma propriedade de inteiro de uma coleção de áreas de trabalho virtuais.</span><span class="sxs-lookup"><span data-stu-id="745c7-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="745c7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="745c7-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="745c7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="745c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="745c7-110">*Chave* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="745c7-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c7-111">Uma chave que identifica a propriedade a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="745c7-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="745c7-112">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="745c7-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="745c7-113">O novo valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="745c7-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="745c7-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="745c7-114">Return value</span></span>

<span data-ttu-id="745c7-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="745c7-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="745c7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="745c7-116">Requirements</span></span>



| <span data-ttu-id="745c7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="745c7-117">Requirement</span></span> | <span data-ttu-id="745c7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="745c7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="745c7-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="745c7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="745c7-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="745c7-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="745c7-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="745c7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="745c7-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="745c7-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="745c7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="745c7-123">Namespace</span></span><br/>                | <span data-ttu-id="745c7-124">\\RDMs CIMv2 \\ raiz</span><span class="sxs-lookup"><span data-stu-id="745c7-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="745c7-125">MOF</span><span class="sxs-lookup"><span data-stu-id="745c7-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="745c7-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="745c7-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="745c7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="745c7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="745c7-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="745c7-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="745c7-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="745c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="745c7-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="745c7-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





