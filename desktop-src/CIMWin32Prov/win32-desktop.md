---
description: A \_ classe Win32 DesktopWMI representa as características comuns da área de trabalho de um usuário. As propriedades dessa classe podem ser modificadas pelo usuário para personalizar a área de trabalho.
ms.assetid: 9615a443-7611-4c30-9693-ea71b09b013b
ms.tgt_platform: multiple
title: Classe Win32_Desktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Desktop
- Win32_Desktop.Caption
- Win32_Desktop.Description
- Win32_Desktop.SettingID
- Win32_Desktop.BorderWidth
- Win32_Desktop.CoolSwitch
- Win32_Desktop.CursorBlinkRate
- Win32_Desktop.DragFullWindows
- Win32_Desktop.GridGranularity
- Win32_Desktop.IconSpacing
- Win32_Desktop.IconTitleFaceName
- Win32_Desktop.IconTitleSize
- Win32_Desktop.IconTitleWrap
- Win32_Desktop.Name
- Win32_Desktop.Pattern
- Win32_Desktop.ScreenSaverActive
- Win32_Desktop.ScreenSaverExecutable
- Win32_Desktop.ScreenSaverSecure
- Win32_Desktop.ScreenSaverTimeout
- Win32_Desktop.Wallpaper
- Win32_Desktop.WallpaperStretched
- Win32_Desktop.WallpaperTiled
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1d005104cb663a680bac080b7ff9b6529fd9b7a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826689"
---
# <a name="win32_desktop-class"></a><span data-ttu-id="43b9b-104">\_Classe de área de trabalho Win32</span><span class="sxs-lookup"><span data-stu-id="43b9b-104">Win32\_Desktop class</span></span>

