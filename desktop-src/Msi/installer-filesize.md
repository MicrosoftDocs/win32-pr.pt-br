---
description: O método FileSize do objeto instalador usa as chamadas à API do Win32 para retornar o tamanho do arquivo especificado em path.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Método Installer. FileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747764"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="e0629-103">Método Installer. FileSize</span><span class="sxs-lookup"><span data-stu-id="e0629-103">Installer.FileSize method</span></span>

<span data-ttu-id="e0629-104">O método **filesize** do objeto [**instalador**](installer-object.md) usa as chamadas à API do Win32 para retornar o tamanho do arquivo especificado em *Path*.</span><span class="sxs-lookup"><span data-stu-id="e0629-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0629-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0629-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="e0629-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0629-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0629-107">*Caminho*</span><span class="sxs-lookup"><span data-stu-id="e0629-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="e0629-108">Cadeia de caracteres necessária que contém o caminho para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="e0629-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0629-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0629-109">Return value</span></span>

<span data-ttu-id="e0629-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e0629-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0629-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0629-111">Requirements</span></span>



| <span data-ttu-id="e0629-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0629-112">Requirement</span></span> | <span data-ttu-id="e0629-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e0629-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0629-114">Versão</span><span class="sxs-lookup"><span data-stu-id="e0629-114">Version</span></span><br/> | <span data-ttu-id="e0629-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e0629-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e0629-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e0629-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e0629-117">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e0629-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e0629-118">DLL</span><span class="sxs-lookup"><span data-stu-id="e0629-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0629-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0629-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e0629-120">IID</span><span class="sxs-lookup"><span data-stu-id="e0629-120">IID</span></span><br/>     | <span data-ttu-id="e0629-121">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e0629-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




