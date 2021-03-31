---
title: O arquivo UUID de interface
description: O arquivo de UUID de interface coleta as definições dos identificadores de interface de todas as interfaces no arquivo IDL processado.
ms.assetid: 8e7198e9-8166-426d-a6cc-e9a0a798811b
keywords:
- MIDL e MIDL de COM, interfaces, arquivos UUID de proxy
- arquivo UUID de interface MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d9ff6e8a115f51aaff001749d29e1206716abc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636887"
---
# <a name="the-interface-uuid-file"></a><span data-ttu-id="706a3-105">O arquivo UUID de interface</span><span class="sxs-lookup"><span data-stu-id="706a3-105">The Interface UUID File</span></span>

<span data-ttu-id="706a3-106">O arquivo de UUID de interface coleta as definições dos identificadores de interface de todas as interfaces no arquivo IDL processado.</span><span class="sxs-lookup"><span data-stu-id="706a3-106">The interface UUID file collects the definitions of the interface identifiers from all interfaces in the processed IDL file.</span></span> <span data-ttu-id="706a3-107">Semelhante ao arquivo stub e ao arquivo de cabeçalho, o fechamento do fluxo de entrada é definido pelo arquivo IDL atual e pelos arquivos incluídos.</span><span class="sxs-lookup"><span data-stu-id="706a3-107">Similar to the stub file and the header file, the input stream closure is defined by the current IDL file and the included files.</span></span> <span data-ttu-id="706a3-108">Por exemplo, para a interface IFace, o compilador gera uma IFace de IID constante \_ e a inicializa para o UUID da interface especificado no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="706a3-108">For example, for Interface IFace, the compiler generates a constant IID\_IFace and initializes it to the interface's UUID specified in the IDL file.</span></span> <span data-ttu-id="706a3-109">Os aplicativos cliente e a DLL de proxy usam essa constante para identificar a interface.</span><span class="sxs-lookup"><span data-stu-id="706a3-109">Client applications and the proxy DLL use this constant to identify the interface.</span></span>

<span data-ttu-id="706a3-110">O nome padrão para um arquivo de interface IID gerado a partir de um arquivo. idl é o arquivo \_ i.c.</span><span class="sxs-lookup"><span data-stu-id="706a3-110">The default name for an interface IID file generated from a file.idl is File\_i.c.</span></span> <span data-ttu-id="706a3-111">A opção de compilador [**/IID nomedearquivo**](-iid.md) MIDL substitui o nome padrão do arquivo UUID da interface.</span><span class="sxs-lookup"><span data-stu-id="706a3-111">The [**/iid**](-iid.md) MIDL compiler switch overrides the default name of the interface UUID file.</span></span>

 

 




