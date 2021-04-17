---
title: Diretrizes para gravar DLLs EAP
description: As DLLs ou plug-ins de EAP podem ser escritos para otimizar seu desempenho em diferentes cenários.
ms.assetid: 79b9bc54-6eb0-4e01-822e-af83fc475ec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdc2d437df61811e6fb24b3a9b4ff406ced4905
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105791607"
---
# <a name="guidelines-for-writing-eap-dlls"></a><span data-ttu-id="37aaa-103">Diretrizes para gravar DLLs EAP</span><span class="sxs-lookup"><span data-stu-id="37aaa-103">Guidelines for Writing EAP DLLs</span></span>

<span data-ttu-id="37aaa-104">As DLLs ou plug-ins de EAP podem ser escritos para otimizar seu desempenho em diferentes cenários.</span><span class="sxs-lookup"><span data-stu-id="37aaa-104">EAP DLLs or Plug-ins can be written to optimize their performance in different scenarios.</span></span>

## <a name="general-guidelines"></a><span data-ttu-id="37aaa-105">Diretrizes gerais</span><span class="sxs-lookup"><span data-stu-id="37aaa-105">General Guidelines</span></span>

-   <span data-ttu-id="37aaa-106">Para criar uma conexão criptografada, os plug-ins EAP devem gerar chaves de criptografia e retorná-las por meio dos atributos RADIUS específicos do fornecedor da Microsoft MS-MPPE-Send-Keys e MS-MPPE-recv-Keys.</span><span class="sxs-lookup"><span data-stu-id="37aaa-106">In order to create an encrypted connection, EAP plug-ins must generate encryption keys and return them through the Microsoft vendor-specific RADIUS Attributes MS-MPPE-Send-Keys and MS-MPPE-Recv-Keys.</span></span> <span data-ttu-id="37aaa-107">Consulte a seção comentários na [**\_ \_ saída do PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="37aaa-107">See the Remarks section in [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) for more information.</span></span>

## <a name="wireless-guidelines"></a><span data-ttu-id="37aaa-108">Diretrizes sem fio</span><span class="sxs-lookup"><span data-stu-id="37aaa-108">Wireless Guidelines</span></span>

<span data-ttu-id="37aaa-109">Veja a seguir as diretrizes e recomendações para a gravação de um plug-in EAP que dá suporte à autenticação de computadores em cenários sem fio (802.1 X).</span><span class="sxs-lookup"><span data-stu-id="37aaa-109">The following are guidelines and recommendations for writing an EAP Plug-in that supports authenticating machines in wireless (802.1X) scenarios.</span></span> <span data-ttu-id="37aaa-110">Esta seção não se aplica a cenários de VPN e dial-up.</span><span class="sxs-lookup"><span data-stu-id="37aaa-110">This section does not apply to VPN and Dial-up scenarios.</span></span>

-   <span data-ttu-id="37aaa-111">Para não bloquear a execução de sistemas autônomos, os plug-ins EAP não devem fazer nenhuma chamada de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="37aaa-111">In order not to block unattended systems' execution, EAP plug-ins must not make any user interface calls.</span></span>
-   <span data-ttu-id="37aaa-112">A implementação do plug-in do EAP da etapa de autenticação do computador deve ser concluída o mais rapidamente possível para que não atrapalhe a inicialização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="37aaa-112">The EAP Plug-in implementation of the machine authentication step must complete as quickly as possible so it does not hinder operating system startup.</span></span>
    > [!Note]  
    > <span data-ttu-id="37aaa-113">Se o protocolo EAP não oferecer suporte à autenticação de computador, ele deverá verificar o sinalizador de autenticação do computador, o **sinalizador de EAP do RAS \_ \_ \_ \_ auth Authentication** usado no campo **fFlags** na [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input)e retornar um erro.</span><span class="sxs-lookup"><span data-stu-id="37aaa-113">If your EAP protocol does not support machine authentication, it must check for the machine authentication flag, **RAS\_EAP\_FLAG\_MACHINE\_AUTH** used in the **fFlags** field in [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input), and return an error.</span></span>

     

 

 




