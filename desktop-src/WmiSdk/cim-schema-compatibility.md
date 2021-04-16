---
description: Compatibilidade do esquema CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilidade do esquema CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df559469ef6a8284b51951dc365bad6c302ca865
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765320"
---
# <a name="cim-schema-compatibility"></a><span data-ttu-id="b416b-103">Compatibilidade do esquema CIM</span><span class="sxs-lookup"><span data-stu-id="b416b-103">CIM Schema Compatibility</span></span>

<span data-ttu-id="b416b-104">Um componente fundamental da infraestrutura de Instrumentação de Gerenciamento do Windows (WMI) é um modelo orientado a objeto das entidades gerenciáveis em um sistema.</span><span class="sxs-lookup"><span data-stu-id="b416b-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="b416b-105">O modelo está em conformidade com um padrão mantido pelo Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) e é conhecido como o modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="b416b-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="b416b-106">O esquema CIM fornece um mecanismo de descrição de dados único para todos os dados que eles fornecem.</span><span class="sxs-lookup"><span data-stu-id="b416b-106">The CIM schema provides a single data description mechanism for any data that they provide.</span></span>

<span data-ttu-id="b416b-107">A partir do Windows 7, o WMI é compatível com a versão do esquema CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ).</span><span class="sxs-lookup"><span data-stu-id="b416b-107">Starting in Windows 7, WMI is compatible with the CIM Schema version 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)).</span></span> <span data-ttu-id="b416b-108">Agora, os usuários podem compilar um esquema definido por DMTF em um computador com Windows.</span><span class="sxs-lookup"><span data-stu-id="b416b-108">Users can now compile a DMTF defined schema on a Windows computer.</span></span>

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a><span data-ttu-id="b416b-109">Benefícios da compatibilidade de 2.17.1 da versão do esquema CIM</span><span class="sxs-lookup"><span data-stu-id="b416b-109">Benefits of CIM Schema version 2.17.1 compatibility</span></span>

-   <span data-ttu-id="b416b-110">Quando um usuário baixa a versão do esquema CIM 2.17.1 ou arquivos MOF do DMTF, eles podem ser compilados com êxito no computador Windows de destino.</span><span class="sxs-lookup"><span data-stu-id="b416b-110">When a user downloads CIM Schema version 2.17.1 or DMTF MOF files, they can be successfully compiled on the target Windows computer.</span></span>
-   <span data-ttu-id="b416b-111">A versão do esquema CIM 2.17.1 adicionou suporte para BIOS, impressoras, mensagens padrão, estado do sistema operacional, paradigmas de gerenciamento de energia modernos, virtualização e segurança.</span><span class="sxs-lookup"><span data-stu-id="b416b-111">The CIM Schema version 2.17.1 added support for BIOS, printers, standard messages, operating system state, modern power management paradigms, virtualization and security.</span></span>
-   <span data-ttu-id="b416b-112">A versão do esquema CIM 2.1.7.1 oferece suporte a perfil adicional.</span><span class="sxs-lookup"><span data-stu-id="b416b-112">CIM Schema version 2.1.7.1 offers additional profile support.</span></span> <span data-ttu-id="b416b-113">Para obter mais informações, consulte [passagem de associação de namespace cruzado](cross-namespace-association-traversal.md)</span><span class="sxs-lookup"><span data-stu-id="b416b-113">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md)</span></span>

 

 



