---
description: A propriedade Environment do objeto instalador é uma propriedade de leitura/gravação que é o valor da cadeia de caracteres para uma variável de ambiente do processo atual.
ms.assetid: f59a270f-9bd8-4d17-96e2-cb3c62a31cad
title: Propriedade Installer. Environment
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Environment
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3983eceecd8bc709bea4a094c61c9886c73def3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747544"
---
# <a name="installerenvironment-property"></a><span data-ttu-id="f468e-103">Propriedade Installer. Environment</span><span class="sxs-lookup"><span data-stu-id="f468e-103">Installer.Environment property</span></span>

<span data-ttu-id="f468e-104">A propriedade **Environment** do objeto [**instalador**](installer-object.md) é uma propriedade de leitura/gravação que é o valor da cadeia de caracteres para uma variável de ambiente do processo atual.</span><span class="sxs-lookup"><span data-stu-id="f468e-104">The **Environment** property of the [**Installer**](installer-object.md) object is a read-write property that is the string value for an environment variable of the current process.</span></span>

<span data-ttu-id="f468e-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f468e-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f468e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f468e-106">Syntax</span></span>


```JScript
propVal = Installer.Environment
Installer.Environment = propVal 
```



## <a name="property-value"></a><span data-ttu-id="f468e-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f468e-107">Property value</span></span>

<span data-ttu-id="f468e-108">O nome da variável de ambiente a ser lida ou gravada.</span><span class="sxs-lookup"><span data-stu-id="f468e-108">The name of the environment variable to be read or written.</span></span> <span data-ttu-id="f468e-109">Isso não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f468e-109">This is case-insensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="f468e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="f468e-110">Remarks</span></span>

<span data-ttu-id="f468e-111">Definir uma variável de ambiente com a propriedade de **ambiente** afeta apenas a sessão ativa.</span><span class="sxs-lookup"><span data-stu-id="f468e-111">Setting an environment variable with the **Environment** property only affects the active session.</span></span> <span data-ttu-id="f468e-112">Para fazer alterações persistentes em uma variável de ambiente, use a [tabela de ambiente](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="f468e-112">To make persistent changes to an environment variable, use the [Environment table](environment-table.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f468e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f468e-113">Requirements</span></span>



| <span data-ttu-id="f468e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f468e-114">Requirement</span></span> | <span data-ttu-id="f468e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f468e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f468e-116">Versão</span><span class="sxs-lookup"><span data-stu-id="f468e-116">Version</span></span><br/> | <span data-ttu-id="f468e-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f468e-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f468e-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f468e-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f468e-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="f468e-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f468e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f468e-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="f468e-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f468e-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f468e-122">IID</span><span class="sxs-lookup"><span data-stu-id="f468e-122">IID</span></span><br/>     | <span data-ttu-id="f468e-123">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f468e-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




