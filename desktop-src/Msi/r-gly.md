---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 868cb5b7-d5ab-41c7-a6d4-d7964a8ff6de
title: R (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f5093064838ff390b2fa1fa8cc38335d4c5db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828252"
---
# <a name="r-windows-installer"></a><span data-ttu-id="c6489-103">R (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="c6489-103">R (Windows Installer)</span></span>

<span data-ttu-id="c6489-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="c6489-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="c6489-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**interface do usuário reduzida**</span><span class="sxs-lookup"><span data-stu-id="c6489-105"><span id="_msi_reduced_ui_gly"></span><span id="_MSI_REDUCED_UI_GLY"></span>**reduced UI**</span></span>
</dt> <dd>

<span data-ttu-id="c6489-106">Nível dos recursos internos da [*interface do usuário*](i-gly.md) do instalador.</span><span class="sxs-lookup"><span data-stu-id="c6489-106">Level of the installer's [*internal user interface*](i-gly.md) capabilities.</span></span> <span data-ttu-id="c6489-107">Exibe somente caixas de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="c6489-107">Displays only authored modeless dialog boxes.</span></span> <span data-ttu-id="c6489-108">Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c6489-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6489-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**Install**</span><span class="sxs-lookup"><span data-stu-id="c6489-109"><span id="_msi_reinstall_gly"></span><span id="_MSI_REINSTALL_GLY"></span>**reinstall**</span></span>
</dt> <dd>

<span data-ttu-id="c6489-110">Reinstalação parcial ou completa de um aplicativo instalado.</span><span class="sxs-lookup"><span data-stu-id="c6489-110">Partial or complete reinstallation of an installed application.</span></span> <span data-ttu-id="c6489-111">Normalmente, feito para reparar um aplicativo se algum arquivo ou entrada de registro tiver sido corrompido ou estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="c6489-111">Commonly done to repair an application if any files or registry entries have become corrupted or are missing.</span></span> <span data-ttu-id="c6489-112">Para obter mais informações, consulte [reinstalando um recurso ou aplicativo](reinstalling-a-feature-or-application.md).</span><span class="sxs-lookup"><span data-stu-id="c6489-112">For more information, see [Reinstalling a Feature or Application](reinstalling-a-feature-or-application.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6489-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**resiliência**</span><span class="sxs-lookup"><span data-stu-id="c6489-113"><span id="_msi_resiliency_gly"></span><span id="_MSI_RESILIENCY_GLY"></span>**resiliency**</span></span>
</dt> <dd>

<span data-ttu-id="c6489-114">Capacidade do aplicativo de recuperação normal a partir de erro sem gerar mensagens de erro.</span><span class="sxs-lookup"><span data-stu-id="c6489-114">Application capability of graceful recovery from error without generating error messages.</span></span> <span data-ttu-id="c6489-115">Para obter mais informações, consulte [resiliência](resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="c6489-115">For more information, see [Resiliency](resiliency.md).</span></span>

</dd> <dt>

<span data-ttu-id="c6489-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**versão**</span><span class="sxs-lookup"><span data-stu-id="c6489-116"><span id="_msi_rollback_gly"></span><span id="_MSI_ROLLBACK_GLY"></span>**rollback**</span></span>
</dt> <dd>

<span data-ttu-id="c6489-117">A restauração automática do estado original do computador deve ocorrer falha na instalação.</span><span class="sxs-lookup"><span data-stu-id="c6489-117">Automatic restoration of the original state of the computer should the installation fail.</span></span> <span data-ttu-id="c6489-118">Para obter mais informações, consulte [Rollback Installation (Windows Installer)](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="c6489-118">For more information, see [Rollback Installation (Windows Installer)](rollback-installation.md).</span></span>

</dd> </dl>

 

 



