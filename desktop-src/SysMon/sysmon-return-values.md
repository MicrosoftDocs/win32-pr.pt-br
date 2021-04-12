---
title: Valores de retorno de SYSMON
description: A seguir está uma lista de valores de retorno do monitor do sistema que são definidos em Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366429"
---
# <a name="sysmon-return-values"></a><span data-ttu-id="84181-103">Valores de retorno de SYSMON</span><span class="sxs-lookup"><span data-stu-id="84181-103">SYSMON Return Values</span></span>

<span data-ttu-id="84181-104">A seguir está uma lista de valores de retorno do monitor do sistema que são definidos em Smonmsg. h.</span><span class="sxs-lookup"><span data-stu-id="84181-104">The following is a list of the System Monitor return values that are defined in Smonmsg.h.</span></span>



| <span data-ttu-id="84181-105">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="84181-105">Return value</span></span>                                       | <span data-ttu-id="84181-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="84181-106">Description</span></span>                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84181-107">SMON \_ status \_ DUPL \_ \_ caminho do contador (0xC0001388)</span><span class="sxs-lookup"><span data-stu-id="84181-107">SMON\_STATUS\_DUPL\_COUNTER\_PATH (0xC0001388)</span></span>     | <span data-ttu-id="84181-108">A coleção de contadores já contém o contador especificado.</span><span class="sxs-lookup"><span data-stu-id="84181-108">The counter collection already contains the specified counter.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="84181-109">\_Status \_ do SMON no \_ \_ objeto SYSMON (0xC0001389)</span><span class="sxs-lookup"><span data-stu-id="84181-109">SMON\_STATUS\_NO\_SYSMON\_OBJECT (0xC0001389)</span></span>      | <span data-ttu-id="84181-110">As configurações não contêm nenhum objeto HTML do monitor de sistema completo.</span><span class="sxs-lookup"><span data-stu-id="84181-110">The settings do not contain any complete System Monitor HTML objects.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="84181-111">SMON \_ o \_ status \_ \_ de poucas amostras (0xC000138A)</span><span class="sxs-lookup"><span data-stu-id="84181-111">SMON\_STATUS\_TOO\_FEW\_SAMPLES (0xC000138A)</span></span>       | <span data-ttu-id="84181-112">O arquivo de log especificado contém menos de dois exemplos de dados.</span><span class="sxs-lookup"><span data-stu-id="84181-112">The specified log file contains fewer than two data samples.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="84181-113">\_ \_ \_ \_ \_ Limite de tamanho do arquivo de log de status SMON (0xC000138B)</span><span class="sxs-lookup"><span data-stu-id="84181-113">SMON\_STATUS\_LOG\_FILE\_SIZE\_LIMIT (0xC000138B)</span></span>  | <span data-ttu-id="84181-114">O arquivo de log especificado excede os limites de tamanho do controle do monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="84181-114">The specified log file exceeds the size limits of the System Monitor control.</span></span> <span data-ttu-id="84181-115">Se um arquivo de log estiver selecionado no momento, selecione atividade atual como a fonte de dados para descarregar o arquivo de log atual e, em seguida, selecione novamente o arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="84181-115">If a log file is currently selected, select current activity as the data source in order to unload the current log file, then reselect the specified log file.</span></span> |
| <span data-ttu-id="84181-116">\_ \_ \_ \_ \_ Fonte de dados do arquivo de log de status SMON (0xC000138C)</span><span class="sxs-lookup"><span data-stu-id="84181-116">SMON\_STATUS\_LOG\_FILE\_DATA\_SOURCE (0xC000138C)</span></span> | <span data-ttu-id="84181-117">Para adicionar um novo arquivo de log à fonte de dados, o tipo de fonte de dados deve ser alterado para um tipo diferente de sysmonLogFiles.</span><span class="sxs-lookup"><span data-stu-id="84181-117">To add a new log file to the data source, the data source type must be changed to a type other than sysmonLogFiles.</span></span>                                                                                                                          |
| <span data-ttu-id="84181-118">SMON \_ status \_ DUPL \_ log \_ File \_ Path (0xC000138D)</span><span class="sxs-lookup"><span data-stu-id="84181-118">SMON\_STATUS\_DUPL\_LOG\_FILE\_PATH (0xC000138D)</span></span>   | <span data-ttu-id="84181-119">A coleção de arquivos de log já contém o arquivo de log especificado.</span><span class="sxs-lookup"><span data-stu-id="84181-119">The log file collection already contains the specified log file.</span></span>                                                                                                                                                                             |



 

<span data-ttu-id="84181-120">Para obter uma descrição de valores de retorno adicionais retornados pelo monitor do sistema, consulte códigos de [erro do sistema](/windows/desktop/Debug/system-error-codes) e [códigos de erro auxiliares de dados de desempenho](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span><span class="sxs-lookup"><span data-stu-id="84181-120">For a description of additional return values returned by System Monitor, see [System Error Codes](/windows/desktop/Debug/system-error-codes) and [Performance Data Helper Error Codes](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).</span></span>

 

 