---
description: O método EnableUIPreview do objeto de banco de dados facilita a criação de caixas de diálogo e de mural, fornecendo o suporte necessário para exibir caixas de diálogo de interface do usuário armazenadas no banco de dados do instalador.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Método Database. EnableUIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756734"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="3e975-103">Método Database. EnableUIPreview</span><span class="sxs-lookup"><span data-stu-id="3e975-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="3e975-104">O método **EnableUIPreview** do objeto de [**banco de dados**](database-object.md) facilita a criação de caixas de diálogo e de mural, fornecendo o suporte necessário para exibir caixas de diálogo de interface do usuário armazenadas no banco de dados do instalador.</span><span class="sxs-lookup"><span data-stu-id="3e975-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="3e975-105">O método inicia o modo de visualização retornando um objeto de **banco de dados** de visualização.</span><span class="sxs-lookup"><span data-stu-id="3e975-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="3e975-106">O modo de visualização termina quando o objeto de visualização é liberado.</span><span class="sxs-lookup"><span data-stu-id="3e975-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e975-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e975-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="3e975-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e975-108">Parameters</span></span>

<span data-ttu-id="3e975-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3e975-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e975-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e975-110">Return value</span></span>

<span data-ttu-id="3e975-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3e975-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e975-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e975-112">Requirements</span></span>



| <span data-ttu-id="3e975-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e975-113">Requirement</span></span> | <span data-ttu-id="3e975-114">Valor</span><span class="sxs-lookup"><span data-stu-id="3e975-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e975-115">Versão</span><span class="sxs-lookup"><span data-stu-id="3e975-115">Version</span></span><br/> | <span data-ttu-id="3e975-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3e975-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3e975-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3e975-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3e975-118">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="3e975-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3e975-119">DLL</span><span class="sxs-lookup"><span data-stu-id="3e975-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="3e975-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e975-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3e975-121">IID</span><span class="sxs-lookup"><span data-stu-id="3e975-121">IID</span></span><br/>     | <span data-ttu-id="3e975-122">IID \_ IDatabase é definido como 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3e975-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




