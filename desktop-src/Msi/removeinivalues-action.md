---
description: A ação RemoveIniValues remove as informações do arquivo. ini especificadas para remoção na tabela RemoveIniFile se o componente estiver configurado para ser instalado localmente ou executado de origem.
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: Ação RemoveIniValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dfb847d911e847de00ede6eab30ac3a86615eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922738"
---
# <a name="removeinivalues-action"></a><span data-ttu-id="ae896-103">Ação RemoveIniValues</span><span class="sxs-lookup"><span data-stu-id="ae896-103">RemoveIniValues Action</span></span>

<span data-ttu-id="ae896-104">A ação RemoveIniValues remove as informações do arquivo. ini especificadas para remoção na [tabela RemoveIniFile](removeinifile-table.md) se o componente estiver configurado para ser instalado localmente ou executado de origem.</span><span class="sxs-lookup"><span data-stu-id="ae896-104">The RemoveIniValues action removes .ini file information specified for removal in the [RemoveIniFile table](removeinifile-table.md) if the component is set to be installed locally or run-from-source.</span></span> <span data-ttu-id="ae896-105">A ação RemoveIniValues remove informações do arquivo. ini que foram associadas a um componente na [tabela inifile](inifile-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae896-105">The RemoveIniValues action removes .ini file information that has been associated with a component in the [IniFile table](inifile-table.md).</span></span> <span data-ttu-id="ae896-106">Essa ação também removerá informações do arquivo. ini se as informações tiverem sido gravadas pela [ação WriteIniValues](writeinivalues-action.md) e o componente estiver agendado para ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="ae896-106">This action also removes .ini file information if the information was written by the [WriteIniValues action](writeinivalues-action.md) and the component is scheduled to be uninstalled.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="ae896-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="ae896-107">Sequence Restrictions</span></span>

<span data-ttu-id="ae896-108">A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes da ação RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="ae896-108">The [InstallValidate](installvalidate-action.md) action must be called before the RemoveIniValues action.</span></span> <span data-ttu-id="ae896-109">Se uma ação [WriteIniValues](writeinivalues-action.md) for usada na sequência, ela deverá aparecer após RemoveIniValues.</span><span class="sxs-lookup"><span data-stu-id="ae896-109">If a [WriteIniValues](writeinivalues-action.md) action is used in the sequence, it must appear after RemoveIniValues.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="ae896-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="ae896-110">ActionData Messages</span></span>



| <span data-ttu-id="ae896-111">Campo</span><span class="sxs-lookup"><span data-stu-id="ae896-111">Field</span></span> | <span data-ttu-id="ae896-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="ae896-112">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="ae896-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="ae896-113">\[1\]</span></span> | <span data-ttu-id="ae896-114">Identificador do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="ae896-114">Identifier of .ini file.</span></span>      |
| <span data-ttu-id="ae896-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="ae896-115">\[2\]</span></span> | <span data-ttu-id="ae896-116">Uma seção de chave de arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="ae896-116">An .ini file key section.</span></span>     |
| <span data-ttu-id="ae896-117">\[3\]</span><span class="sxs-lookup"><span data-stu-id="ae896-117">\[3\]</span></span> | <span data-ttu-id="ae896-118">Item removido do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="ae896-118">Item removed from .ini file.</span></span>  |
| <span data-ttu-id="ae896-119">\[4\]</span><span class="sxs-lookup"><span data-stu-id="ae896-119">\[4\]</span></span> | <span data-ttu-id="ae896-120">Valor removido do arquivo. ini.</span><span class="sxs-lookup"><span data-stu-id="ae896-120">Value removed from .ini file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ae896-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae896-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae896-122">Tabela RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="ae896-122">RemoveIniFile table</span></span>](removeinifile-table.md)
</dt> <dt>

[<span data-ttu-id="ae896-123">Tabela IniFile</span><span class="sxs-lookup"><span data-stu-id="ae896-123">IniFile table</span></span>](inifile-table.md)
</dt> <dt>

[<span data-ttu-id="ae896-124">Ação WriteIniValues</span><span class="sxs-lookup"><span data-stu-id="ae896-124">WriteIniValues action</span></span>](writeinivalues-action.md)
</dt> <dt>

[<span data-ttu-id="ae896-125">InstallValidate</span><span class="sxs-lookup"><span data-stu-id="ae896-125">InstallValidate</span></span>](installvalidate-action.md)
</dt> </dl>

 

 



