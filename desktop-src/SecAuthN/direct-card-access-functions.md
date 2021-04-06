---
description: Usando o subsistema de cartão inteligente, você pode se comunicar com cartões que podem não estar em conformidade com as especificações ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funções de acesso de cartão direto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826822"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="be893-103">Funções de acesso de cartão direto</span><span class="sxs-lookup"><span data-stu-id="be893-103">Direct Card Access Functions</span></span>

<span data-ttu-id="be893-104">Usando o subsistema de [*cartão inteligente*](/windows/desktop/SecGloss/s-gly) , você pode se comunicar com cartões que podem não estar em conformidade com as especificações ISO 7816.</span><span class="sxs-lookup"><span data-stu-id="be893-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="be893-105">Para fazer isso, as funções a seguir permitem controlar os atributos das comunicações entre o aplicativo e o cartão fornecendo uma manipulação direta e de baixo nível do [*leitor*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="be893-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="be893-106">Para usar essas funções, você precisa fornecer um identificador para o atributo em questão.</span><span class="sxs-lookup"><span data-stu-id="be893-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="be893-107">Para obter os identificadores de atributo e valores válidos, consulte a tabela 3-1 em *requisitos para dispositivos de Interface PC-Connected*.</span><span class="sxs-lookup"><span data-stu-id="be893-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="be893-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="be893-108">Topic</span></span>                                    | <span data-ttu-id="be893-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="be893-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="be893-110">**SCardControl**</span><span class="sxs-lookup"><span data-stu-id="be893-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="be893-111">Forneça controle direto do leitor.</span><span class="sxs-lookup"><span data-stu-id="be893-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="be893-112">**SCardGetAttrib**</span><span class="sxs-lookup"><span data-stu-id="be893-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="be893-113">Obter atributos de leitor.</span><span class="sxs-lookup"><span data-stu-id="be893-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="be893-114">**SCardSetAttrib**</span><span class="sxs-lookup"><span data-stu-id="be893-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="be893-115">Definir atributo de leitor.</span><span class="sxs-lookup"><span data-stu-id="be893-115">Set reader attribute.</span></span>                 |



 

 

 
