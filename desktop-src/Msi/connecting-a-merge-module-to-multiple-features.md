---
description: O método Connect do objeto de mesclagem pode ser usado para conectar um módulo a um recurso adicional que foi mesclado ao banco de dados ou que será mesclado no banco de dados. O recurso deve existir antes de chamar este método.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Conectando um módulo de mesclagem a vários recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829352"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a><span data-ttu-id="49e6c-104">Conectando um módulo de mesclagem a vários recursos</span><span class="sxs-lookup"><span data-stu-id="49e6c-104">Connecting a Merge Module to Multiple Features</span></span>

<span data-ttu-id="49e6c-105">O método [**Connect**](merge-connect.md) do [objeto de mesclagem](merge-object.md) pode ser usado para conectar um módulo a um recurso adicional que foi mesclado ao banco de dados ou que será mesclado no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="49e6c-105">The [**Connect**](merge-connect.md) method of the [Merge Object](merge-object.md) can be used to connect a module to an additional feature that has been merged into the database or that will be merged into the database.</span></span> <span data-ttu-id="49e6c-106">O recurso deve existir antes de chamar este método.</span><span class="sxs-lookup"><span data-stu-id="49e6c-106">The feature must exist before calling this method.</span></span>

<span data-ttu-id="49e6c-107">Um módulo de mesclagem nunca deve entregar um componente que contém arquivos do sistema ao recurso principal de um aplicativo, pois isso pode fazer com que o instalador valide e repare o aplicativo sempre que o arquivo do sistema for usado.</span><span class="sxs-lookup"><span data-stu-id="49e6c-107">A merge module should never deliver a component containing system files to the main feature of an application, because this may cause the Installer to validate and repair the application each time the system file is used.</span></span> <span data-ttu-id="49e6c-108">Um arquivo. msi destinado a aceitar componentes de um módulo de mesclagem deve ser criado para que qualquer componente que contenha arquivos do sistema pertença apenas a recursos separados do recurso principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49e6c-108">A .msi file that is intended to accept components from a merge module should be authored so that any components that contain system files only belong to features that are separate from the main feature of the application.</span></span>

<span data-ttu-id="49e6c-109">Se o pacote usar um módulo de mesclagem que contém arquivos do sistema que vinculam todos os componentes do módulo de mesclagem ao recurso principal do aplicativo, uma tentativa de usar o arquivo do sistema poderá disparar o instalador para tentar reparar o recurso principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="49e6c-109">If your package uses a merge module containing system files that link all the components from the merge module to the main feature of the application, an attempt to use the system file may trigger the Installer to try and repair the main feature of the application.</span></span> <span data-ttu-id="49e6c-110">Se o recurso principal não puder ser reparado, a instalação poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="49e6c-110">If the main feature cannot be repaired, the installation may fail.</span></span>

 

 



