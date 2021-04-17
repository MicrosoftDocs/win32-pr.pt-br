---
title: Conexões Multilink e de retorno de chamada
description: Para o primeiro link em uma conexão de vínculos múltiplos, o serviço de autenticação define o sinalizador de \_ vínculo do sinalizador EAP RAS \_ \_ primeiro \_ no membro fFlags da \_ estrutura de entrada PPP EAP \_ .
ms.assetid: a6aee73b-43b2-43b4-a6f1-ac7b293c44ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af39ebfa54469e2f44c44c800cebbfb176b33cad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105780339"
---
# <a name="multilink-and-callback-connections"></a><span data-ttu-id="8c305-103">Conexões Multilink e de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="8c305-103">Multilink and Callback Connections</span></span>

<span data-ttu-id="8c305-104">Para o primeiro link em uma conexão de vínculos múltiplos, o serviço de autenticação define o sinalizador de \_ vínculo do sinalizador EAP RAS \_ \_ primeiro \_ no membro **FFlags** da estrutura de [**\_ \_ entrada PPP EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) .</span><span class="sxs-lookup"><span data-stu-id="8c305-104">For the first link in a multilink connection, the authentication service sets the RAS\_EAP\_FLAG\_FIRST\_LINK flag in the **fFlags** member of the [**PPP\_EAP\_INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) structure.</span></span> <span data-ttu-id="8c305-105">O protocolo de autenticação pode usar a presença desse sinalizador para determinar se deve apresentar uma interface do usuário especificamente para o primeiro link de uma conexão de vínculos múltiplos.</span><span class="sxs-lookup"><span data-stu-id="8c305-105">The authentication protocol can use the presence of this flag to determine whether to present a user interface specifically for the first link of a multilink connection.</span></span>

<span data-ttu-id="8c305-106">Se a conexão estiver configurada para que o servidor chame de volta o computador cliente, o sinalizador de \_ \_ primeiro link do sinalizador EAP RAS \_ \_ não será definido no retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8c305-106">If the connection is configured so that the server calls back the client computer, the RAS\_EAP\_FLAG\_FIRST\_LINK flag will not be set on the callback.</span></span>

<span data-ttu-id="8c305-107">Se o protocolo de autenticação definir o membro **fSaveConnectionData** da [**saída do PPP \_ \_ EAP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) como **true**, os links subsequentes na conexão Multilink receberão os novos dados específicos da conexão.</span><span class="sxs-lookup"><span data-stu-id="8c305-107">If the authentication protocol sets the **fSaveConnectionData** member of [**PPP\_EAP\_OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) to **TRUE**, subsequent links in the multilink connection receive the new connection-specific data.</span></span> <span data-ttu-id="8c305-108">No caso de dados específicos do usuário, no entanto, o protocolo de autenticação continua a obter os dados originais específicos do usuário, mesmo que ele defina o membro **fSaveUserData** da **saída do PPP \_ \_ EAP** como **true**.</span><span class="sxs-lookup"><span data-stu-id="8c305-108">In the case of user-specific data, however, the authentication protocol continues to get the original user-specific data even if it sets the **fSaveUserData** member of **PPP\_EAP\_OUTPUT** to **TRUE**.</span></span>

<span data-ttu-id="8c305-109">O protocolo de autenticação pode usar uma [interface do usuário interativa](interactive-user-interface.md) para coletar dados de um link específico de uma conexão de vínculos múltiplos.</span><span class="sxs-lookup"><span data-stu-id="8c305-109">The authentication protocol may use an [interactive user interface](interactive-user-interface.md) to collect data for a particular link of a multilink connection.</span></span> <span data-ttu-id="8c305-110">Nesse caso, o serviço de autenticação disponibiliza os dados resultantes para o protocolo de autenticação durante os links subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8c305-110">In this case, the authentication service makes the resulting data available to the authentication protocol during subsequent links.</span></span> <span data-ttu-id="8c305-111">No entanto, esses dados nunca são salvos no armazenamento persistente.</span><span class="sxs-lookup"><span data-stu-id="8c305-111">However, this data is never saved to persistent storage.</span></span>

 

 




