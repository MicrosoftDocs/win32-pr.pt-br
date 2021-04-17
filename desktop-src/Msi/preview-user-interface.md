---
description: O arquivo VBScript WiDialog.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. Este exemplo mostra como o script é usado para visualizar caixas de diálogo em um banco de dados Windows Installer.
ms.assetid: b3d72ba1-1d19-4460-8b9b-94f72214e8b1
title: Visualizar interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7736c442cdfcb22034326ff459eb89fc28b0c9af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749786"
---
# <a name="preview-user-interface"></a><span data-ttu-id="ee8a5-104">Visualizar interface do usuário</span><span class="sxs-lookup"><span data-stu-id="ee8a5-104">Preview User Interface</span></span>

<span data-ttu-id="ee8a5-105">O arquivo VBScript WiDialog.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a5-105">The VBScript file WiDialog.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="ee8a5-106">Este exemplo mostra como o script é usado para visualizar caixas de diálogo em um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-106">This sample shows how script is used to preview dialogs in a Windows Installer database.</span></span>

<span data-ttu-id="ee8a5-107">Este exemplo demonstra:</span><span class="sxs-lookup"><span data-stu-id="ee8a5-107">This sample demonstrates:</span></span>

-   <span data-ttu-id="ee8a5-108">[**Método OpenDatabase (objeto Installer)**](installer-opendatabase.md), o [**método CreateRecord**](installer-createrecord.md)e o [**método LastErrorRecord**](installer-lasterrorrecord.md) do [**objeto instalador**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="ee8a5-108">[**OpenDatabase method (Installer Object)**](installer-opendatabase.md), the [**CreateRecord method**](installer-createrecord.md), and the [**LastErrorRecord method**](installer-lasterrorrecord.md) of the [**Installer Object**](installer-object.md)</span></span>
-   <span data-ttu-id="ee8a5-109">[**Método OpenView**](database-openview.md) e o [**método EnableUIpreview**](database-enableuipreview.md) do [**objeto Database**](database-object.md)</span><span class="sxs-lookup"><span data-stu-id="ee8a5-109">[**OpenView method**](database-openview.md) and the [**EnableUIpreview method**](database-enableuipreview.md) of the [**Database Object**](database-object.md)</span></span>
-   <span data-ttu-id="ee8a5-110">[**Método execute**](view-execute.md) e o [**método FETCH**](view-fetch.md) do [**objeto View**](view-object.md)</span><span class="sxs-lookup"><span data-stu-id="ee8a5-110">[**Execute method**](view-execute.md) and the [**Fetch method**](view-fetch.md) of the [**View Object**](view-object.md)</span></span>
-   <span data-ttu-id="ee8a5-111">[**Propriedade StringData**](record-stringdata.md) Propertyof o [ **objeto Record**](record-object.md)</span><span class="sxs-lookup"><span data-stu-id="ee8a5-111">[**StringData property**](record-stringdata.md) propertyof the [**Record Object**](record-object.md)</span></span>

<span data-ttu-id="ee8a5-112">Este exemplo requer a versão CScript.exe ou WScript.exe do Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-112">This sample requires the CScript.exe or WScript.exe version of Windows Script Host.</span></span> <span data-ttu-id="ee8a5-113">Para usar CScript.exe para este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-113">To use CScript.exe for this sample, type a command at the command prompt using the following syntax.</span></span> <span data-ttu-id="ee8a5-114">A ajuda será exibida se o primeiro argumento for/?</span><span class="sxs-lookup"><span data-stu-id="ee8a5-114">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="ee8a5-115">ou se poucos argumentos forem especificados.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-115">or if too few arguments are specified.</span></span> <span data-ttu-id="ee8a5-116">Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] .</span><span class="sxs-lookup"><span data-stu-id="ee8a5-116">To redirect the output to a file, end the command line with VBS > \[*path to file*\].</span></span> <span data-ttu-id="ee8a5-117">O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-117">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="ee8a5-118">**cscript WiDialog.vbs** *\[ caminho para \] \[ nomes \] de caixa de diálogo do banco de dados*</span><span class="sxs-lookup"><span data-stu-id="ee8a5-118">**cscript WiDialog.vbs** *\[path to database\]\[Dialog names\]*</span></span>

<span data-ttu-id="ee8a5-119">Especifique o caminho para um banco de dados Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-119">Specify the path to a Windows Installer database.</span></span> <span data-ttu-id="ee8a5-120">Especifique o nome de uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-120">Specify the name of a dialog.</span></span> <span data-ttu-id="ee8a5-121">Esse nome deve ser listado na coluna caixa de diálogo da [tabela de diálogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a5-121">This name must be listed in the Dialog column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="ee8a5-122">Para exibir um mural, acrescente o nome da caixa de diálogo com o nome do controle da [tabela de controle](control-table.md) e acrescente isso ao nome do mural na tabela do [mural](billboard-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a5-122">To view a billboard, append the dialog's name with the control's name from the [Control table](control-table.md) and append this to the name of the billboard in the [Billboard table](billboard-table.md).</span></span> <span data-ttu-id="ee8a5-123">Se nenhuma caixa de diálogo for especificada, todas as caixas de diálogo na tabela de diálogo serão exibidas em sequência.</span><span class="sxs-lookup"><span data-stu-id="ee8a5-123">If no dialogs are specified, all dialogs in Dialog table are displayed sequentially.</span></span>

<span data-ttu-id="ee8a5-124">Para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a5-124">For additional scripting examples, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md).</span></span> <span data-ttu-id="ee8a5-125">Para utilitários de exemplo que não exigem o Windows Script Host, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a5-125">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



