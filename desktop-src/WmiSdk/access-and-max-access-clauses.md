---
description: Cada definição de objeto MIB contém uma cláusula de acesso (SNMPv1) ou MAX-ACCESS (SNMPv2C) que define os direitos de acesso ao objeto.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Cláusulas ACCESS e MAX-ACCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810627"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="18ee3-103">Cláusulas ACCESS e MAX-ACCESS</span><span class="sxs-lookup"><span data-stu-id="18ee3-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="18ee3-104">Cada definição de objeto MIB contém uma cláusula de acesso (SNMPv1) ou MAX-ACCESS (SNMPv2C) que define os direitos de acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="18ee3-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="18ee3-105">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="18ee3-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="18ee3-106">A tabela a seguir lista o mapeamento da cláusula de acesso SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="18ee3-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="18ee3-107">Cláusula de acesso MIB</span><span class="sxs-lookup"><span data-stu-id="18ee3-107">MIB ACCESS clause</span></span> | <span data-ttu-id="18ee3-108">Qualificador CIM</span><span class="sxs-lookup"><span data-stu-id="18ee3-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="18ee3-109">somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ee3-109">read-only</span></span>         | <span data-ttu-id="18ee3-110">**Ler**</span><span class="sxs-lookup"><span data-stu-id="18ee3-110">**Read**</span></span>            |
| <span data-ttu-id="18ee3-111">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="18ee3-111">read-write</span></span>        | <span data-ttu-id="18ee3-112">**Leitura**, **gravação**</span><span class="sxs-lookup"><span data-stu-id="18ee3-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="18ee3-113">somente gravação</span><span class="sxs-lookup"><span data-stu-id="18ee3-113">write-only</span></span>        | <span data-ttu-id="18ee3-114">**Gravar**</span><span class="sxs-lookup"><span data-stu-id="18ee3-114">**Write**</span></span>           |
| <span data-ttu-id="18ee3-115">Não acessível</span><span class="sxs-lookup"><span data-stu-id="18ee3-115">not-accessible</span></span>    | <span data-ttu-id="18ee3-116">**Não \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="18ee3-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="18ee3-117">A tabela a seguir lista o mapeamento da cláusula de acesso MAX do SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="18ee3-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="18ee3-118">MIB-cláusula de acesso</span><span class="sxs-lookup"><span data-stu-id="18ee3-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="18ee3-119">Qualificador CIM</span><span class="sxs-lookup"><span data-stu-id="18ee3-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="18ee3-120">somente leitura</span><span class="sxs-lookup"><span data-stu-id="18ee3-120">read-only</span></span>             | <span data-ttu-id="18ee3-121">**Ler**</span><span class="sxs-lookup"><span data-stu-id="18ee3-121">**Read**</span></span>            |
| <span data-ttu-id="18ee3-122">leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="18ee3-122">read-write</span></span>            | <span data-ttu-id="18ee3-123">**Leitura**, **gravação**</span><span class="sxs-lookup"><span data-stu-id="18ee3-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="18ee3-124">ler-criar</span><span class="sxs-lookup"><span data-stu-id="18ee3-124">read-create</span></span>           | <span data-ttu-id="18ee3-125">**Ler**</span><span class="sxs-lookup"><span data-stu-id="18ee3-125">**Read**</span></span>            |
| <span data-ttu-id="18ee3-126">acessível para notificação</span><span class="sxs-lookup"><span data-stu-id="18ee3-126">accessible-for-notify</span></span> | <span data-ttu-id="18ee3-127">**Não \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="18ee3-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="18ee3-128">Não acessível</span><span class="sxs-lookup"><span data-stu-id="18ee3-128">not-accessible</span></span>        | <span data-ttu-id="18ee3-129">**Não \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="18ee3-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="18ee3-130">Quando um objeto MIB é mapeado para não acessível e não é uma propriedade com chave da classe, não há nenhum mapeamento do objeto MIB em si.</span><span class="sxs-lookup"><span data-stu-id="18ee3-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



