---
description: O método ForceSourceListResolution do objeto instalador força a Windows Installer a Pesquisar a lista de origem em busca de uma origem de produto válida.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Método Installer. ForceSourceListResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752850"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="10d73-103">Método Installer. ForceSourceListResolution</span><span class="sxs-lookup"><span data-stu-id="10d73-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="10d73-104">O método **ForceSourceListResolution** do objeto [**instalador**](installer-object.md) força o instalador a Pesquisar a lista de origem para uma fonte de produto válida na próxima vez que uma fonte for necessária, como quando o instalador executa uma instalação ou reinstalação, ou quando precisa do caminho para um conjunto de componentes ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="10d73-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d73-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="10d73-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="10d73-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="10d73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d73-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="10d73-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="10d73-108">Especifica o código do produto.</span><span class="sxs-lookup"><span data-stu-id="10d73-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="10d73-109">*Usuário*</span><span class="sxs-lookup"><span data-stu-id="10d73-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="10d73-110">Nome de usuário para instalação por usuário; Cadeia de caracteres nula ou vazia para instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="10d73-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d73-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="10d73-111">Return value</span></span>

<span data-ttu-id="10d73-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="10d73-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d73-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10d73-113">Requirements</span></span>



| <span data-ttu-id="10d73-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="10d73-114">Requirement</span></span> | <span data-ttu-id="10d73-115">Valor</span><span class="sxs-lookup"><span data-stu-id="10d73-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d73-116">Versão</span><span class="sxs-lookup"><span data-stu-id="10d73-116">Version</span></span><br/> | <span data-ttu-id="10d73-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="10d73-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="10d73-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="10d73-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="10d73-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="10d73-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="10d73-120">DLL</span><span class="sxs-lookup"><span data-stu-id="10d73-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="10d73-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d73-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="10d73-122">IID</span><span class="sxs-lookup"><span data-stu-id="10d73-122">IID</span></span><br/>     | <span data-ttu-id="10d73-123">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="10d73-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="10d73-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="10d73-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d73-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="10d73-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="10d73-126">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="10d73-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