<span data-ttu-id="43b9b-105">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ da área de trabalho do Win32** representa as características comuns da área de trabalho de um usuário.</span><span class="sxs-lookup"><span data-stu-id="43b9b-105">The **Win32\_Desktop**[WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the common characteristics of a user's desktop.</span></span> <span data-ttu-id="43b9b-106">As propriedades dessa classe podem ser modificadas pelo usuário para personalizar a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43b9b-106">The properties of this class can be modified by the user to customize the desktop.</span></span>

<span data-ttu-id="43b9b-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="43b9b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="43b9b-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="43b9b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b9b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43b9b-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Desktop : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BorderWidth;
  boolean CoolSwitch;
  uint32  CursorBlinkRate;
  boolean DragFullWindows;
  uint32  GridGranularity;
  uint32  IconSpacing;
  string  IconTitleFaceName;
  uint32  IconTitleSize;
  boolean IconTitleWrap;
  string  Name;
  string  Pattern;
  boolean ScreenSaverActive;
  string  ScreenSaverExecutable;
  boolean ScreenSaverSecure;
  uint32  ScreenSaverTimeout;
  string  Wallpaper;
  boolean WallpaperStretched;
  boolean WallpaperTiled;
};
```

## <a name="members"></a><span data-ttu-id="43b9b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="43b9b-110">Members</span></span>

<span data-ttu-id="43b9b-111">A classe de **\_ área de trabalho Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43b9b-111">The **Win32\_Desktop** class has these types of members:</span></span>

-   [<span data-ttu-id="43b9b-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43b9b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43b9b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43b9b-113">Properties</span></span>

<span data-ttu-id="43b9b-114">A classe de **\_ área de trabalho Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43b9b-114">The **Win32\_Desktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43b9b-115">**BorderWidth**</span><span class="sxs-lookup"><span data-stu-id="43b9b-115">**BorderWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-116">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43b9b-116">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-118">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \\ \\ WindowMetrics \| BorderWidth ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|BorderWidth")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-119">Largura das bordas em torno de todas as janelas com bordas ajustáveis.</span><span class="sxs-lookup"><span data-stu-id="43b9b-119">Width of the borders around all windows with adjustable borders.</span></span>

<span data-ttu-id="43b9b-120">Exemplo: 3</span><span class="sxs-lookup"><span data-stu-id="43b9b-120">Example: 3</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="43b9b-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-124">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="43b9b-124">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-125">Breve descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="43b9b-125">Short textual description of the current object.</span></span>

<span data-ttu-id="43b9b-126">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="43b9b-126">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-127">**CoolSwitch**</span><span class="sxs-lookup"><span data-stu-id="43b9b-127">**CoolSwitch**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-128">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("painel de controle do Win32Registry \| \\ \\ Desktop \| CoolSwitch")</span><span class="sxs-lookup"><span data-stu-id="43b9b-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CoolSwitch")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-131">A alternância rápida de tarefas está ativada.</span><span class="sxs-lookup"><span data-stu-id="43b9b-131">Fast task switching is turned on.</span></span> <span data-ttu-id="43b9b-132">A alternância rápida de tarefas permite que o usuário alterne entre janelas usando a combinação de teclado **ALT + TAB** .</span><span class="sxs-lookup"><span data-stu-id="43b9b-132">Fast task switching allows the user to switch between windows using the **ALT+TAB** keyboard combination.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-133">**CursorBlinkRate**</span><span class="sxs-lookup"><span data-stu-id="43b9b-133">**CursorBlinkRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-134">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43b9b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-136">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("painel de controle do Win32Registry \| \\ \\ Desktop \| CursorBlinkRate"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("milissegundos")</span><span class="sxs-lookup"><span data-stu-id="43b9b-136">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|CursorBlinkRate"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliseconds")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-137">Período de tempo entre o cursor sucessivo piscar.</span><span class="sxs-lookup"><span data-stu-id="43b9b-137">Length of time between successive cursor blinks.</span></span>

<span data-ttu-id="43b9b-138">Exemplo: 530</span><span class="sxs-lookup"><span data-stu-id="43b9b-138">Example: 530</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="43b9b-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-142">Descrição textual do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="43b9b-142">Textual description of the current object.</span></span>

<span data-ttu-id="43b9b-143">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="43b9b-143">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-144">**DragFullWindows**</span><span class="sxs-lookup"><span data-stu-id="43b9b-144">**DragFullWindows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-145">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-147">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("painel de controle do Win32Registry \| \\ \\ Desktop \| DragFullWindows")</span><span class="sxs-lookup"><span data-stu-id="43b9b-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|DragFullWindows")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-148">O conteúdo de uma janela é mostrado quando um usuário move a janela.</span><span class="sxs-lookup"><span data-stu-id="43b9b-148">Contents of a window are shown when a user moves the window.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-149">**GridGranularity**</span><span class="sxs-lookup"><span data-stu-id="43b9b-149">**GridGranularity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-150">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43b9b-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-152">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("painel de controle do Win32Registry \| \\ \\ Desktop \| GridGranularity"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span><span class="sxs-lookup"><span data-stu-id="43b9b-152">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|Control Panel\\\\Desktop\|GridGranularity"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("8 pixels")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-153">Espaçamento da grade à qual as janelas estão associadas na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43b9b-153">Spacing of the grid that windows are bound to on the desktop.</span></span> <span data-ttu-id="43b9b-154">Isso facilita a organização do Windows.</span><span class="sxs-lookup"><span data-stu-id="43b9b-154">This makes organizing windows easier.</span></span> <span data-ttu-id="43b9b-155">O espaçamento normalmente é suficiente para que o usuário não perceba.</span><span class="sxs-lookup"><span data-stu-id="43b9b-155">The spacing is usually fine enough that the user does not notice it.</span></span>

<span data-ttu-id="43b9b-156">Example: 1</span><span class="sxs-lookup"><span data-stu-id="43b9b-156">Example: 1</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-157">**IconSpacing**</span><span class="sxs-lookup"><span data-stu-id="43b9b-157">**IconSpacing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-158">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43b9b-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-160">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \\ \\ WindowMetrics \| IconSpacing "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" pixels ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconSpacing"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-161">Espaçamento entre ícones.</span><span class="sxs-lookup"><span data-stu-id="43b9b-161">Spacing between icons.</span></span>

<span data-ttu-id="43b9b-162">Exemplo: 75</span><span class="sxs-lookup"><span data-stu-id="43b9b-162">Example: 75</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-163">**IconTitleFaceName**</span><span class="sxs-lookup"><span data-stu-id="43b9b-163">**IconTitleFaceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-166">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \\ \\ WindowMetrics \| IconFont ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconFont")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-167">Fonte usada para os nomes dos ícones.</span><span class="sxs-lookup"><span data-stu-id="43b9b-167">Font used for the names of the icons.</span></span>

<span data-ttu-id="43b9b-168">Exemplo: "MS San Serif"</span><span class="sxs-lookup"><span data-stu-id="43b9b-168">Example: "MS San Serif"</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-169">**IconTitleSize**</span><span class="sxs-lookup"><span data-stu-id="43b9b-169">**IconTitleSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43b9b-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-172">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| fonte e estruturas de texto \| [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) \| lfHeight"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("ponto")</span><span class="sxs-lookup"><span data-stu-id="43b9b-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Font and Text Structures\|[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)\|lfHeight"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("point")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-173">Tamanho da fonte do ícone.</span><span class="sxs-lookup"><span data-stu-id="43b9b-173">Icon font size.</span></span>

<span data-ttu-id="43b9b-174">Exemplo: 9</span><span class="sxs-lookup"><span data-stu-id="43b9b-174">Example: 9</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-175">**IconTitleWrap**</span><span class="sxs-lookup"><span data-stu-id="43b9b-175">**IconTitleWrap**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-176">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-178">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \\ \\ WindowMetrics \| IconTitleWrap ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-178">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\\\\WindowMetrics\|IconTitleWrap")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-179">O texto do título do ícone é quebrado para a próxima linha.</span><span class="sxs-lookup"><span data-stu-id="43b9b-179">Icon's title text wraps to the next line.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-180">**Nome**</span><span class="sxs-lookup"><span data-stu-id="43b9b-180">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-183">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="43b9b-183">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-184">Nome que identifica o perfil da área de trabalho atual.</span><span class="sxs-lookup"><span data-stu-id="43b9b-184">Name that identifies the current desktop profile.</span></span>

<span data-ttu-id="43b9b-185">Exemplo: "MainProf"</span><span class="sxs-lookup"><span data-stu-id="43b9b-185">Example: "MainProf"</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-186">**Padrão**</span><span class="sxs-lookup"><span data-stu-id="43b9b-186">**Pattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-187">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-189">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . Padrão de \\ \\ área de trabalho do painel de controle padrão \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Pattern")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-190">Nome do padrão usado como o plano de fundo da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43b9b-190">Name of the pattern used as the background for the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-191">**ScreenSaverActive**</span><span class="sxs-lookup"><span data-stu-id="43b9b-191">**ScreenSaverActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-192">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-192">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-194">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \| ScreenSaveActive ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-194">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveActive")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-195">A proteção de tela está ativa.</span><span class="sxs-lookup"><span data-stu-id="43b9b-195">Screen saver is active.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-196">**ScreenSaverExecutable**</span><span class="sxs-lookup"><span data-stu-id="43b9b-196">**ScreenSaverExecutable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-199">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\SCRNSAVE.EXE da área de trabalho do painel de controle padrão \\ \\ \| ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|SCRNSAVE.EXE")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-200">Nome do arquivo executável da proteção de tela atual.</span><span class="sxs-lookup"><span data-stu-id="43b9b-200">Name of the current screen saver executable file.</span></span>

<span data-ttu-id="43b9b-201">Exemplo: "LOGON. SCR</span><span class="sxs-lookup"><span data-stu-id="43b9b-201">Example: "LOGON.SCR"</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-202">**ScreenSaverSecure**</span><span class="sxs-lookup"><span data-stu-id="43b9b-202">**ScreenSaverSecure**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-203">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-203">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-205">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \| ScreenSaverIsSecure ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-205">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaverIsSecure")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-206">A senha está habilitada para a proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="43b9b-206">Password is enabled for the screen saver.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-207">**ScreenSaverTimeout**</span><span class="sxs-lookup"><span data-stu-id="43b9b-207">**ScreenSaverTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-208">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43b9b-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-210">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \| ScreenSaveTimeOut "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" segundos ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|ScreenSaveTimeOut"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("seconds")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-211">Quantidade de tempo que o passa antes que a proteção de tela seja iniciada.</span><span class="sxs-lookup"><span data-stu-id="43b9b-211">Amount of time that passes before the screen saver starts.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-212">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="43b9b-212">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-213">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-215">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="43b9b-215">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-216">Identificador pelo qual o objeto atual é conhecido.</span><span class="sxs-lookup"><span data-stu-id="43b9b-216">Identifier by which the current object is known.</span></span>

<span data-ttu-id="43b9b-217">Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="43b9b-217">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-218">**Papel de parede**</span><span class="sxs-lookup"><span data-stu-id="43b9b-218">**Wallpaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-219">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43b9b-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-221">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ \\ \\ Papel de parede da área de trabalho do painel de controle padrão \| ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|Wallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-222">Nome do arquivo para o design do papel de parede no plano de fundo da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43b9b-222">File name for the wallpaper design on the background of the desktop.</span></span>

<span data-ttu-id="43b9b-223">Exemplo: "WINNT.BMP"</span><span class="sxs-lookup"><span data-stu-id="43b9b-223">Example: "WINNT.BMP"</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-224">**WallpaperStretched**</span><span class="sxs-lookup"><span data-stu-id="43b9b-224">**WallpaperStretched**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-225">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-227">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão papel de parede de \\ \\ área de trabalho \| ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-227">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|WallpaperStyle")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-228">O papel de parede é alongado para preencher a tela inteira.</span><span class="sxs-lookup"><span data-stu-id="43b9b-228">Wallpaper is stretched to fill the entire screen.</span></span> <span data-ttu-id="43b9b-229">Microsoft Plus!</span><span class="sxs-lookup"><span data-stu-id="43b9b-229">Microsoft Plus!</span></span> <span data-ttu-id="43b9b-230">deve ser instalado antes que essa opção esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="43b9b-230">must be installed before this option is available.</span></span> <span data-ttu-id="43b9b-231">Se **for false**, o papel de parede manterá suas dimensões originais no plano de fundo da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43b9b-231">If **FALSE**, the wallpaper retains its original dimensions on the desktop background.</span></span>

</dd> <dt>

<span data-ttu-id="43b9b-232">**WallpaperTiled**</span><span class="sxs-lookup"><span data-stu-id="43b9b-232">**WallpaperTiled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43b9b-233">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="43b9b-233">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43b9b-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43b9b-235">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| . \\ \\ Painel de controle padrão \\ \\ Desktop \| TileWallpaper ")</span><span class="sxs-lookup"><span data-stu-id="43b9b-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|.DEFAULT\\\\Control Panel\\\\Desktop\|TileWallpaper")</span></span>
</dt> </dl>

<span data-ttu-id="43b9b-236">O papel de parede é enlado ou centralizado.</span><span class="sxs-lookup"><span data-stu-id="43b9b-236">Wallpaper is tiled or centered.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43b9b-237">Comentários</span><span class="sxs-lookup"><span data-stu-id="43b9b-237">Remarks</span></span>

<span data-ttu-id="43b9b-238">A classe de **\_ área de trabalho Win32** é derivada da [**\_ configuração CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="43b9b-238">The **Win32\_Desktop** class is derived from [**CIM\_Setting**](cim-setting.md).</span></span>

<span data-ttu-id="43b9b-239">O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside.</span><span class="sxs-lookup"><span data-stu-id="43b9b-239">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="43b9b-240">Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio.</span><span class="sxs-lookup"><span data-stu-id="43b9b-240">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="43b9b-241">Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="43b9b-241">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="43b9b-242">Exemplos</span><span class="sxs-lookup"><span data-stu-id="43b9b-242">Examples</span></span>

<span data-ttu-id="43b9b-243">O exemplo de código a seguir descreve como recuperar informações da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="43b9b-243">The following code sample describes how to retrieve desktop information.</span></span>


```PowerShell
$desktops = Get-WmiObject win32_desktop

