---
description: Esta seção fornece uma lista dos códigos de retorno do WMI, constantes simbólicas, valores literais e descrições. Esses códigos podem ser retornados por scripts, aplicativos C++ ou comandos WMIC.
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: Códigos de retorno do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e05455b109bd05b7a1693b8a05b13f6f7aeb646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781200"
---
# <a name="wmi-return-codes"></a><span data-ttu-id="ec7f2-104">Códigos de retorno do WMI</span><span class="sxs-lookup"><span data-stu-id="ec7f2-104">WMI Return Codes</span></span>

<span data-ttu-id="ec7f2-105">Esta seção fornece uma lista dos códigos de retorno do WMI, constantes simbólicas, valores literais e descrições.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-105">This section provides a list of the WMI return codes, symbolic constants, literal values, and descriptions.</span></span> <span data-ttu-id="ec7f2-106">Esses códigos podem ser retornados por scripts, aplicativos C++ ou comandos [**WMIC**](wmic.md) .</span><span class="sxs-lookup"><span data-stu-id="ec7f2-106">These codes may be returned by scripts, C++ applications, or [**Wmic**](wmic.md) commands.</span></span>

<span data-ttu-id="ec7f2-107">Se ocorrer um erro, o WMI retornará um dos seguintes códigos de erro como um valor de 32 bits, em que os dois bits de ordem superior indicam o código de severidade da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-107">If an error occurs, WMI returns one of the following error codes as a 32-bit value where the two high-order bits indicate the severity code of the message.</span></span>

<dl> <dt>

<span data-ttu-id="ec7f2-108"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="ec7f2-108"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="ec7f2-109">Êxito</span><span class="sxs-lookup"><span data-stu-id="ec7f2-109">Success</span></span>

</dd> <dt>

<span data-ttu-id="ec7f2-110"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="ec7f2-110"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="ec7f2-111">Informativo</span><span class="sxs-lookup"><span data-stu-id="ec7f2-111">Informational</span></span>

</dd> <dt>

<span data-ttu-id="ec7f2-112"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="ec7f2-112"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="ec7f2-113">Aviso</span><span class="sxs-lookup"><span data-stu-id="ec7f2-113">Warning</span></span>

</dd> <dt>

<span data-ttu-id="ec7f2-114"><span id="3"></span>Beta</span><span class="sxs-lookup"><span data-stu-id="ec7f2-114"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="ec7f2-115">Erro</span><span class="sxs-lookup"><span data-stu-id="ec7f2-115">Error</span></span>

</dd> </dl>

> [!Note]
>
> <span data-ttu-id="ec7f2-116">Se o WMI retornar mensagens de erro, lembre-se de que eles podem não indicar problemas no serviço WMI ou em provedores WMI.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-116">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="ec7f2-117">As falhas podem se originar em outras partes do sistema operacional e surgir como erros por meio do WMI.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-117">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="ec7f2-118">Em qualquer circunstância, não exclua o repositório WMI como uma primeira ação, pois a exclusão do repositório pode causar danos ao sistema ou aos aplicativos instalados.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-118">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="ec7f2-119">Para obter mais informações sobre a origem do problema, você pode baixar e executar a ferramenta de linha de comando de diagnóstico [Utilitário de diagnóstico WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="ec7f2-119">To obtain more information about the source of the problem, you can download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="ec7f2-120">Essa ferramenta produz um relatório que, em geral, pode isolar a origem do problema e fornecer instruções sobre como corrigi-lo.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-120">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="ec7f2-121">O relatório também ajuda os serviços de suporte da Microsoft para ajudá-lo.</span><span class="sxs-lookup"><span data-stu-id="ec7f2-121">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="ec7f2-122">Você pode baixar o Utilitário de Diagnóstico WMI [aqui](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="ec7f2-122">You can download the WMI Diagnosis Utility [here](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

-   [<span data-ttu-id="ec7f2-123">**Constantes de erro WMI**</span><span class="sxs-lookup"><span data-stu-id="ec7f2-123">**WMI Error Constants**</span></span>](wmi-error-constants.md)
-   [<span data-ttu-id="ec7f2-124">**Constantes de não erro do WMI**</span><span class="sxs-lookup"><span data-stu-id="ec7f2-124">**WMI Non-Error Constants**</span></span>](wmi-non-error-constants.md)

 

 



