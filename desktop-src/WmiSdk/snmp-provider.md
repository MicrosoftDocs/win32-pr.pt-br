---
description: O provedor SNMP (Simple Network Management Protocol) permite que aplicativos cliente acessem informações de SNMP por meio de Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: 71e758d9-2ea6-42f5-93b4-d370a96b10cf
ms.tgt_platform: multiple
title: WMI e SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea7e8385e1fb95ac20d14af31f82444350e044
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171977"
---
# <a name="wmi-and-snmp"></a><span data-ttu-id="add02-103">WMI e SNMP</span><span class="sxs-lookup"><span data-stu-id="add02-103">WMI and SNMP</span></span>

<span data-ttu-id="add02-104">O provedor SNMP (Simple Network Management Protocol) permite que aplicativos cliente acessem informações de SNMP por meio de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="add02-104">The Simple Network Management Protocol (SNMP) provider allows client applications to access SNMP information through Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="add02-105">O provedor SNMP não é instalado por padrão.</span><span class="sxs-lookup"><span data-stu-id="add02-105">The SNMP provider is not installed by default.</span></span> <span data-ttu-id="add02-106">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="add02-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

<span data-ttu-id="add02-107">O SNMP (Simple Network Management Protocol) usa um esquema para definir objetos.</span><span class="sxs-lookup"><span data-stu-id="add02-107">Simple Network Management Protocol (SNMP) uses a schema to define objects.</span></span> <span data-ttu-id="add02-108">O esquema é diferente do esquema usado no WMI.</span><span class="sxs-lookup"><span data-stu-id="add02-108">The schema is different from the schema used in WMI.</span></span> <span data-ttu-id="add02-109">O esquema SNMPv1 e SNMPv2C é chamado de estrutura de informações de gerenciamento (SMI) e é empacotado como arquivos de MIB (base de informações de gerenciamento).</span><span class="sxs-lookup"><span data-stu-id="add02-109">The SNMPv1 and SNMPv2C schema is called the Structure of Management Information (SMI), and is packaged as Management Information Base (MIB) files.</span></span> <span data-ttu-id="add02-110">Os arquivos MIB definem objetos usando uma linguagem padrão — o ASN. 1) — e várias definições de macro que servem como modelos para descrever os objetos.</span><span class="sxs-lookup"><span data-stu-id="add02-110">MIB files define objects using a standard language—Abstract Syntax Notation 1 (ASN.1)—and a number of macro definitions that serve as templates for describing the objects.</span></span> <span data-ttu-id="add02-111">As macros fornecem informações como o nome do objeto, o identificador, a sintaxe, a descrição, os direitos de acesso, as operações de protocolo e a codificação de protocolo.</span><span class="sxs-lookup"><span data-stu-id="add02-111">The macros provide information such as the object name, identifier, syntax, description, access rights, protocol operations, and protocol encoding.</span></span> <span data-ttu-id="add02-112">A tabela a seguir lista como o provedor SNMP trata diferentes aspectos de um objeto MIB.</span><span class="sxs-lookup"><span data-stu-id="add02-112">The following table lists how the SNMP provider handles different aspects of a MIB object.</span></span>



| <span data-ttu-id="add02-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="add02-113">Topic</span></span>                                                    | <span data-ttu-id="add02-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="add02-114">Description</span></span>                                                 |
|----------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="add02-115">Macro do tipo de notificação</span><span class="sxs-lookup"><span data-stu-id="add02-115">NOTIFICATION-TYPE Macro</span></span>](notification-type-macro.md)   | <span data-ttu-id="add02-116">Como a macro do **tipo de notificação** é MAPEADA de SNMP para WMI.</span><span class="sxs-lookup"><span data-stu-id="add02-116">How the **NOTIFICATION-TYPE** macro maps from SNMP to WMI.</span></span>  |
| [<span data-ttu-id="add02-117">Macro de tipo de objeto</span><span class="sxs-lookup"><span data-stu-id="add02-117">OBJECT-TYPE Macro</span></span>](object-type-macro.md)               | <span data-ttu-id="add02-118">Como a macro do **tipo de objeto** é MAPEADA de SNMP para WMI.</span><span class="sxs-lookup"><span data-stu-id="add02-118">How the **OBJECT-TYPE** macro maps from SNMP to WMI.</span></span>        |
| [<span data-ttu-id="add02-119">Macro de Convenção TEXTUAL</span><span class="sxs-lookup"><span data-stu-id="add02-119">TEXTUAL-CONVENTION Macro</span></span>](textual-convention-macro.md) | <span data-ttu-id="add02-120">Como a macro de **Convenção textual** é MAPEADA de SNMP para WMI.</span><span class="sxs-lookup"><span data-stu-id="add02-120">How the **TEXTUAL-CONVENTION** macro maps from SNMP to WMI.</span></span> |
| [<span data-ttu-id="add02-121">Macro do tipo INTERCEPTAção</span><span class="sxs-lookup"><span data-stu-id="add02-121">TRAP-TYPE Macro</span></span>](trap-type-macro.md)                   | <span data-ttu-id="add02-122">Como a macro do **tipo Trap** é MAPEADA de SNMP para WMI.</span><span class="sxs-lookup"><span data-stu-id="add02-122">How the **TRAP-TYPE** macro maps from SNMP to WMI.</span></span>          |



 

<span data-ttu-id="add02-123">O provedor SNMP vem com um compilador que converte objetos MIB em objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="add02-123">The SNMP provider comes with a compiler that translates MIB objects into WMI objects.</span></span> <span data-ttu-id="add02-124">O compilador SNMP também pode gerar um erro ou outras mensagens.</span><span class="sxs-lookup"><span data-stu-id="add02-124">The SNMP compiler can also output error or other messages.</span></span> <span data-ttu-id="add02-125">Para obter mais informações, consulte [mensagens de erro do compilador SNMP](snmp-compiler-error-messages.md) e [mensagens de informações gerais](general-information-messages.md).</span><span class="sxs-lookup"><span data-stu-id="add02-125">For more information, see [SNMP compiler Error Messages](snmp-compiler-error-messages.md) and [General Information Messages](general-information-messages.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="add02-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="add02-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="add02-127">Referência de WMI</span><span class="sxs-lookup"><span data-stu-id="add02-127">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="add02-128">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="add02-128">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 