"This system has {0} desktop objects" -f $desktops.length
Foreach ($dt in $desktops) {
"Desktop {0}" -f $i++
"  BorderWidth           : {0}" -f $dt.BorderWidth 
"  Caption               : {0}" -f $dt.Caption
"  CoolSwitch            : {0}" -f $dt.CoolSwitch
"  CursorBlinkRate       : {0}" -f $dt.CursorBlinkRate
"  Description           : {0}" -f $dt.Description 
"  DragFullWindows       : {0}" -f $dt.DragFullWindows
"  GridGranularity       : {0}" -f $dt.GridGranularity 
"  IconSpacing           : {0}" -f $dt.IconSpacing
"  IconTitleFaceName     : {0}" -f $dt.IconTitleFaceName
"  IconTitleSize         : {0}" -f $dt.IconTitleSize
"  IconTitleWrap         : {0}" -f $dt.conTitleWrap
"  Name                  : {0}" -f $dt.Name
"  Pattern               : {0}" -f $dt.Pattern 
"  ScreenSaverActive     : {0}" -f $dt.ScreenSaverActive
"  ScreenSaverExecutable : {0}" -f $dt.ScreenSaverExecutable
"  ScreenSaverSecure     : {0}" -f $dt.creenSaverSecure
"  ScreenSaverTimeout    : {0}" -f $dt.ScreenSaverTimeout
"  SettingID             : {0}" -f $dt.SettingID
"  Wallpaper             : {0}" -f $dt.Wallpaper
"  WallpaperStretched    : {0}" -f $dt.WallpaperStretched
"  WallpaperTiled        : {0}" -f $dt.WallpaperTiled
""
}
```



## <a name="requirements"></a><span data-ttu-id="43b9b-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43b9b-244">Requirements</span></span>



| <span data-ttu-id="43b9b-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="43b9b-245">Requirement</span></span> | <span data-ttu-id="43b9b-246">Valor</span><span class="sxs-lookup"><span data-stu-id="43b9b-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43b9b-247">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43b9b-247">Minimum supported client</span></span><br/> | <span data-ttu-id="43b9b-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43b9b-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="43b9b-249">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43b9b-249">Minimum supported server</span></span><br/> | <span data-ttu-id="43b9b-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43b9b-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43b9b-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="43b9b-251">Namespace</span></span><br/>                | <span data-ttu-id="43b9b-252">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="43b9b-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="43b9b-253">MOF</span><span class="sxs-lookup"><span data-stu-id="43b9b-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43b9b-254"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43b9b-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="43b9b-255">DLL</span><span class="sxs-lookup"><span data-stu-id="43b9b-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43b9b-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43b9b-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b9b-257">Confira também</span><span class="sxs-lookup"><span data-stu-id="43b9b-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b9b-258">**Configuração de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="43b9b-258">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

<span data-ttu-id="43b9b-259">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43b9b-259">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

