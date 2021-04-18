---
description: O método ViewDialog do objeto UIPreview exibe uma caixa de diálogo de interface do usuário criada no banco de dados atual.
ms.assetid: 5bc935ac-38ca-4a51-a1dc-6879dee97b05
title: Método UIPreview. ViewDialog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewDialog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d9ad3772ced2dba952a3d3b068aaa307d1c06398
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757375"
---
# <a name="uipreviewviewdialog-method"></a><span data-ttu-id="329a8-103">Método UIPreview. ViewDialog</span><span class="sxs-lookup"><span data-stu-id="329a8-103">UIPreview.ViewDialog method</span></span>

<span data-ttu-id="329a8-104">O método **ViewDialog** do objeto [**UIPreview**](uipreview-object.md) exibe uma caixa de diálogo de interface do usuário criada no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="329a8-104">The **ViewDialog** method of the [**UIPreview**](uipreview-object.md) object displays an authored user interface dialog box stored in the current database.</span></span>

## <a name="syntax"></a><span data-ttu-id="329a8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="329a8-105">Syntax</span></span>


```JScript
UIPreview.ViewDialog(
  dialog
)
```



## <a name="parameters"></a><span data-ttu-id="329a8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="329a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="329a8-107">*'*</span><span class="sxs-lookup"><span data-stu-id="329a8-107">*dialog*</span></span> 
</dt> <dd>

<span data-ttu-id="329a8-108">Nome necessário da caixa de diálogo, diferencia maiúsculas de minúsculas e a chave primária da tabela do banco de dados de diálogo.</span><span class="sxs-lookup"><span data-stu-id="329a8-108">Required name of the dialog box, case-sensitive, and the primary key of the Dialog database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="329a8-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="329a8-109">Return value</span></span>

<span data-ttu-id="329a8-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="329a8-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="329a8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="329a8-111">Requirements</span></span>



| <span data-ttu-id="329a8-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="329a8-112">Requirement</span></span> | <span data-ttu-id="329a8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="329a8-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="329a8-114">Versão</span><span class="sxs-lookup"><span data-stu-id="329a8-114">Version</span></span><br/> | <span data-ttu-id="329a8-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="329a8-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="329a8-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="329a8-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="329a8-117">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="329a8-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="329a8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="329a8-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="329a8-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="329a8-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="329a8-120">IID</span><span class="sxs-lookup"><span data-stu-id="329a8-120">IID</span></span><br/>     | <span data-ttu-id="329a8-121">IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="329a8-121">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




