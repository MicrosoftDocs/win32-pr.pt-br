---
description: Para cada senha que deve ser inserida pelo usuário, adicione um controle de edição em uma caixa de diálogo que armazena o valor da senha em uma propriedade.
ms.assetid: aa4ff8b8-cbbb-4b18-83b3-279e52d9f6d3
title: Criando a interface do usuário para entrada de senha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37cd7bb9531cbf63a443011656f200717dc0214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753454"
---
# <a name="authoring-the-user-interface-for-password-input"></a><span data-ttu-id="b4a85-103">Criando a interface do usuário para entrada de senha</span><span class="sxs-lookup"><span data-stu-id="b4a85-103">Authoring the User Interface for Password Input</span></span>

<span data-ttu-id="b4a85-104">Para cada senha que deve ser inserida pelo usuário, adicione um controle de edição em uma caixa de diálogo que armazena o valor da senha em uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="b4a85-104">For each password that must be entered by the user, add an edit control on a dialog that stores the value of the password into a property.</span></span> <span data-ttu-id="b4a85-105">Esse [controle de edição](edit-control.md) deve ter o [atributo de controle de senha](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="b4a85-105">This [edit control](edit-control.md) should have the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="b4a85-106">Isso especifica que a propriedade inserida é uma senha e impede que o instalador grave a propriedade no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="b4a85-106">This specifies that the property entered is a password and prevents the installer from writing the property to the log file.</span></span>

<span data-ttu-id="b4a85-107">Os [atributos de controle](control-attributes.md) para o controle de edição de senha são MsidbControlAttributesVisible, MsidbControlAttributesEnabled e msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span><span class="sxs-lookup"><span data-stu-id="b4a85-107">The [control attributes](control-attributes.md) for the password edit control are msidbControlAttributesVisible, msidbControlAttributesEnabled, and msidbControlAttributesPasswordInput (1 + 2 + 2097152).</span></span> <span data-ttu-id="b4a85-108">O X, Y, largura, altura e controle, \_ em seguida, dependem do layout do controle na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b4a85-108">The X, Y, Width, Height, and Control\_Next depend on the layout of the control on the dialog.</span></span>

[<span data-ttu-id="b4a85-109">Tabela de controle</span><span class="sxs-lookup"><span data-stu-id="b4a85-109">Control Table</span></span>](control-table.md)



| <span data-ttu-id="b4a85-110">caixa de diálogo\_</span><span class="sxs-lookup"><span data-stu-id="b4a85-110">Dialog\_</span></span> | <span data-ttu-id="b4a85-111">controle\_</span><span class="sxs-lookup"><span data-stu-id="b4a85-111">Control\_</span></span>            | <span data-ttu-id="b4a85-112">Type</span><span class="sxs-lookup"><span data-stu-id="b4a85-112">Type</span></span> | <span data-ttu-id="b4a85-113">X</span><span class="sxs-lookup"><span data-stu-id="b4a85-113">X</span></span>   | <span data-ttu-id="b4a85-114">S</span><span class="sxs-lookup"><span data-stu-id="b4a85-114">Y</span></span>   | <span data-ttu-id="b4a85-115">Largura</span><span class="sxs-lookup"><span data-stu-id="b4a85-115">Width</span></span> | <span data-ttu-id="b4a85-116">Altura</span><span class="sxs-lookup"><span data-stu-id="b4a85-116">Height</span></span> | <span data-ttu-id="b4a85-117">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4a85-117">Attributes</span></span> | <span data-ttu-id="b4a85-118">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b4a85-118">Property</span></span>         | <span data-ttu-id="b4a85-119">Texto</span><span class="sxs-lookup"><span data-stu-id="b4a85-119">Text</span></span> | <span data-ttu-id="b4a85-120">\_Próximo controle</span><span class="sxs-lookup"><span data-stu-id="b4a85-120">Control\_Next</span></span> | <span data-ttu-id="b4a85-121">Ajuda</span><span class="sxs-lookup"><span data-stu-id="b4a85-121">Help</span></span> |
|----------|----------------------|------|-----|-----|-------|--------|------------|------------------|------|---------------|------|
| <span data-ttu-id="b4a85-122">MyDialog</span><span class="sxs-lookup"><span data-stu-id="b4a85-122">MyDialog</span></span> | <span data-ttu-id="b4a85-123">TestUserPasswordEdit</span><span class="sxs-lookup"><span data-stu-id="b4a85-123">TestUserPasswordEdit</span></span> | <span data-ttu-id="b4a85-124">Editar</span><span class="sxs-lookup"><span data-stu-id="b4a85-124">Edit</span></span> | <span data-ttu-id="b4a85-125">25</span><span class="sxs-lookup"><span data-stu-id="b4a85-125">25</span></span>  | <span data-ttu-id="b4a85-126">120</span><span class="sxs-lookup"><span data-stu-id="b4a85-126">120</span></span> | <span data-ttu-id="b4a85-127">300</span><span class="sxs-lookup"><span data-stu-id="b4a85-127">300</span></span>   | <span data-ttu-id="b4a85-128">20</span><span class="sxs-lookup"><span data-stu-id="b4a85-128">20</span></span>     | <span data-ttu-id="b4a85-129">2097155</span><span class="sxs-lookup"><span data-stu-id="b4a85-129">2097155</span></span>    | <span data-ttu-id="b4a85-130">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="b4a85-130">TESTUSERPASSWORD</span></span> |      | <span data-ttu-id="b4a85-131">Cancelar</span><span class="sxs-lookup"><span data-stu-id="b4a85-131">Cancel</span></span>        |      |



 

<span data-ttu-id="b4a85-132">Continue a [proteger a instalação](securing-the-installation.md).</span><span class="sxs-lookup"><span data-stu-id="b4a85-132">Continue to [Securing the installation](securing-the-installation.md).</span></span>

 

 



