---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidade com DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105761580"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="bad17-103">Compatibilidade com DEP/NX</span><span class="sxs-lookup"><span data-stu-id="bad17-103">DEP/NX compatibility</span></span>

<span data-ttu-id="bad17-104">Por padrão, no Windows Internet Explorer 7, o DEP/NX está desabilitado por motivos de compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="bad17-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="bad17-105">Vários Complementos populares não são compatíveis com o DEP/NX e falham quando o Windows Internet Explorer os carrega com o DEP/NX habilitado.</span><span class="sxs-lookup"><span data-stu-id="bad17-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="bad17-106">Normalmente, esses Complementos são criados usando uma versão mais antiga do ATL Framework.</span><span class="sxs-lookup"><span data-stu-id="bad17-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="bad17-107">O ATL 7,1 e versões anteriores não são projetados com o recurso de segurança DEP.</span><span class="sxs-lookup"><span data-stu-id="bad17-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="bad17-108">Felizmente, as novas versões dos Service Packs do Microsoft Windows têm novas APIs DEP/NX que permitem usar o DEP/NX e manter a compatibilidade com versões mais antigas do ATL.</span><span class="sxs-lookup"><span data-stu-id="bad17-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="bad17-109">Essas novas APIs permitem que o Internet Explorer opte pelo DEP/NX sem causar complementos que são criados usando versões mais antigas do ATL para falhar.</span><span class="sxs-lookup"><span data-stu-id="bad17-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="bad17-110">Quando um complemento não é compatível com o DEP/NX e não usa uma ATL desatualizada, você pode usar uma opção Política de Grupo para recusar o DEP/NX para o Internet Explorer até que uma versão atualizada do controle quebrado seja implantada.</span><span class="sxs-lookup"><span data-stu-id="bad17-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="bad17-111">Os administradores locais podem controlar o DEP/NX executando o Internet Explorer como administrador e desmarcando a opção **habilitar proteção de memória** no painel **avançado** de **Opções da Internet**.</span><span class="sxs-lookup"><span data-stu-id="bad17-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bad17-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bad17-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bad17-113">Corrigindo problemas de compatibilidade em aplicativos Web usando o modo de exibição de compatibilidade</span><span class="sxs-lookup"><span data-stu-id="bad17-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
