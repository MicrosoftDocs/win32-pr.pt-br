---
description: O método addsource do objeto instalador adiciona uma fonte à lista de fontes de rede válidas na SourceList.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Método Installer. addsource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751196"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="79deb-103">Método Installer. addsource</span><span class="sxs-lookup"><span data-stu-id="79deb-103">Installer.AddSource method</span></span>

<span data-ttu-id="79deb-104">O método **addsource** do objeto [**instalador**](installer-object.md) adiciona uma fonte à lista de fontes de rede válidas na SourceList.</span><span class="sxs-lookup"><span data-stu-id="79deb-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="79deb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79deb-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="79deb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79deb-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="79deb-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="79deb-108">Especifica o código do produto.</span><span class="sxs-lookup"><span data-stu-id="79deb-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-109">*Usuário*</span><span class="sxs-lookup"><span data-stu-id="79deb-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="79deb-110">Nome de usuário para instalação por usuário; Cadeia de caracteres nula ou vazia para instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="79deb-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="79deb-111">*Origem*</span><span class="sxs-lookup"><span data-stu-id="79deb-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="79deb-112">Ponteiro para a cadeia de caracteres que especifica a origem.</span><span class="sxs-lookup"><span data-stu-id="79deb-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79deb-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79deb-113">Return value</span></span>

<span data-ttu-id="79deb-114">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="79deb-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="79deb-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79deb-115">Requirements</span></span>



| <span data-ttu-id="79deb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79deb-116">Requirement</span></span> | <span data-ttu-id="79deb-117">Valor</span><span class="sxs-lookup"><span data-stu-id="79deb-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79deb-118">Versão</span><span class="sxs-lookup"><span data-stu-id="79deb-118">Version</span></span><br/> | <span data-ttu-id="79deb-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79deb-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="79deb-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="79deb-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="79deb-121">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="79deb-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="79deb-122">DLL</span><span class="sxs-lookup"><span data-stu-id="79deb-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="79deb-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79deb-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="79deb-124">IID</span><span class="sxs-lookup"><span data-stu-id="79deb-124">IID</span></span><br/>     | <span data-ttu-id="79deb-125">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="79deb-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="79deb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="79deb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79deb-127">**MsiSourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="79deb-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="79deb-128">resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="79deb-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




