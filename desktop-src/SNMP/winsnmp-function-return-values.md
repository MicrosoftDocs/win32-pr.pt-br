---
title: Valores de retorno da função WinSNMP
description: O valor de retorno de uma chamada de função WinSNMP pode ser um identificador para um recurso que a implementação do Microsoft WinSNMP aloca para o aplicativo WinSNMP.
ms.assetid: f0723cc7-fa3b-4a72-93a0-49d40a1fedd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a8e42e7d27b1079398efb2970b385bfc4e732c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008042"
---
# <a name="winsnmp-function-return-values"></a><span data-ttu-id="1cf78-103">Valores de retorno da função WinSNMP</span><span class="sxs-lookup"><span data-stu-id="1cf78-103">WinSNMP Function Return Values</span></span>

<span data-ttu-id="1cf78-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1cf78-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1cf78-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1cf78-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1cf78-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="1cf78-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="1cf78-107">O valor de retorno de uma chamada de função WinSNMP pode ser um identificador para um recurso que a implementação do Microsoft WinSNMP aloca para o aplicativo WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="1cf78-107">The return value from a WinSNMP function call can be a handle to a resource that the Microsoft WinSNMP implementation allocates for the WinSNMP application.</span></span>

<span data-ttu-id="1cf78-108">A tabela a seguir lista os cinco tipos de recursos que a implementação aloca.</span><span class="sxs-lookup"><span data-stu-id="1cf78-108">The following table lists the five types of resource handles that the implementation allocates.</span></span>



| <span data-ttu-id="1cf78-109">Tipo de identificador</span><span class="sxs-lookup"><span data-stu-id="1cf78-109">Handle type</span></span>    | <span data-ttu-id="1cf78-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cf78-110">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="1cf78-111">\_sessão HSNMP</span><span class="sxs-lookup"><span data-stu-id="1cf78-111">HSNMP\_SESSION</span></span> | <span data-ttu-id="1cf78-112">Tratar de uma sessão WinSNMP</span><span class="sxs-lookup"><span data-stu-id="1cf78-112">Handle to a WinSNMP session</span></span>       |
| <span data-ttu-id="1cf78-113">\_entidade HSNMP</span><span class="sxs-lookup"><span data-stu-id="1cf78-113">HSNMP\_ENTITY</span></span>  | <span data-ttu-id="1cf78-114">Identificador para uma entidade SNMP</span><span class="sxs-lookup"><span data-stu-id="1cf78-114">Handle to an SNMP entity</span></span>          |
| <span data-ttu-id="1cf78-115">contexto de HSNMP \_</span><span class="sxs-lookup"><span data-stu-id="1cf78-115">HSNMP\_CONTEXT</span></span> | <span data-ttu-id="1cf78-116">Identificador para um contexto SNMP</span><span class="sxs-lookup"><span data-stu-id="1cf78-116">Handle to an SNMP context</span></span>         |
| <span data-ttu-id="1cf78-117">PDU de HSNMP \_</span><span class="sxs-lookup"><span data-stu-id="1cf78-117">HSNMP\_PDU</span></span>     | <span data-ttu-id="1cf78-118">Identificador para uma unidade de dados de protocolo</span><span class="sxs-lookup"><span data-stu-id="1cf78-118">Handle to a protocol data unit</span></span>    |
| <span data-ttu-id="1cf78-119">HSNMP \_ VBL</span><span class="sxs-lookup"><span data-stu-id="1cf78-119">HSNMP\_VBL</span></span>     | <span data-ttu-id="1cf78-120">Identificador para uma lista de associação de variável</span><span class="sxs-lookup"><span data-stu-id="1cf78-120">Handle to a variable binding list</span></span> |



 

<span data-ttu-id="1cf78-121">Para obter mais informações, consulte [objetos de identificador de recursos](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1cf78-121">For more information, see [Resource Handle Objects](resource-handle-objects.md).</span></span>

<span data-ttu-id="1cf78-122">O valor de retorno também pode ser um valor inteiro longo sem sinal do tipo **smiUINT32** que representa um valor de \_ status de snmpapi.</span><span class="sxs-lookup"><span data-stu-id="1cf78-122">The return value can also be an unsigned long integer value of the **smiUINT32** type that represents an SNMPAPI\_STATUS value.</span></span>

<span data-ttu-id="1cf78-123">A tabela a seguir lista os valores de status de WinSNMP e seu significado.</span><span class="sxs-lookup"><span data-stu-id="1cf78-123">The following table lists the WinSNMP status values and their meaning.</span></span>



| <span data-ttu-id="1cf78-124">Status</span><span class="sxs-lookup"><span data-stu-id="1cf78-124">Status</span></span>           | <span data-ttu-id="1cf78-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="1cf78-125">Description</span></span>                                                                      |
|------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="1cf78-126">falha de SNMPAPI \_</span><span class="sxs-lookup"><span data-stu-id="1cf78-126">SNMPAPI\_FAILURE</span></span> | <span data-ttu-id="1cf78-127">Indica um erro.</span><span class="sxs-lookup"><span data-stu-id="1cf78-127">Indicates an error.</span></span> <span data-ttu-id="1cf78-128">Equivale a 0 ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="1cf78-128">Equates to 0 or **NULL**.</span></span>                                    |
| <span data-ttu-id="1cf78-129">SNMPAPI \_ êxito</span><span class="sxs-lookup"><span data-stu-id="1cf78-129">SNMPAPI\_SUCCESS</span></span> | <span data-ttu-id="1cf78-130">Indica que a função foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="1cf78-130">Indicates the function completed successfully.</span></span> <span data-ttu-id="1cf78-131">Equivale a 1 ou uma contagem positiva.</span><span class="sxs-lookup"><span data-stu-id="1cf78-131">Equates to 1 or a positive count.</span></span> |



 

 

 