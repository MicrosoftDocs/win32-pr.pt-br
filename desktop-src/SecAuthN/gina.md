---
description: A finalidade de uma DLL GINA é fornecer procedimentos de autenticação e identificação de usuário personalizáveis. A GINA padrão faz isso delegando o monitoramento de eventos SAS ao Winlogon, que recebe e processa as sequências de atenção seguro (SASs) de CTL + ALT + DEL.
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662744"
---
# <a name="gina"></a><span data-ttu-id="d70ca-104">GINA</span><span class="sxs-lookup"><span data-stu-id="d70ca-104">GINA</span></span>

<span data-ttu-id="d70ca-105">A [*Gina*](/windows/desktop/SecGloss/g-gly) opera no [*contexto*](/windows/desktop/SecGloss/c-gly) do processo do [*Winlogon*](/windows/desktop/SecGloss/w-gly) e, como tal, a dll Gina é carregada logo no início do processo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="d70ca-105">The [*GINA*](/windows/desktop/SecGloss/g-gly) operates in the [*context*](/windows/desktop/SecGloss/c-gly) of the [*Winlogon*](/windows/desktop/SecGloss/w-gly) process and, as such, the GINA DLL is loaded very early in the boot process.</span></span> <span data-ttu-id="d70ca-106">A DLL GINA deve seguir as regras para que a integridade do sistema seja mantida, particularmente em relação à interação com o usuário.</span><span class="sxs-lookup"><span data-stu-id="d70ca-106">The GINA DLL must follow rules so that the integrity of the system is maintained, particularly with respect to interaction with the user.</span></span>

> [!Note]  
> <span data-ttu-id="d70ca-107">As DLLs GINAs são ignoradas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d70ca-107">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="d70ca-108">O uso mais comum da GINA é comunicar-se com um dispositivo externo, como um [*leitor*](/windows/desktop/SecGloss/r-gly)de cartão inteligente.</span><span class="sxs-lookup"><span data-stu-id="d70ca-108">The most common use of the GINA is to communicate with an external device such as a smart-card [*reader*](/windows/desktop/SecGloss/r-gly).</span></span> <span data-ttu-id="d70ca-109">É essencial definir o parâmetro Start para o driver de dispositivo como System (WinNT. h: início do \_ sistema de serviço \_ ) para garantir que o driver seja carregado até o momento em que a Gina é invocada.</span><span class="sxs-lookup"><span data-stu-id="d70ca-109">It is essential to set the start parameter for the device driver to system (Winnt.h: SERVICE\_SYSTEM\_START) to ensure that the driver is loaded by the time the GINA is invoked.</span></span>

<span data-ttu-id="d70ca-110">A finalidade de uma DLL GINA é fornecer procedimentos de autenticação e identificação de usuário personalizáveis.</span><span class="sxs-lookup"><span data-stu-id="d70ca-110">The purpose of a GINA DLL is to provide customizable user identification and authentication procedures.</span></span> <span data-ttu-id="d70ca-111">A GINA padrão faz isso delegando o monitoramento de eventos SAS ao Winlogon, que recebe e processa as [*sequências de atenção seguro*](/windows/desktop/SecGloss/s-gly) (SASs) de CTL + ALT + del.</span><span class="sxs-lookup"><span data-stu-id="d70ca-111">The default GINA does this by delegating SAS event monitoring to Winlogon, which receives and processes CTL+ALT+DEL [*secure attention sequences*](/windows/desktop/SecGloss/s-gly) (SASs).</span></span> <span data-ttu-id="d70ca-112">Uma GINA personalizada é responsável por se configurar para receber eventos de SAS (além do evento de SAS CTRL + ALT + DEL) e notificar o Winlogon quando ocorrerem eventos de SAS.</span><span class="sxs-lookup"><span data-stu-id="d70ca-112">A custom GINA is responsible for setting itself up to receive SAS events (other than the default CTRL+ALT+DEL SAS event) and notifying Winlogon when SAS events occur.</span></span> <span data-ttu-id="d70ca-113">O Winlogon avaliará seu estado para determinar o que é necessário para processar a SAS da GINAção personalizada.</span><span class="sxs-lookup"><span data-stu-id="d70ca-113">Winlogon will evaluate its state to determine what is required to process the custom GINA's SAS.</span></span> <span data-ttu-id="d70ca-114">Esse processamento geralmente inclui chamadas para as funções de processamento SAS da GINA.</span><span class="sxs-lookup"><span data-stu-id="d70ca-114">This processing usually includes calls to the GINA's SAS processing functions.</span></span>

<span data-ttu-id="d70ca-115">Para obter informações sobre funções de exportação de GINA específicas, consulte [funções de exportação de Gina](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d70ca-115">For information about specific GINA export functions, see [GINA Export Functions](authentication-functions.md).</span></span> <span data-ttu-id="d70ca-116">Para obter informações sobre como usar estruturas GINA para passar informações, consulte [estruturas Gina](authentication-structures.md).</span><span class="sxs-lookup"><span data-stu-id="d70ca-116">For information about using GINA structures to pass information, see [GINA Structures](authentication-structures.md).</span></span>



| <span data-ttu-id="d70ca-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="d70ca-117">Topic</span></span>                                                                             | <span data-ttu-id="d70ca-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d70ca-118">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="d70ca-119">Carregando e executando uma DLL GINA</span><span class="sxs-lookup"><span data-stu-id="d70ca-119">Loading and Running a GINA DLL</span></span>](loading-and-running-a-gina-dll.md)<br/>   | <span data-ttu-id="d70ca-120">Qual valor da chave do registro a ser alterado para carregar e executar uma DLL GINA personalizada.</span><span class="sxs-lookup"><span data-stu-id="d70ca-120">Which registry key value to alter to load and run a custom GINA DLL.</span></span><br/> |
| [<span data-ttu-id="d70ca-121">Criando e testando uma DLL GINA</span><span class="sxs-lookup"><span data-stu-id="d70ca-121">Building and Testing a GINA DLL</span></span>](building-and-testing-a-gina-dll.md)<br/> | <span data-ttu-id="d70ca-122">Como testar uma DLL GINA.</span><span class="sxs-lookup"><span data-stu-id="d70ca-122">How to test a GINA DLL.</span></span><br/>                                              |



 

 

