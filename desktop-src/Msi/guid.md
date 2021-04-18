---
description: O tipo de dados GUID é uma cadeia de caracteres de texto que representa um identificador de classe (ID). COM deve ser capaz de converter a cadeia de caracteres em uma ID de classe válida. Todos os GUIDs devem ser criados em letras maiúsculas.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766874"
---
# <a name="guid"></a><span data-ttu-id="7afb3-105">GUID</span><span class="sxs-lookup"><span data-stu-id="7afb3-105">GUID</span></span>

<span data-ttu-id="7afb3-106">O tipo de dados GUID é uma cadeia de caracteres de texto que representa um identificador de classe (ID).</span><span class="sxs-lookup"><span data-stu-id="7afb3-106">The GUID data type is a text string representing a Class identifier (ID).</span></span> <span data-ttu-id="7afb3-107">COM deve ser capaz de converter a cadeia de caracteres em uma ID de classe válida.</span><span class="sxs-lookup"><span data-stu-id="7afb3-107">COM must be able to convert the string to a valid Class ID.</span></span> <span data-ttu-id="7afb3-108">Todos os GUIDs devem ser criados em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="7afb3-108">All GUIDs must be authored in uppercase.</span></span>

<span data-ttu-id="7afb3-109">O formato válido para um GUID é {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, em que X é um dígito hexadecimal (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F).</span><span class="sxs-lookup"><span data-stu-id="7afb3-109">The valid format for a GUID is {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} where X is a hex digit (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).</span></span>

<span data-ttu-id="7afb3-110">Observe que os utilitários como o GUIDGEN podem gerar GUIDs contendo letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7afb3-110">Note that utilities such as GUIDGEN can generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="7afb3-111">Eles devem ser alterados para letras maiúsculas antes que o GUID possa ser usado pelo instalador como um código de produto válido, código de pacote ou código de componente.</span><span class="sxs-lookup"><span data-stu-id="7afb3-111">These must all be changed to uppercase letters before the GUID can be used by the installer as a valid product code, package code, or component code.</span></span>

 

 



