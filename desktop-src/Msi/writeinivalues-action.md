---
description: A ação WriteIniValues grava as informações do arquivo. ini que o aplicativo precisa gravar em seus arquivos. ini.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: Ação WriteIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd96e86c361c7fe83b6ad33959149e82fb9d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828854"
---
# <a name="writeinivalues-action"></a><span data-ttu-id="6ecb7-103">Ação WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="6ecb7-103">WriteIniValues Action</span></span>

<span data-ttu-id="6ecb7-104">A ação WriteIniValues grava as informações do arquivo. ini que o aplicativo precisa gravar em seus arquivos. ini.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-104">The WriteIniValues action writes the .ini file information that the application needs written to its .ini files.</span></span> <span data-ttu-id="6ecb7-105">A gravação dessas informações é restringida pela tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="6ecb7-105">The writing of this information is gated by the [Component table](component-table.md).</span></span> <span data-ttu-id="6ecb7-106">Um valor. ini será gravado se o componente correspondente tiver sido configurado para ser instalado localmente ou executado a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-106">An .ini value is written if the corresponding component has been set to be installed either locally or run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6ecb7-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="6ecb7-107">Sequence Restrictions</span></span>

<span data-ttu-id="6ecb7-108">A ação InstallValidate deve vir antes da ação WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-108">The InstallValidate action must come before the WriteIniValues action.</span></span> <span data-ttu-id="6ecb7-109">Se houver uma [ação RemoveIniValues](removeinivalues-action.md) na sequência, ela deverá vir antes da ação WriteIniValues.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-109">If there is a [RemoveIniValues action](removeinivalues-action.md) in the sequence, then it must come before the WriteIniValues action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6ecb7-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="6ecb7-110">ActionData Messages</span></span>



| <span data-ttu-id="6ecb7-111">Campo</span><span class="sxs-lookup"><span data-stu-id="6ecb7-111">Field</span></span> | <span data-ttu-id="6ecb7-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="6ecb7-112">Description of action data</span></span>              |
|-------|-----------------------------------------|
| <span data-ttu-id="6ecb7-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6ecb7-113">\[1\]</span></span> | <span data-ttu-id="6ecb7-114">Identificador do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-114">Identifier of .ini file.</span></span>                |
| <span data-ttu-id="6ecb7-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="6ecb7-115">\[2\]</span></span> | <span data-ttu-id="6ecb7-116">a chave de arquivo. ini na seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-116">.ini file key in the following section.</span></span> |
| <span data-ttu-id="6ecb7-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="6ecb7-117">\[3\]</span></span> | <span data-ttu-id="6ecb7-118">Item removido do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-118">Item removed from .ini file.</span></span>            |
| <span data-ttu-id="6ecb7-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="6ecb7-119">\[4\]</span></span> | <span data-ttu-id="6ecb7-120">Valor removido do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="6ecb7-120">Value removed from .ini file.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="6ecb7-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ecb7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ecb7-122">Tabela IniFile</span><span class="sxs-lookup"><span data-stu-id="6ecb7-122">IniFile table</span></span>](inifile-table.md)
</dt> </dl>

 

 



