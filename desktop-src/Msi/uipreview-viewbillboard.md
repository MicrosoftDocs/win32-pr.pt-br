---
description: O método ViewBillboard do objeto UIPreview exibe um mural criado usando o controle de host na caixa de diálogo exibida no momento.
ms.assetid: c51c1a5b-af53-47a8-9281-e790efadcfc4
title: Método UIPreview. ViewBillboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview.ViewBillboard
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9cf1c6ee2a47fdb246fcc847627bb63432b8a67f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750591"
---
# <a name="uipreviewviewbillboard-method"></a><span data-ttu-id="e5050-103">Método UIPreview. ViewBillboard</span><span class="sxs-lookup"><span data-stu-id="e5050-103">UIPreview.ViewBillboard method</span></span>

<span data-ttu-id="e5050-104">O método **ViewBillboard** do objeto [**UIPreview**](uipreview-object.md) exibe um mural criado usando o controle de host na caixa de diálogo exibida no momento.</span><span class="sxs-lookup"><span data-stu-id="e5050-104">The **ViewBillboard** method of the [**UIPreview**](uipreview-object.md) object displays an authored billboard using the host control in the currently displayed dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5050-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5050-105">Syntax</span></span>


```JScript
UIPreview.ViewBillboard(
  control,
  billboard
)
```



## <a name="parameters"></a><span data-ttu-id="e5050-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5050-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5050-107">*control*</span><span class="sxs-lookup"><span data-stu-id="e5050-107">*control*</span></span> 
</dt> <dd>

<span data-ttu-id="e5050-108">Nome necessário do controle que hospeda o mural, diferencia maiúsculas de minúsculas, juntamente com a caixa de diálogo e as chaves primárias da tabela do banco de dados de controle.</span><span class="sxs-lookup"><span data-stu-id="e5050-108">Required name of the control hosting the billboard, case-sensitive, along with the dialog box, and the primary keys of the Control database table.</span></span>

</dd> <dt>

<span data-ttu-id="e5050-109">*mensagem*</span><span class="sxs-lookup"><span data-stu-id="e5050-109">*billboard*</span></span> 
</dt> <dd>

<span data-ttu-id="e5050-110">Nome necessário do mural a ser exibido usando o controle especificado e a caixa de diálogo atual e a chave primária da tabela do banco de dados do mural.</span><span class="sxs-lookup"><span data-stu-id="e5050-110">Required name of the billboard to display using the specified control and current dialog box, and the primary key of the Billboard database table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5050-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e5050-111">Return value</span></span>

<span data-ttu-id="e5050-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e5050-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5050-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5050-113">Requirements</span></span>



| <span data-ttu-id="e5050-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5050-114">Requirement</span></span> | <span data-ttu-id="e5050-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e5050-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5050-116">Versão</span><span class="sxs-lookup"><span data-stu-id="e5050-116">Version</span></span><br/> | <span data-ttu-id="e5050-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e5050-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e5050-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e5050-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e5050-119">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5050-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e5050-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e5050-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5050-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5050-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e5050-122">IID</span><span class="sxs-lookup"><span data-stu-id="e5050-122">IID</span></span><br/>     | <span data-ttu-id="e5050-123">IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e5050-123">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




