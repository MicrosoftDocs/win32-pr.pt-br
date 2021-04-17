---
description: O método ClearSourceList do objeto do instalador remove todas as fontes de rede da lista de origem.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Método Installer. ClearSourceList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748156"
---
# <a name="installerclearsourcelist-method"></a><span data-ttu-id="73c27-103">Método Installer. ClearSourceList</span><span class="sxs-lookup"><span data-stu-id="73c27-103">Installer.ClearSourceList method</span></span>

<span data-ttu-id="73c27-104">O método **ClearSourceList** do objeto do [**instalador**](installer-object.md) remove todas as fontes de rede da lista de origem.</span><span class="sxs-lookup"><span data-stu-id="73c27-104">The **ClearSourceList** method of the [**Installer**](installer-object.md) object removes all network sources from the source list.</span></span>

## <a name="syntax"></a><span data-ttu-id="73c27-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73c27-105">Syntax</span></span>


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="73c27-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73c27-107">*Product*</span><span class="sxs-lookup"><span data-stu-id="73c27-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="73c27-108">Especifica o código do produto.</span><span class="sxs-lookup"><span data-stu-id="73c27-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="73c27-109">*Usuário*</span><span class="sxs-lookup"><span data-stu-id="73c27-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="73c27-110">Nome de usuário para instalação por usuário; Cadeia de caracteres nula ou vazia para instalação por máquina.</span><span class="sxs-lookup"><span data-stu-id="73c27-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73c27-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73c27-111">Return value</span></span>

<span data-ttu-id="73c27-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="73c27-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="73c27-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73c27-113">Requirements</span></span>



| <span data-ttu-id="73c27-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="73c27-114">Requirement</span></span> | <span data-ttu-id="73c27-115">Valor</span><span class="sxs-lookup"><span data-stu-id="73c27-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73c27-116">Versão</span><span class="sxs-lookup"><span data-stu-id="73c27-116">Version</span></span><br/> | <span data-ttu-id="73c27-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73c27-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="73c27-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="73c27-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="73c27-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="73c27-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="73c27-120">DLL</span><span class="sxs-lookup"><span data-stu-id="73c27-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="73c27-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73c27-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="73c27-122">IID</span><span class="sxs-lookup"><span data-stu-id="73c27-122">IID</span></span><br/>     | <span data-ttu-id="73c27-123">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="73c27-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="73c27-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="73c27-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73c27-125">**MsiSourceListClearAll**</span><span class="sxs-lookup"><span data-stu-id="73c27-125">**MsiSourceListClearAll**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[<span data-ttu-id="73c27-126">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="73c27-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




