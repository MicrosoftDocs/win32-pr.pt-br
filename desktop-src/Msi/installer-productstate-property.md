---
description: A propriedade Productstate é uma propriedade somente leitura que retorna as informações de estado de instalação de um produto.
ms.assetid: 9ae3bc86-aa13-41b3-b058-4037607f7dd5
title: Método de Propriedade Installer. Productstate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cdd1397def1cd25405d0a80a6d5cfde2ee6ef77e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748153"
---
# <a name="installerproductstate-property-method"></a><span data-ttu-id="dccca-103">Método de Propriedade Installer. Productstate</span><span class="sxs-lookup"><span data-stu-id="dccca-103">Installer.ProductState Property method</span></span>

<span data-ttu-id="dccca-104">A **Propriedade productstate** é uma propriedade somente leitura que retorna as informações de estado de instalação de um produto.</span><span class="sxs-lookup"><span data-stu-id="dccca-104">The **ProductState property** is a read-only property that returns the install state information for a product.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dccca-105">Syntax</span></span>


```JScript
Installer.ProductState Property(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="dccca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dccca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccca-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="dccca-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="dccca-108">Especifica o código do produto do produto.</span><span class="sxs-lookup"><span data-stu-id="dccca-108">Specifies the product code of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccca-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dccca-109">Return value</span></span>

<span data-ttu-id="dccca-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="dccca-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dccca-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="dccca-111">Remarks</span></span>

<span data-ttu-id="dccca-112">Retorna um dos valores mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="dccca-112">Returns one of the values shown in the following table.</span></span>



| <span data-ttu-id="dccca-113">Estado de instalação</span><span class="sxs-lookup"><span data-stu-id="dccca-113">Installation state</span></span>        | <span data-ttu-id="dccca-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dccca-114">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="dccca-115">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="dccca-115">msiInstallStateAbsent</span></span>     | <span data-ttu-id="dccca-116">O produto está instalado para um usuário diferente.</span><span class="sxs-lookup"><span data-stu-id="dccca-116">The product is installed for a different user.</span></span>   |
| <span data-ttu-id="dccca-117">msiInstallStateDefault</span><span class="sxs-lookup"><span data-stu-id="dccca-117">msiInstallStateDefault</span></span>    | <span data-ttu-id="dccca-118">O produto está instalado para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="dccca-118">The product is installed for the current user.</span></span>   |
| <span data-ttu-id="dccca-119">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="dccca-119">msiInstallStateAdvertised</span></span> | <span data-ttu-id="dccca-120">O produto é anunciado, mas não está instalado.</span><span class="sxs-lookup"><span data-stu-id="dccca-120">The product is advertised but not installed.</span></span>     |
| <span data-ttu-id="dccca-121">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="dccca-121">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="dccca-122">Um parâmetro inválido foi passado para a função.</span><span class="sxs-lookup"><span data-stu-id="dccca-122">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="dccca-123">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="dccca-123">msiInstallStateUnknown</span></span>    | <span data-ttu-id="dccca-124">O produto não está anunciado nem instalado.</span><span class="sxs-lookup"><span data-stu-id="dccca-124">The product is neither advertised nor installed.</span></span> |
| <span data-ttu-id="dccca-125">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="dccca-125">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="dccca-126">Os dados de configuração estão corrompidos.</span><span class="sxs-lookup"><span data-stu-id="dccca-126">The configuration data is corrupt.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="dccca-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dccca-127">Requirements</span></span>



| <span data-ttu-id="dccca-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="dccca-128">Requirement</span></span> | <span data-ttu-id="dccca-129">Valor</span><span class="sxs-lookup"><span data-stu-id="dccca-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dccca-130">Versão</span><span class="sxs-lookup"><span data-stu-id="dccca-130">Version</span></span><br/> | <span data-ttu-id="dccca-131">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dccca-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="dccca-132">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dccca-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="dccca-133">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="dccca-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="dccca-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dccca-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="dccca-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dccca-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="dccca-136">IID</span><span class="sxs-lookup"><span data-stu-id="dccca-136">IID</span></span><br/>     | <span data-ttu-id="dccca-137">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="dccca-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="dccca-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="dccca-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccca-139">**MsiQueryProductState**</span><span class="sxs-lookup"><span data-stu-id="dccca-139">**MsiQueryProductState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)
</dt> </dl>

 

 




