---
title: Windows (noções básicas de Design)
description: As janelas são as principais \ 0034; telas \ 0034; ou superfícies de interface do usuário do seu aplicativo de área de trabalho, incluindo o próprio Windows e pop-ups, caixas de diálogo e assistentes principais. Siga estas diretrizes ao decidir qual superfície usar e a melhor maneira de usá-las.
ms.assetid: E1FA78DA-D580-4B0E-AB59-29F013278766
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 5b7bb58750635af25d49208992d5583c44520a04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930067"
---
# <a name="windows-design-basics"></a><span data-ttu-id="b35b7-104">Windows (noções básicas de Design)</span><span class="sxs-lookup"><span data-stu-id="b35b7-104">Windows (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="b35b7-105">Este guia de design foi criado para o Windows 7 e não foi atualizado para versões mais recentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="b35b7-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="b35b7-106">Grande parte da orientação ainda se aplica em princípio, mas a apresentação e os exemplos não refletem nossas [diretrizes de design atuais](/windows/uwp/design/).</span><span class="sxs-lookup"><span data-stu-id="b35b7-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="b35b7-107">As janelas são as principais "telas" ou as superfícies de interface do usuário do seu aplicativo de área de trabalho, incluindo o próprio Windows e pop-ups, caixas de diálogo e assistentes principais.</span><span class="sxs-lookup"><span data-stu-id="b35b7-107">Windows are the main "canvases" or UI surfaces of your desktop app, including the main windows itself and pop-ups, dialogs, and wizards.</span></span> <span data-ttu-id="b35b7-108">Siga estas diretrizes ao decidir qual superfície usar e a melhor maneira de usá-las.</span><span class="sxs-lookup"><span data-stu-id="b35b7-108">Follow these guidelines when deciding which surface to use and how best to use them.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b35b7-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="b35b7-109">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b35b7-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="b35b7-110">Topic</span></span></th>
<th><span data-ttu-id="b35b7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="b35b7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b35b7-112"><a href="win-window-mgt.md">Gerenciamento de janelas</a></span><span class="sxs-lookup"><span data-stu-id="b35b7-112"><a href="win-window-mgt.md">Window Management</a></span></span><br/></td>
<td><span data-ttu-id="b35b7-113">Este artigo aborda o posicionamento padrão do Windows quando inicialmente exibido na tela, sua ordem de empilhamento relativa a outras janelas (<a href="glossary.md">ordem Z</a>), seu tamanho inicial e como a exibição afeta o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="b35b7-113">This article covers default placement of windows when initially displayed on the screen, their stacking order relative to other windows (<a href="glossary.md">Z order</a>), their initial size, and how their display affects input focus.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b35b7-114"><a href="win-window-frames.md">Quadros de janela</a></span><span class="sxs-lookup"><span data-stu-id="b35b7-114"><a href="win-window-frames.md">Window Frames</a></span></span><br/></td>
<td><span data-ttu-id="b35b7-115">A maioria dos programas deve usar quadros de janela padrão.</span><span class="sxs-lookup"><span data-stu-id="b35b7-115">Most programs should use standard window frames.</span></span> <span data-ttu-id="b35b7-116">Aplicativos de imersão podem ter um modo de tela inteira que oculta o quadro da janela.</span><span class="sxs-lookup"><span data-stu-id="b35b7-116">Immersive applications can have a full screen mode that hides the window frame.</span></span> <span data-ttu-id="b35b7-117">Considere o uso estratégico de vidro para uma aparência mais simples, mais leve e coesa.</span><span class="sxs-lookup"><span data-stu-id="b35b7-117">Consider using glass strategically for a simpler, lighter, more cohesive look.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b35b7-118"><a href="win-dialog-box.md">Caixas de diálogo</a></span><span class="sxs-lookup"><span data-stu-id="b35b7-118"><a href="win-dialog-box.md">Dialog Boxes</a></span></span><br/></td>
<td><span data-ttu-id="b35b7-119">Uma caixa de diálogo é uma janela secundária que permite aos usuários executar um comando, pergunta aos usuários uma pergunta ou fornece aos usuários informações ou comentários sobre o progresso.</span><span class="sxs-lookup"><span data-stu-id="b35b7-119">A dialog box is a secondary window that allows users to perform a command, asks users a question, or provides users with information or progress feedback.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b35b7-120"><a href="win-common-dlg.md">Caixas de diálogo comuns</a></span><span class="sxs-lookup"><span data-stu-id="b35b7-120"><a href="win-common-dlg.md">Common Dialogs</a></span></span><br/></td>
<td><span data-ttu-id="b35b7-121">Os diálogos comuns do Microsoft Windows consistem nas caixas de diálogo abrir arquivo, salvar arquivo, abrir pasta, localizar e substituir, imprimir, Configurar página, fonte e cor.</span><span class="sxs-lookup"><span data-stu-id="b35b7-121">The Microsoft Windows common dialogs consist of the Open File, Save File, Open Folder, Find and Replace, Print, Page Setup, Font, and Color dialog boxes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b35b7-122"><a href="win-wizards.md">Assistentes</a></span><span class="sxs-lookup"><span data-stu-id="b35b7-122"><a href="win-wizards.md">Wizards</a></span></span><br/></td>
<td><span data-ttu-id="b35b7-123">Apesar de o maravilhoso, o nome estranho, os assistentes não são, na verdade, uma forma especial de interface do usuário e têm apenas um determinado intervalo de utilitários.</span><span class="sxs-lookup"><span data-stu-id="b35b7-123">Despite that wonderful, whimsical name, wizards are not really a special form of user interface, and they have only a particular range of utility.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b35b7-124"><a href="win-property-win.md">Janelas de propriedades</a></span><span class="sxs-lookup"><span data-stu-id="b35b7-124"><a href="win-property-win.md">Property Windows</a></span></span><br/></td>
<td><span data-ttu-id="b35b7-125">A janela de propriedades é o nome coletivo para os seguintes tipos de interfaces de usuário (UIs):</span><span class="sxs-lookup"><span data-stu-id="b35b7-125">Property window is the collective name for the following types of user interfaces (UIs):</span></span><br/>
<ul>
<li><span data-ttu-id="b35b7-126">Folha de propriedades: usada para <strong>Exibir e alterar as propriedades de um objeto ou de uma coleção de objetos em uma caixa de diálogo</strong>.</span><span class="sxs-lookup"><span data-stu-id="b35b7-126">Property sheet: used to <strong>view and change properties for an object or collection of objects in a dialog box</strong>.</span></span></li>
<li><span data-ttu-id="b35b7-127">Inspetor de propriedades: usado para <strong>Exibir e alterar as propriedades de um objeto ou de uma coleção de objetos em um painel</strong>.</span><span class="sxs-lookup"><span data-stu-id="b35b7-127">Property inspector: used to <strong>view and change properties for an object or collection of objects in a pane</strong>.</span></span></li>
<li><span data-ttu-id="b35b7-128">Caixa de diálogo opções: usada para <strong>Exibir e alterar as opções de um aplicativo</strong>.</span><span class="sxs-lookup"><span data-stu-id="b35b7-128">Options dialog box: used to <strong>view and change options for an application</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

