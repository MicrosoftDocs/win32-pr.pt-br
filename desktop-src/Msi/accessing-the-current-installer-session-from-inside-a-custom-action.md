---
description: Nondeferred ações personalizadas que chamam scripts ou bibliotecas de vínculo dinâmico podem acessar uma instalação em execução para consultar ou modificar os atributos da sessão de instalação atual.
ms.assetid: cf70b0b3-ac81-47ab-a4c8-4db53ed9dc84
title: Acessando a sessão do instalador atual de dentro de uma ação personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29a870247f70742d408c0f5d1d0e67f20cef65d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921536"
---
# <a name="accessing-the-current-installer-session-from-inside-a-custom-action"></a><span data-ttu-id="0003e-103">Acessando a sessão do instalador atual de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="0003e-103">Accessing the Current Installer Session from Inside a Custom Action</span></span>

<span data-ttu-id="0003e-104">Nondeferred ações personalizadas que chamam [scripts](scripts.md) ou [bibliotecas de vínculo dinâmico](dynamic-link-libraries.md) podem acessar uma instalação em execução para consultar ou modificar os atributos da sessão de instalação atual.</span><span class="sxs-lookup"><span data-stu-id="0003e-104">Nondeferred custom actions that call [dynamic-link libraries](dynamic-link-libraries.md) or [scripts](scripts.md) may access a running installation to query or modify the attributes of the current installation session.</span></span> <span data-ttu-id="0003e-105">Somente um objeto de **sessão** pode existir para cada processo e os scripts de ação personalizada não devem tentar criar outra sessão.</span><span class="sxs-lookup"><span data-stu-id="0003e-105">Only one **Session** object can exist for each process, and custom action scripts must not attempt to create another session.</span></span>

<span data-ttu-id="0003e-106">As ações personalizadas só podem adicionar, modificar ou remover linhas, colunas ou tabelas temporárias de um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0003e-106">Custom actions can only add, modify, or remove temporary rows, columns, or tables from a database.</span></span> <span data-ttu-id="0003e-107">As ações personalizadas não podem modificar dados persistentes em um banco de dados, como, por exemplo, aqueles que fazem parte dele armazenados no disco.</span><span class="sxs-lookup"><span data-stu-id="0003e-107">Custom actions cannot modify persistent data in a database, for example, data that is a part of the database stored on disk.</span></span>

[<span data-ttu-id="0003e-108">Bibliotecas de vínculo dinâmico</span><span class="sxs-lookup"><span data-stu-id="0003e-108">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)

<span data-ttu-id="0003e-109">Para acessar uma instalação em execução, ações personalizadas que chamam bibliotecas de vínculo dinâmico (DLL) são passadas para um identificador do tipo MSIHANDLE para a sessão atual como o único argumento para o ponto de entrada de DLL chamado na coluna de destino da [tabela CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="0003e-109">To access a running installation, custom actions that call dynamic-link libraries (DLL) are passed a handle of the type MSIHANDLE for the current session as the only argument to the DLL entry point named in the Target column of the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="0003e-110">Como o instalador fornece esse identificador, a ação personalizada não deve fechá-lo, por exemplo, para receber o identificador *hInstall* do instalador, a função de ação personalizada é declarada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="0003e-110">Because the installer provides this handle, the custom action should not close it, for example, to receive the handle *hInstall* from the installer, the custom action function is declared as follows.</span></span>


```C++
UINT __stdcall CustomAction(MSIHANDLE hInstall)
```



<span data-ttu-id="0003e-111">Para acesso somente leitura ao banco de dados atual, obtenha o identificador de banco de dados chamando [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span><span class="sxs-lookup"><span data-stu-id="0003e-111">For read-only access to the current database obtain the database handle by calling [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase).</span></span> <span data-ttu-id="0003e-112">Para obter mais informações, consulte [obtendo um identificador de banco de dados](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="0003e-112">For more information, see [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span>

[<span data-ttu-id="0003e-113">Scripts</span><span class="sxs-lookup"><span data-stu-id="0003e-113">Scripts</span></span>](scripts.md)

<span data-ttu-id="0003e-114">Ações personalizadas escritas em VBScript ou JScript podem acessar a sessão de instalação atual usando o [**objeto de sessão**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="0003e-114">Custom actions written in VBScript or JScript can access the current installation session by using the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="0003e-115">O instalador cria um objeto de **sessão** chamado "sessão" que faz referência à instalação atual.</span><span class="sxs-lookup"><span data-stu-id="0003e-115">The installer creates a **Session** object named "Session" that references the current installation.</span></span> <span data-ttu-id="0003e-116">Para acesso somente leitura ao banco de dados atual, use a propriedade de [**banco de dados**](session-database.md) do objeto de **sessão** .</span><span class="sxs-lookup"><span data-stu-id="0003e-116">For read-only access to the current database use the [**Database**](session-database.md) property of the **Session** object.</span></span>

<span data-ttu-id="0003e-117">Como um script é executado a partir do contexto do objeto [**Session**](session-object.md) , nem sempre é necessário qualificar totalmente as propriedades e os métodos.</span><span class="sxs-lookup"><span data-stu-id="0003e-117">Because a script is run from the context of the [**Session**](session-object.md) object, it is not always necessary to fully qualify properties and methods.</span></span> <span data-ttu-id="0003e-118">No exemplo a seguir, ao usar o VBScript, a referência me pode substituir o objeto **Session** , por exemplo, as três linhas a seguir são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0003e-118">In the following example, when using VBScript, the Me reference can replace the **Session** object, for example, the following three lines are equivalent.</span></span>


```VB
Session.SetInstallLevel 1
```




```VB
Me.SetInstallLevel 1
```




```VB
SetInstallLevel 1
```



[<span data-ttu-id="0003e-119">Arquivos executáveis</span><span class="sxs-lookup"><span data-stu-id="0003e-119">Executable Files</span></span>](executable-files.md)

<span data-ttu-id="0003e-120">Você não pode acessar a sessão do instalador atual de ações personalizadas que chamam arquivos executáveis iniciados com uma linha de comando, por exemplo, [tipo de ação personalizada 2](custom-action-type-2.md) e [tipo de ação personalizada 18](custom-action-type-18.md).</span><span class="sxs-lookup"><span data-stu-id="0003e-120">You cannot access the current installer session from custom actions that call executable files launched with a command-line, for example, [Custom Action Type 2](custom-action-type-2.md) and [Custom Action Type 18](custom-action-type-18.md).</span></span>

[<span data-ttu-id="0003e-121">Ações personalizadas de execução adiada</span><span class="sxs-lookup"><span data-stu-id="0003e-121">Deferred Execution Custom Actions</span></span>](deferred-execution-custom-actions.md)

<span data-ttu-id="0003e-122">Você não pode acessar a sessão do instalador atual ou todos os dados de propriedade de uma ação personalizada de execução adiada.</span><span class="sxs-lookup"><span data-stu-id="0003e-122">You cannot access the current installer session or all property data from a deferred execution custom action.</span></span> <span data-ttu-id="0003e-123">Para obter mais informações, consulte [obtendo informações de contexto para ações personalizadas de execução adiada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="0003e-123">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0003e-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0003e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0003e-125">Acessando um banco de dados ou sessão de dentro de uma ação personalizada</span><span class="sxs-lookup"><span data-stu-id="0003e-125">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



