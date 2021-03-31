---
title: Gerenciando a política de retransmissão
description: O aplicativo WinSNMP pode solicitar que a implementação do Microsoft WinSNMP execute a política de retransmissão do aplicativo. Quando a implementação gerencia a retransmissão, ela usa o período de tempo limite e os valores de contagem de repetição em seu banco de dados.
ms.assetid: 1f1a9589-3566-4d90-ac4d-7acf69f34676
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f2e47d983f8da62ccb8ffbe9c20b35c71bfbb70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005848"
---
# <a name="managing-the-retransmission-policy"></a><span data-ttu-id="81aed-104">Gerenciando a política de retransmissão</span><span class="sxs-lookup"><span data-stu-id="81aed-104">Managing the Retransmission Policy</span></span>

<span data-ttu-id="81aed-105">O aplicativo WinSNMP pode solicitar que a implementação do Microsoft WinSNMP execute a política de retransmissão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81aed-105">The WinSNMP application can request that the Microsoft WinSNMP implementation execute the application's retransmission policy.</span></span> <span data-ttu-id="81aed-106">Quando a implementação gerencia a retransmissão, ela usa o período de tempo limite e os valores de contagem de repetição em seu banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81aed-106">When the implementation manages retransmission, it uses the time-out period and the retry count values in its database.</span></span>

<span data-ttu-id="81aed-107">A implementação identifica o modo de retransmissão padrão em um valor de retorno da função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) durante a inicialização.</span><span class="sxs-lookup"><span data-stu-id="81aed-107">The implementation identifies the default retransmission mode in a return value from the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function during initialization.</span></span> <span data-ttu-id="81aed-108">O modo pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="81aed-108">The mode can be one of the following values.</span></span>



| <span data-ttu-id="81aed-109">Valor</span><span class="sxs-lookup"><span data-stu-id="81aed-109">Value</span></span>        | <span data-ttu-id="81aed-110">Significado</span><span class="sxs-lookup"><span data-stu-id="81aed-110">Meaning</span></span>                                                                      |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="81aed-111">SNMPAPI \_ em</span><span class="sxs-lookup"><span data-stu-id="81aed-111">SNMPAPI\_ON</span></span>  | <span data-ttu-id="81aed-112">A implementação está executando a política de retransmissão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81aed-112">The implementation is executing the application's retransmission policy.</span></span>     |
| <span data-ttu-id="81aed-113">SNMPAPI \_ desativado</span><span class="sxs-lookup"><span data-stu-id="81aed-113">SNMPAPI\_OFF</span></span> | <span data-ttu-id="81aed-114">A implementação não está executando a política de retransmissão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="81aed-114">The implementation is not executing the application's retransmission policy.</span></span> |



 

<span data-ttu-id="81aed-115">Um aplicativo WinSNMP pode recuperar a qualquer momento o modo de retransmissão atual em vigor para a implementação chamando a função [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="81aed-115">A WinSNMP application can retrieve at any time the current retransmission mode in effect for the implementation by calling the [**SnmpGetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretransmitmode) function.</span></span> <span data-ttu-id="81aed-116">A API WinSNMP fornece outras [funções de banco de dados](winsnmp-functions.md) que simplificam o gerenciamento da política de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="81aed-116">The WinSNMP API provides other [database functions](winsnmp-functions.md) that simplify management of the retransmission policy.</span></span>

<span data-ttu-id="81aed-117">A qualquer momento durante a execução do programa, o aplicativo WinSNMP pode ajustar a execução da política executando uma das seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="81aed-117">At any time during program execution, the WinSNMP application can adjust execution of the policy by performing one of the following steps:</span></span>

-   <span data-ttu-id="81aed-118">Solicite que a implementação inicie ou pare de executar a política de retransmissão chamando a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="81aed-118">Request that the implementation start or stop executing the retransmission policy by calling the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="81aed-119">Para obter mais informações, consulte [ativando e](turning-retransmission-on-and-off.md)desativando a retransmissão.</span><span class="sxs-lookup"><span data-stu-id="81aed-119">For more information, see [Turning Retransmission On and Off](turning-retransmission-on-and-off.md).</span></span>
-   <span data-ttu-id="81aed-120">Modifique o período de tempo limite e repita a contagem de valores no banco de dados da implementação.</span><span class="sxs-lookup"><span data-stu-id="81aed-120">Modify the time-out period and retry count values in the implementation's database.</span></span> <span data-ttu-id="81aed-121">Para obter mais informações, consulte [alterando a política de retransmissão](changing-the-retransmission-policy.md).</span><span class="sxs-lookup"><span data-stu-id="81aed-121">For more information, see [Changing the Retransmission Policy](changing-the-retransmission-policy.md).</span></span>
-   <span data-ttu-id="81aed-122">Chame a função [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) para cancelar o ciclo de retransmissão e liberar estruturas de dados internas associadas a uma única solicitação de mensagem SNMP.</span><span class="sxs-lookup"><span data-stu-id="81aed-122">Call the [**SnmpCancelMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcancelmsg) function to cancel the retransmission cycle and release internal data structures associated with a single SNMP message request.</span></span> <span data-ttu-id="81aed-123">Para obter mais informações, consulte [cancelando a retransmissão](canceling-retransmission.md).</span><span class="sxs-lookup"><span data-stu-id="81aed-123">For more information, see [Canceling Retransmission](canceling-retransmission.md).</span></span>

<span data-ttu-id="81aed-124">O aplicativo pode executar sua própria política de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="81aed-124">The application can execute its own retransmission policy.</span></span> <span data-ttu-id="81aed-125">Nesse caso, a execução pode ou não ser baseada nos valores no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="81aed-125">In this case, execution may or may not be based on the values in the database.</span></span>

 

 




