---
description: O objeto UIPreview é usado para exibir caixas de diálogo de interface do usuário e murals durante a criação. Esse objeto é criado pelo método EnableUIPreview do objeto Database.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Objeto UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754339"
---
# <a name="uipreview-object"></a><span data-ttu-id="08f2b-104">Objeto UIPreview</span><span class="sxs-lookup"><span data-stu-id="08f2b-104">UIPreview object</span></span>

<span data-ttu-id="08f2b-105">O objeto **UIPreview** é usado para exibir caixas de diálogo de interface do usuário e murals durante a criação.</span><span class="sxs-lookup"><span data-stu-id="08f2b-105">The **UIPreview** object is used to view user interface dialog boxes and billboards during authoring.</span></span> <span data-ttu-id="08f2b-106">Esse objeto é criado pelo método [**EnableUIPreview**](database-enableuipreview.md) do objeto [**Database**](database-object.md) .</span><span class="sxs-lookup"><span data-stu-id="08f2b-106">This object is created by the [**EnableUIPreview**](database-enableuipreview.md) method of the [**Database**](database-object.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="08f2b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="08f2b-107">Members</span></span>

<span data-ttu-id="08f2b-108">O objeto **UIPreview** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="08f2b-108">The **UIPreview** object has these types of members:</span></span>

-   [<span data-ttu-id="08f2b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="08f2b-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="08f2b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08f2b-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="08f2b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="08f2b-111">Methods</span></span>

<span data-ttu-id="08f2b-112">O objeto **UIPreview** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="08f2b-112">The **UIPreview** object has these methods.</span></span>



| <span data-ttu-id="08f2b-113">Método</span><span class="sxs-lookup"><span data-stu-id="08f2b-113">Method</span></span>                                           | <span data-ttu-id="08f2b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="08f2b-114">Description</span></span>                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08f2b-115">**ViewBillboard**</span><span class="sxs-lookup"><span data-stu-id="08f2b-115">**ViewBillboard**</span></span>](uipreview-viewbillboard.md) | <span data-ttu-id="08f2b-116">Exibe um mural criado usando o controle de host na caixa de diálogo exibida no momento.</span><span class="sxs-lookup"><span data-stu-id="08f2b-116">Displays an authored billboard using the host control in the currently displayed dialog box.</span></span><br/> |
| [<span data-ttu-id="08f2b-117">**ViewDialog**</span><span class="sxs-lookup"><span data-stu-id="08f2b-117">**ViewDialog**</span></span>](uipreview-viewdialog.md)       | <span data-ttu-id="08f2b-118">Exibe uma caixa de diálogo de IU criada armazenada no banco de dados atual.</span><span class="sxs-lookup"><span data-stu-id="08f2b-118">Displays an authored UI dialog box stored in the current database.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="08f2b-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="08f2b-119">Properties</span></span>

<span data-ttu-id="08f2b-120">O objeto **UIPreview** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="08f2b-120">The **UIPreview** object has these properties.</span></span>



| <span data-ttu-id="08f2b-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="08f2b-121">Property</span></span>                                          | <span data-ttu-id="08f2b-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="08f2b-122">Access type</span></span>           | <span data-ttu-id="08f2b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="08f2b-123">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="08f2b-124">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="08f2b-124">**Property**</span></span>](uipreview-property.md)<br/> | <span data-ttu-id="08f2b-125">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="08f2b-125">Read/write</span></span><br/> | <span data-ttu-id="08f2b-126">Representa o valor da cadeia de caracteres de uma propriedade nomeada do instalador ou, se prefixado com um sinal de porcentagem (%), o valor de uma variável de ambiente do sistema para o processo atual.</span><span class="sxs-lookup"><span data-stu-id="08f2b-126">Represents the string value of a named installer property or, if prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="08f2b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08f2b-127">Requirements</span></span>



| <span data-ttu-id="08f2b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="08f2b-128">Requirement</span></span> | <span data-ttu-id="08f2b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="08f2b-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08f2b-130">Versão</span><span class="sxs-lookup"><span data-stu-id="08f2b-130">Version</span></span><br/> | <span data-ttu-id="08f2b-131">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="08f2b-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="08f2b-132">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08f2b-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="08f2b-133">Windows Installer no Windows Server 2003 ou no Windows XP</span><span class="sxs-lookup"><span data-stu-id="08f2b-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="08f2b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="08f2b-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="08f2b-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08f2b-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="08f2b-136">IID</span><span class="sxs-lookup"><span data-stu-id="08f2b-136">IID</span></span><br/>     | <span data-ttu-id="08f2b-137">IID \_ IUIPreview é definido como 000C109A-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="08f2b-137">IID\_IUIPreview is defined as 000C109A-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="08f2b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="08f2b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08f2b-139">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="08f2b-139">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




