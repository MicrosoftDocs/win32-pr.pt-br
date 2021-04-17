---
description: O método OpenPackage do objeto do instalador abre um pacote do instalador para uso com funções que acessam o banco de dados do produto e o mecanismo de instalação, retornando um objeto de sessão.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Método Installer. OpenPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747543"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="6b273-103">Método Installer. OpenPackage</span><span class="sxs-lookup"><span data-stu-id="6b273-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="6b273-104">O método **OpenPackage** do objeto do [**instalador**](installer-object.md) abre um pacote do instalador para uso com funções que acessam o banco de dados do produto e o mecanismo de instalação, retornando um objeto de [**sessão**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6b273-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b273-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b273-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="6b273-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b273-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="6b273-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="6b273-108">Cadeia de caracteres necessária que contém o nome do caminho do pacote.</span><span class="sxs-lookup"><span data-stu-id="6b273-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="6b273-109">*options*</span><span class="sxs-lookup"><span data-stu-id="6b273-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="6b273-110">Um valor inteiro opcional que especifica se **OpenPackage** deve ou não ignorar o estado atual do computador ao criar o objeto de sessão.</span><span class="sxs-lookup"><span data-stu-id="6b273-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="6b273-111">Nenhum valor ou um valor de 0 para opções usa como padrão o comportamento original.</span><span class="sxs-lookup"><span data-stu-id="6b273-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="6b273-112">Quando as opções são 1, o método **OpenPackage** ignora o estado atual do computador ao abrir o pacote.</span><span class="sxs-lookup"><span data-stu-id="6b273-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="6b273-113">Um valor de 1 impede alterações no estado atual do computador.</span><span class="sxs-lookup"><span data-stu-id="6b273-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="6b273-114">Para obter mais informações, consulte [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="6b273-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b273-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6b273-115">Return value</span></span>

<span data-ttu-id="6b273-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6b273-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b273-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b273-117">Remarks</span></span>

<span data-ttu-id="6b273-118">O método **OpenPackage** pode aceitar o identificador de banco de dados diretamente em vez da cadeia de caracteres para o caminho do pacote.</span><span class="sxs-lookup"><span data-stu-id="6b273-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="6b273-119">Observe que apenas um objeto de [**sessão**](session-object.md) pode ser aberto por um único processo.</span><span class="sxs-lookup"><span data-stu-id="6b273-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="6b273-120">**OpenPackage** não pode ser usado em uma ação personalizada porque a instalação ativa é a única sessão permitida.</span><span class="sxs-lookup"><span data-stu-id="6b273-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="6b273-121">Um objeto de [**sessão**](session-object.md) seguro ignora o estado atual do computador ao abrir o pacote e impede alterações no estado atual do computador.</span><span class="sxs-lookup"><span data-stu-id="6b273-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="6b273-122">Para obter mais informações, consulte [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="6b273-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b273-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b273-123">Requirements</span></span>



| <span data-ttu-id="6b273-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b273-124">Requirement</span></span> | <span data-ttu-id="6b273-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6b273-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b273-126">Versão</span><span class="sxs-lookup"><span data-stu-id="6b273-126">Version</span></span><br/> | <span data-ttu-id="6b273-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6b273-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6b273-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6b273-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6b273-129">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b273-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6b273-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6b273-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b273-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b273-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6b273-132">IID</span><span class="sxs-lookup"><span data-stu-id="6b273-132">IID</span></span><br/>     | <span data-ttu-id="6b273-133">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6b273-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




