---
description: A tabela MsiShortcutProperty permite que o instalador de janela defina propriedades para atalhos que também são objetos de shell do Windows.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Tabela MsiShortcutProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506109"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="d66cd-103">Tabela MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="d66cd-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="d66cd-104">A tabela MsiShortcutProperty permite que o instalador de janela defina propriedades para atalhos que também são objetos de [shell do Windows](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d66cd-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="d66cd-105">A partir do Windows Vista e do Windows Server 2008, o Shell do Windows fornece uma interface IPropertyStore para objetos do Shell, como atalhos.</span><span class="sxs-lookup"><span data-stu-id="d66cd-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="d66cd-106">Um pacote Windows Installer 5,0 em execução no Windows Server 2008 R2 ou no Windows 7 pode definir essas propriedades quando o atalho é instalado.</span><span class="sxs-lookup"><span data-stu-id="d66cd-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="d66cd-107">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="d66cd-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="d66cd-108">Esta tabela está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="d66cd-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="d66cd-109">A tabela MsiShortcutProperty tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d66cd-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="d66cd-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="d66cd-110">Column</span></span>              | <span data-ttu-id="d66cd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d66cd-111">Type</span></span>                         | <span data-ttu-id="d66cd-112">Chave</span><span class="sxs-lookup"><span data-stu-id="d66cd-112">Key</span></span> | <span data-ttu-id="d66cd-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="d66cd-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="d66cd-114">MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="d66cd-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="d66cd-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="d66cd-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="d66cd-116">S</span><span class="sxs-lookup"><span data-stu-id="d66cd-116">Y</span></span>   | <span data-ttu-id="d66cd-117">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-117">N</span></span>        |
| <span data-ttu-id="d66cd-118">Atalho\_</span><span class="sxs-lookup"><span data-stu-id="d66cd-118">Shortcut\_</span></span>          | [<span data-ttu-id="d66cd-119">Identificador</span><span class="sxs-lookup"><span data-stu-id="d66cd-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="d66cd-120">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-120">N</span></span>   | <span data-ttu-id="d66cd-121">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-121">N</span></span>        |
| <span data-ttu-id="d66cd-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="d66cd-122">PropertyKey</span></span>         | [<span data-ttu-id="d66cd-123">Binário</span><span class="sxs-lookup"><span data-stu-id="d66cd-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d66cd-124">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-124">N</span></span>   | <span data-ttu-id="d66cd-125">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-125">N</span></span>        |
| <span data-ttu-id="d66cd-126">PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="d66cd-126">PropVariantValue</span></span>    | [<span data-ttu-id="d66cd-127">Binário</span><span class="sxs-lookup"><span data-stu-id="d66cd-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="d66cd-128">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-128">N</span></span>   | <span data-ttu-id="d66cd-129">N</span><span class="sxs-lookup"><span data-stu-id="d66cd-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d66cd-130">Colunas</span><span class="sxs-lookup"><span data-stu-id="d66cd-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d66cd-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="d66cd-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="d66cd-132">Identificador exclusivo desta linha da tabela MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="d66cd-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="d66cd-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Atalho\_</span><span class="sxs-lookup"><span data-stu-id="d66cd-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="d66cd-134">Uma chave na tabela de [atalho](shortcut-table.md) que identifica o atalho com uma propriedade definida.</span><span class="sxs-lookup"><span data-stu-id="d66cd-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="d66cd-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="d66cd-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="d66cd-136">Um valor de cadeia de caracteres que fornece informações para a estrutura [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) .</span><span class="sxs-lookup"><span data-stu-id="d66cd-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="d66cd-137">As informações neste campo devem se referir ao nome canônico de uma propriedade registrada com o sistema de propriedades do Windows.</span><span class="sxs-lookup"><span data-stu-id="d66cd-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="d66cd-138">Para obter mais informações sobre o sistema de propriedades do Windows, consulte [visão geral do sistema de propriedades](/previous-versions//bb776909(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d66cd-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="d66cd-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="d66cd-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="d66cd-140">Um valor de cadeia de caracteres que fornece informações para a estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d66cd-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="d66cd-141">Várias propriedades podem ser definidas em um atalho.</span><span class="sxs-lookup"><span data-stu-id="d66cd-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="d66cd-142">Se a mesma propriedade for definida várias vezes no mesmo atalho, o valor será definido em uma ordem não especificada.</span><span class="sxs-lookup"><span data-stu-id="d66cd-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="d66cd-143">Windows Installer pode definir propriedades de atalho somente quando o atalho é instalado ou reinstalado.</span><span class="sxs-lookup"><span data-stu-id="d66cd-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="d66cd-144">Um patch que não reinstala um atalho que já foi instalado não atualiza as propriedades do atalho.</span><span class="sxs-lookup"><span data-stu-id="d66cd-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="d66cd-145">Um patch pode atualizar as propriedades, incluindo uma tabela de [atalho](shortcut-table.md) no pacote de patch e reinstalando o atalho.</span><span class="sxs-lookup"><span data-stu-id="d66cd-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="d66cd-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="d66cd-146">Remarks</span></span>

<span data-ttu-id="d66cd-147">[Windows Installer mensagem de erro](windows-installer-error-messages.md) 1946 é retornada como um aviso e a instalação continuará, se Windows Installer não puder definir uma propriedade de atalho especificada na tabela MsiShortcutProperty.</span><span class="sxs-lookup"><span data-stu-id="d66cd-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="d66cd-148">Validação</span><span class="sxs-lookup"><span data-stu-id="d66cd-148">Validation</span></span>

<dl>

[<span data-ttu-id="d66cd-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="d66cd-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
