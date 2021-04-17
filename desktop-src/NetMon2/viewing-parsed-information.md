---
description: O Visualizador de quadros Monitor de Rede exibe dados analisados em três painéis.
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: Exibindo informações analisadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557312"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="d75d5-103">Exibindo informações analisadas</span><span class="sxs-lookup"><span data-stu-id="d75d5-103">Viewing Parsed Information</span></span>

<span data-ttu-id="d75d5-104">O Visualizador de quadros Monitor de Rede exibe dados analisados em três painéis.</span><span class="sxs-lookup"><span data-stu-id="d75d5-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="d75d5-105">O painel superior exibe um resumo do quadro que inclui o protocolo identificado.</span><span class="sxs-lookup"><span data-stu-id="d75d5-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="d75d5-106">O painel central exibe as propriedades de dados formatados que podem ser organizadas hierarquicamente como parte da exibição do analisador.</span><span class="sxs-lookup"><span data-stu-id="d75d5-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="d75d5-107">O painel inferior exibe dados brutos realçados selecionados no painel central.</span><span class="sxs-lookup"><span data-stu-id="d75d5-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="d75d5-108">Você pode especificar como as informações no visualizador são exibidas quando você desenvolve seu próprio analisador.</span><span class="sxs-lookup"><span data-stu-id="d75d5-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="d75d5-109">A ilustração a seguir mostra como as informações podem ser exibidas no Visualizador de quadros Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="d75d5-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![Visualizador de quadros do monitor de rede](images/parseui.png)

> [!Note]  
> <span data-ttu-id="d75d5-111">Os analisadores não exibem quadros.</span><span class="sxs-lookup"><span data-stu-id="d75d5-111">Parsers do not display frames.</span></span> <span data-ttu-id="d75d5-112">Os analisadores reconhecem os campos nas informações fornecidas e, em seguida, notificam Monitor de Rede para exibir o quadro.</span><span class="sxs-lookup"><span data-stu-id="d75d5-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="d75d5-113">A filtragem é uma operação de nível superior que permite filtrar consultas para abranger analisadores.</span><span class="sxs-lookup"><span data-stu-id="d75d5-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="d75d5-114">No analisador, use apenas as funções que podem ser executadas em aplicativos Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="d75d5-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="d75d5-115">Antes de anexar Propriedades aos dados brutos, um analisador deve primeiro registrar todas as propriedades possíveis com o kernel Monitor de Rede.</span><span class="sxs-lookup"><span data-stu-id="d75d5-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="d75d5-116">O analisador envia uma mensagem ao kernel para criar um banco de dados de propriedade e, em seguida, preenche o banco de dados de propriedades com cada propriedade possível para seu protocolo.</span><span class="sxs-lookup"><span data-stu-id="d75d5-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="d75d5-117">Cada propriedade no banco de dados de propriedades contém informações como uma descrição textual, um tipo de dado e um qualificador que são usados para formatar os dados brutos e uma rotina de formatação usada para exibir os dados.</span><span class="sxs-lookup"><span data-stu-id="d75d5-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 



