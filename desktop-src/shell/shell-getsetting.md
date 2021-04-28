---
description: Método Shell. Configuration – recupera uma configuração de shell global.
ms.assetid: 3E8C7C6A-5696-4756-B4BF-902FA2420AE9
title: Método Shell. Configuration (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSetting
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: dc8fe6277208808ad5f5b182f3eee416daf4a5d0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083734"
---
# <a name="shellgetsetting-method"></a><span data-ttu-id="ff1ca-103">Método Shell. Configuration</span><span class="sxs-lookup"><span data-stu-id="ff1ca-103">Shell.GetSetting method</span></span>

<span data-ttu-id="ff1ca-104">Recupera uma configuração de shell global.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-104">Retrieves a global Shell setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff1ca-105">Syntax</span></span>


```JScript
retVal = Shell.GetSetting(
  lSetting
)
```


```VB

Shell.GetSetting( _
  ByVal lSetting As long _
) As VARIANT_BOOL
```





## <a name="parameters"></a><span data-ttu-id="ff1ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff1ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff1ca-107">*lSetting* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff1ca-107">*lSetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff1ca-108">Tipo: **longo**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-108">Type: **long**</span></span>

<span data-ttu-id="ff1ca-109">Um valor que especifica a configuração de shell atual a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-109">A value that specifies the current Shell setting to retrieve.</span></span> <span data-ttu-id="ff1ca-110">Apenas uma configuração pode ser recuperada em cada chamada.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-110">Only one setting can be retrieved in each call.</span></span> <span data-ttu-id="ff1ca-111">Os valores a seguir são reconhecidos por este método.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-111">The following values are recognized by this method.</span></span>

<dt>

<span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>

<span data-ttu-id="ff1ca-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF \_ AUTOCHECKSELECT** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-112"><span id="SSF_AUTOCHECKSELECT"></span><span id="ssf_autocheckselect"></span>**SSF\_AUTOCHECKSELECT** (0x00800000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-113">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-113">**Windows Vista and later**.</span></span> <span data-ttu-id="ff1ca-114">O estado da opção **usar caixas de seleção para selecionar itens** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-114">The state of the **Use check boxes to select items** option.</span></span> <span data-ttu-id="ff1ca-115">Essa opção é habilitada automaticamente quando o sistema tem um dispositivo de entrada de caneta configurado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-115">This option is enabled automatically when the system has a pen input device configured.</span></span>

</dd> <dt>

<span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>

<span data-ttu-id="ff1ca-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-116"><span id="SSF_DESKTOPHTML"></span><span id="ssf_desktophtml"></span>**SSF\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-117">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-117">Not used.</span></span>

</dd> <dt>

<span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>

<span data-ttu-id="ff1ca-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF \_ DONTPRETTYPATH** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-118"><span id="SSF_DONTPRETTYPATH"></span><span id="ssf_dontprettypath"></span>**SSF\_DONTPRETTYPATH** (0x00000800)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-119">O estado da opção **permitir todos os nomes em maiúsculas** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-119">The state of the **Allow all uppercase names** option.</span></span> <span data-ttu-id="ff1ca-120">A partir do Windows Vista, essa opção de pasta não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-120">As of Windows Vista, this folder option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>

<span data-ttu-id="ff1ca-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-121"><span id="SSF_DOUBLECLICKINWEBVIEW"></span><span id="ssf_doubleclickinwebview"></span>**SSF\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-122">O estado do **clique duplo para abrir uma opção de item (clique único para selecionar)** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-122">The state of the **Double-click to open an item (single-click to select)** option.</span></span>

</dd> <dt>

<span id="SSF_FILTER"></span><span id="ssf_filter"></span>

<span data-ttu-id="ff1ca-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF \_ FILTER** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-123"><span id="SSF_FILTER"></span><span id="ssf_filter"></span>**SSF\_FILTER** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-124">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>

<span data-ttu-id="ff1ca-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF \_ HIDDENFILEEXTS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-125"><span id="SSF_HIDDENFILEEXTS"></span><span id="ssf_hiddenfileexts"></span>**SSF\_HIDDENFILEEXTS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-126">Not used.</span></span>

</dd> <dt>

<span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>

<span data-ttu-id="ff1ca-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF \_ HIDEICONS** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-127"><span id="SSF_HIDEICONS"></span><span id="ssf_hideicons"></span>**SSF\_HIDEICONS** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-128">O estado do ícone de exibição no modo de exibição de lista do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-128">The state of icon display in the Windows Explorer list view.</span></span> <span data-ttu-id="ff1ca-129">Se essa opção estiver ativa, nenhum ícone será exibido na exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-129">If this option is active, no icons are displayed in the list view.</span></span>

</dd> <dt>

<span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>

<span data-ttu-id="ff1ca-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF \_ ICONSONLY** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-130"><span id="SSF_ICONSONLY"></span><span id="ssf_iconsonly"></span>**SSF\_ICONSONLY** (0x01000000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-131">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-131">**Windows Vista and later**.</span></span> <span data-ttu-id="ff1ca-132">O estado do nome de exibição é exibido no modo de exibição de lista do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-132">The state of display name display in the Windows Explorer list view.</span></span> <span data-ttu-id="ff1ca-133">Se essa opção estiver ativa, os ícones serão exibidos no modo de exibição de lista, mas os nomes de exibição não serão.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-133">If this option is active, icons are displayed in the list view, but display names are not.</span></span>

</dd> <dt>

<span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>

<span data-ttu-id="ff1ca-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF \_ MAPNETDRVBUTTON** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-134"><span id="SSF_MAPNETDRVBUTTON"></span><span id="ssf_mapnetdrvbutton"></span>**SSF\_MAPNETDRVBUTTON** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-135">O estado do **botão Mostrar unidade de rede do mapa na opção da barra de ferramentas** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-135">The state of the **Show map network drive button in toolbar** option.</span></span> <span data-ttu-id="ff1ca-136">A partir do Windows Vista, essa opção não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-136">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>

<span data-ttu-id="ff1ca-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF \_ NOCONFIRMRECYCLE** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-137"><span id="SSF_NOCONFIRMRECYCLE"></span><span id="ssf_noconfirmrecycle"></span>**SSF\_NOCONFIRMRECYCLE** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-138">O estado da opção da caixa de **diálogo de confirmação de exclusão de exibição** da lixeira.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-138">The state of the Recycle Bin's **Display delete confirmation dialog** option.</span></span>

</dd> <dt>

<span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>

<span data-ttu-id="ff1ca-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF \_ NONETCRAWLING** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-139"><span id="SSF_NONETCRAWLING"></span><span id="ssf_nonetcrawling"></span>**SSF\_NONETCRAWLING** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-140">O estado da opção **Pesquisar automaticamente pastas e impressoras de rede** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-140">The state of the **Automatically search for network folders and printers** option.</span></span> <span data-ttu-id="ff1ca-141">A partir do Windows Vista, essa opção não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-141">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>

<span data-ttu-id="ff1ca-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF \_ SEPPROCESS** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-142"><span id="SSF_SEPPROCESS"></span><span id="ssf_sepprocess"></span>**SSF\_SEPPROCESS** (0x00080000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-143">O estado das **janelas de pasta de inicialização em uma opção de processo separada** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-143">The state of the **Launch folder windows in a separate process** option.</span></span>

</dd> <dt>

<span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>

<span data-ttu-id="ff1ca-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF \_ SERVERADMINUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-144"><span id="SSF_SERVERADMINUI"></span><span id="ssf_serveradminui"></span>**SSF\_SERVERADMINUI** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-145">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-145">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>

<span data-ttu-id="ff1ca-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-146"><span id="SSF_SHOWALLOBJECTS"></span><span id="ssf_showallobjects"></span>**SSF\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-147">O estado da opção **arquivos e pastas ocultos** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-147">The state of the **Hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>

<span data-ttu-id="ff1ca-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF \_ SHOWATTRIBCOL** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-148"><span id="SSF_SHOWATTRIBCOL"></span><span id="ssf_showattribcol"></span>**SSF\_SHOWATTRIBCOL** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-149">O estado da opção **Mostrar atributos de arquivo no modo de exibição de detalhes** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-149">The state of the **Show File Attributes in Detail View** option.</span></span> <span data-ttu-id="ff1ca-150">A partir do Windows Vista, essa opção não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-150">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>

<span data-ttu-id="ff1ca-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-151"><span id="SSF_SHOWCOMPCOLOR"></span><span id="ssf_showcompcolor"></span>**SSF\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-152">O estado da opção **Mostrar arquivos NTFS criptografados ou compactados na cor** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-152">The state of the **Show encrypted or compressed NTFS files in color** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>

<span data-ttu-id="ff1ca-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF \_ Conextensões** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-153"><span id="SSF_SHOWEXTENSIONS"></span><span id="ssf_showextensions"></span>**SSF\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-154">O estado da opção **Ocultar extensões para tipos de arquivo conhecidos** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-154">The state of the **Hide extensions for known file types** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>

<span data-ttu-id="ff1ca-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF \_ SHOWINFOTIP** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-155"><span id="SSF_SHOWINFOTIP"></span><span id="ssf_showinfotip"></span>**SSF\_SHOWINFOTIP** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-156">O estado da opção **mostrar descrição pop-up para itens da pasta e da área de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-156">The state of the **Show pop-up description for folder and desktop items** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>

<span data-ttu-id="ff1ca-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF \_ 0x00400000 (nastartpage** )</span><span class="sxs-lookup"><span data-stu-id="ff1ca-157"><span id="SSF_SHOWSTARTPAGE"></span><span id="ssf_showstartpage"></span>**SSF\_SHOWSTARTPAGE** (0x00400000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-158">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-158">Not used.</span></span>

</dd> <dt>

<span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>

<span data-ttu-id="ff1ca-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF \_ SHOWSUPERHIDDEN** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-159"><span id="SSF_SHOWSUPERHIDDEN"></span><span id="ssf_showsuperhidden"></span>**SSF\_SHOWSUPERHIDDEN** (0x00040000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-160">O estado da opção **ocultar arquivos protegidos do sistema operacional** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-160">The state of the **Hide protected operating system files** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>

<span data-ttu-id="ff1ca-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-161"><span id="SSF_SHOWSYSFILES"></span><span id="ssf_showsysfiles"></span>**SSF\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-162">O estado da opção **arquivos e pastas ocultos** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-162">The state of the **Hidden files and folders** option.</span></span> <span data-ttu-id="ff1ca-163">No Windows Vista e posterior, isso é equivalente a SSF \_ SHOWALLOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-163">In Windows Vista and later, this is equivalent to SSF\_SHOWALLOBJECTS.</span></span> <span data-ttu-id="ff1ca-164">Em versões do Windows anteriores ao Windows Vista, esse valor se referia ao estado da opção **não mostrar arquivos e pastas ocultos** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-164">In versions of Windows before Windows Vista, this value referred to the state of the **Do not show hidden files and folders** option.</span></span>

</dd> <dt>

<span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>

<span data-ttu-id="ff1ca-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF \_ SHOWTYPEOVERLAY** (0x02000000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-165"><span id="SSF_SHOWTYPEOVERLAY"></span><span id="ssf_showtypeoverlay"></span>**SSF\_SHOWTYPEOVERLAY** (0x02000000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-166">**Windows Vista e posterior**.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-166">**Windows Vista and later**.</span></span> <span data-ttu-id="ff1ca-167">O estado do **ícone do arquivo de exibição na opção de miniaturas** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-167">The state of the **Display file icon on thumbnails** option.</span></span> <span data-ttu-id="ff1ca-168">Se essa opção estiver ativa, uma sobreposição de tipo de arquivo será aplicada quando um arquivo fornecer uma representação em miniatura.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-168">If this option is active, a file type overlay is applied when a file supplies a thumbnail representation.</span></span>

</dd> <dt>

<span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>

<span data-ttu-id="ff1ca-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF \_ SORTCOLUMNS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-169"><span id="SSF_SORTCOLUMNS"></span><span id="ssf_sortcolumns"></span>**SSF\_SORTCOLUMNS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-170">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-170">Not used.</span></span>

</dd> <dt>

<span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>

<span data-ttu-id="ff1ca-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF \_ STARTPANELON** (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-171"><span id="SSF_STARTPANELON"></span><span id="ssf_startpanelon"></span>**SSF\_STARTPANELON** (0x00200000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-172">O estado da opção de exibição do Windows XP, que seleciona entre o estilo do Windows XP e o estilo clássico.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-172">The state of the Windows XP display option, which selects between the Windows XP style and the classic style.</span></span> <span data-ttu-id="ff1ca-173">A partir do Windows Vista, essa opção não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-173">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>

<span data-ttu-id="ff1ca-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF \_ WebView** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-174"><span id="SSF_WEBVIEW"></span><span id="ssf_webview"></span>**SSF\_WEBVIEW** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-175">O estado da **exibição como uma opção de exibição da Web**.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-175">The state of the **Display as a web view option**.</span></span> <span data-ttu-id="ff1ca-176">A partir do Windows Vista, essa opção não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-176">As of Windows Vista, this option is no longer available.</span></span>

</dd> <dt>

<span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>

<span data-ttu-id="ff1ca-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF \_ WIN95CLASSIC** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="ff1ca-177"><span id="SSF_WIN95CLASSIC"></span><span id="ssf_win95classic"></span>**SSF\_WIN95CLASSIC** (0x00000400)</span></span>


</dt> <dd>

<span data-ttu-id="ff1ca-178">O estado da opção de **estilo clássico** .</span><span class="sxs-lookup"><span data-stu-id="ff1ca-178">The state of the **Classic Style** option.</span></span> <span data-ttu-id="ff1ca-179">A partir do Windows Vista, essa opção não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-179">As of Windows Vista, this option is no longer available.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff1ca-180">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ff1ca-180">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="ff1ca-181">JScript</span><span class="sxs-lookup"><span data-stu-id="ff1ca-181">JScript</span></span>

<span data-ttu-id="ff1ca-182">Tipo: **\_ booliano \* de variante**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-182">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="ff1ca-183">Definir como **true** se a configuração existir; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-183">Set to **true** if the setting exists; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="ff1ca-184">VB</span><span class="sxs-lookup"><span data-stu-id="ff1ca-184">VB</span></span>

<span data-ttu-id="ff1ca-185">Tipo: **\_ booliano \* de variante**</span><span class="sxs-lookup"><span data-stu-id="ff1ca-185">Type: **VARIANT\_BOOL\***</span></span>

<span data-ttu-id="ff1ca-186">Definir como **true** se a configuração existir; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-186">Set to **true** if the setting exists; otherwise, **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="ff1ca-187">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ff1ca-187">Examples</span></span>

<span data-ttu-id="ff1ca-188">Os exemplos a seguir mostram o uso de **GetSetting** para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ff1ca-188">The following examples show the use of **GetSetting** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ff1ca-189">JScript</span><span class="sxs-lookup"><span data-stu-id="ff1ca-189">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnIShellDispatch4GetSettingJ()
    {
        var objIShellDispatch4 = new ActiveXObject("Shell.Application");
        var vReturn;
        var ssfSHOWALLOBJECTS = 1;

        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS);
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="ff1ca-190">VBScript</span><span class="sxs-lookup"><span data-stu-id="ff1ca-190">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4GetSettingVB()
        dim objIShellDispatch4
        
        set objIShellDispatch4 = CreateObject("Shell.Application")
        if (not objIShellDispatch4 is nothing) then
            dim vReturn
            dim ssfSHOWALLOBJECTS
            
            ssfSHOWALLOBJECTS = 1
            vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
            alert(vReturn)
        end if
        set objIShellDispatch4 = nothing
    end function
```



<span data-ttu-id="ff1ca-191">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ff1ca-191">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4GetSetting()
    Dim objIShellDispatch4 As Shell
    
    Set objIShellDispatch4 = New Shell
    If (Not objIShellDispatch4 Is Nothing) Then
        Dim vReturn As Variant
        Dim ssfSHOWALLOBJECTS As Long
        
        ssfSHOWALLOBJECTS = 1
        vReturn = objIShellDispatch4.GetSetting(ssfSHOWALLOBJECTS)
        Debug.Print vReturn
    End If
    Set objIShellDispatch4 = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ff1ca-192">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff1ca-192">Requirements</span></span>



| <span data-ttu-id="ff1ca-193">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff1ca-193">Requirement</span></span> | <span data-ttu-id="ff1ca-194">Valor</span><span class="sxs-lookup"><span data-stu-id="ff1ca-194">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1ca-195">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff1ca-195">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1ca-196">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ff1ca-196">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="ff1ca-197">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff1ca-197">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1ca-198">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ff1ca-198">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ff1ca-199">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff1ca-199">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1ca-200"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ca-200"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ff1ca-201">INSERI</span><span class="sxs-lookup"><span data-stu-id="ff1ca-201">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff1ca-202"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ca-202"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ff1ca-203">DLL</span><span class="sxs-lookup"><span data-stu-id="ff1ca-203">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff1ca-204"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ff1ca-204"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




