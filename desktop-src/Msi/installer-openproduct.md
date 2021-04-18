---
description: O método OpenProduct do objeto do instalador abre um pacote do instalador para um produto instalado usando o código do produto e retorna um objeto de sessão.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Método Installer. OpenProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752848"
---
# <a name="installeropenproduct-method"></a><span data-ttu-id="6456a-103">Método Installer. OpenProduct</span><span class="sxs-lookup"><span data-stu-id="6456a-103">Installer.OpenProduct method</span></span>

<span data-ttu-id="6456a-104">O método **OpenProduct** do objeto do [**instalador**](installer-object.md) abre um pacote do instalador para um produto instalado usando o código do produto e retorna um objeto de [**sessão**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="6456a-104">The **OpenProduct** method of the [**Installer**](installer-object.md) object opens an installer package for an installed product using the product code and returns a [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6456a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6456a-105">Syntax</span></span>


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a><span data-ttu-id="6456a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6456a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6456a-107">*productCode*</span><span class="sxs-lookup"><span data-stu-id="6456a-107">*productCode*</span></span> 
</dt> <dd>

<span data-ttu-id="6456a-108">Cadeia de caracteres necessária que contém o código de produto exclusivo (um [GUID](guid.md)) ou um descritor de ativação escrito pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="6456a-108">Required string containing the unique product code (a [GUID](guid.md)) or an activation descriptor written by the installer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6456a-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6456a-109">Return value</span></span>

<span data-ttu-id="6456a-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6456a-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6456a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6456a-111">Remarks</span></span>

<span data-ttu-id="6456a-112">Observe que apenas um objeto de [**sessão**](session-object.md) pode ser aberto por um único processo.</span><span class="sxs-lookup"><span data-stu-id="6456a-112">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="6456a-113">**OpenProduct** não pode ser usado em uma ação personalizada porque a instalação ativa é a única sessão permitida.</span><span class="sxs-lookup"><span data-stu-id="6456a-113">**OpenProduct** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

## <a name="requirements"></a><span data-ttu-id="6456a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6456a-114">Requirements</span></span>



| <span data-ttu-id="6456a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6456a-115">Requirement</span></span> | <span data-ttu-id="6456a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6456a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6456a-117">Versão</span><span class="sxs-lookup"><span data-stu-id="6456a-117">Version</span></span><br/> | <span data-ttu-id="6456a-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6456a-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6456a-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6456a-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6456a-120">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="6456a-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="6456a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6456a-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="6456a-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6456a-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="6456a-123">IID</span><span class="sxs-lookup"><span data-stu-id="6456a-123">IID</span></span><br/>     | <span data-ttu-id="6456a-124">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="6456a-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




