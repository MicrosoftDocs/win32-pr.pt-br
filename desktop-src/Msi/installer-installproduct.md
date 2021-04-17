---
description: O método InstallProduct do objeto do instalador abre um pacote do instalador e Inicializa uma sessão de instalação.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Método Installer. InstallProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749791"
---
# <a name="installerinstallproduct-method"></a><span data-ttu-id="af822-103">Método Installer. InstallProduct</span><span class="sxs-lookup"><span data-stu-id="af822-103">Installer.InstallProduct method</span></span>

<span data-ttu-id="af822-104">O método **InstallProduct** do objeto do [**instalador**](installer-object.md) abre um pacote do instalador e Inicializa uma sessão de instalação.</span><span class="sxs-lookup"><span data-stu-id="af822-104">The **InstallProduct** method of the [**Installer**](installer-object.md) object opens an installer package and initializes an install session.</span></span>

## <a name="syntax"></a><span data-ttu-id="af822-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="af822-105">Syntax</span></span>


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a><span data-ttu-id="af822-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="af822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af822-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="af822-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="af822-108">Cadeia de caracteres necessária que contém o caminho para o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="af822-108">Required string containing the path to the install package.</span></span>

</dd> <dt>

<span data-ttu-id="af822-109">*propertyValues*</span><span class="sxs-lookup"><span data-stu-id="af822-109">*propertyValues*</span></span> 
</dt> <dd>

<span data-ttu-id="af822-110">Cadeia de caracteres opcional que contém os pares de propriedade = valor separados por espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="af822-110">Optional string containing property=value pairs separated by white space.</span></span>

<span data-ttu-id="af822-111">Para executar uma instalação administrativa, inclua ACTION = ADMIN em *PropertyValues*.</span><span class="sxs-lookup"><span data-stu-id="af822-111">To perform an administrative installation, include ACTION=ADMIN in *propertyValues*.</span></span> <span data-ttu-id="af822-112">Para obter mais informações, consulte a propriedade [**Action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="af822-112">For more information, see the [**ACTION**](action.md) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af822-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="af822-113">Return value</span></span>

<span data-ttu-id="af822-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="af822-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="af822-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="af822-115">Remarks</span></span>

<span data-ttu-id="af822-116">Para remover completamente um produto, defina REMOVE = ALL em *PropertyValues*.</span><span class="sxs-lookup"><span data-stu-id="af822-116">To completely remove a product, set REMOVE=ALL in *propertyValues*.</span></span> <span data-ttu-id="af822-117">Para obter mais informações, consulte [**remover**](remove.md) propriedade.</span><span class="sxs-lookup"><span data-stu-id="af822-117">For more information, see [**REMOVE**](remove.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="af822-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af822-118">Requirements</span></span>



| <span data-ttu-id="af822-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="af822-119">Requirement</span></span> | <span data-ttu-id="af822-120">Valor</span><span class="sxs-lookup"><span data-stu-id="af822-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af822-121">Versão</span><span class="sxs-lookup"><span data-stu-id="af822-121">Version</span></span><br/> | <span data-ttu-id="af822-122">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af822-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="af822-123">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="af822-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="af822-124">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="af822-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="af822-125">DLL</span><span class="sxs-lookup"><span data-stu-id="af822-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="af822-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af822-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="af822-127">IID</span><span class="sxs-lookup"><span data-stu-id="af822-127">IID</span></span><br/>     | <span data-ttu-id="af822-128">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="af822-128">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




