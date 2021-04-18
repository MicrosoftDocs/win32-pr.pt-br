---
description: Visão geral da API de controles dos pais
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Visão geral da API de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105815444"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="0ced0-103">Visão geral da API de controles dos pais</span><span class="sxs-lookup"><span data-stu-id="0ced0-103">Parental Controls API Overview</span></span>

<span data-ttu-id="0ced0-104">As APIs usadas para controles dos pais expõem as configurações de diretiva e restrições integradas e o registro em log da funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="0ced0-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="0ced0-105">Configurações</span><span class="sxs-lookup"><span data-stu-id="0ced0-105">Settings</span></span>

<span data-ttu-id="0ced0-106">São fornecidas duas APIs públicas:</span><span class="sxs-lookup"><span data-stu-id="0ced0-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="0ced0-107">Uma API de conformidade mínima com base em COM baseada em COM (chamada de API de conformidade), principalmente para aplicativos, para determinar se o log deve ser ativado.</span><span class="sxs-lookup"><span data-stu-id="0ced0-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="0ced0-108">Além disso, métodos simples são fornecidos para:</span><span class="sxs-lookup"><span data-stu-id="0ced0-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="0ced0-109">Recuperando o estado de restrições para restrições da Web, limites de tempo, restrições de jogos e restrições de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0ced0-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="0ced0-110">Recuperando a ID do filtro de conteúdo da Web ativo.</span><span class="sxs-lookup"><span data-stu-id="0ced0-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="0ced0-111">Determinar se os elementos da interface do usuário do fornecedor devem ser mostrados, de maneira consistente com a ocultação da caixa quando ingressado em um domínio.</span><span class="sxs-lookup"><span data-stu-id="0ced0-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="0ced0-112">Recuperando a última vez que uma configuração foi alterada para um usuário.</span><span class="sxs-lookup"><span data-stu-id="0ced0-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="0ced0-113">Recuperar se os downloads de arquivos baseados em navegador ou navegadores precisam ser bloqueados para um usuário e a capacidade de solicitar uma URL para ser especificamente permitida pelo filtro de conteúdo da Web para esse usuário.</span><span class="sxs-lookup"><span data-stu-id="0ced0-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="0ced0-114">Determinando se um determinado jogo está bloqueado para um usuário.</span><span class="sxs-lookup"><span data-stu-id="0ced0-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="0ced0-115">Acesso à API de Instrumentação de Gerenciamento do Windows (WMI) a um namespace de controles pai para gravação completa e acesso de leitura a todas as configurações expostas.</span><span class="sxs-lookup"><span data-stu-id="0ced0-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="0ced0-116">Os controles dos pais implantam um provedor WMI para gerenciar permissões de leitura/gravação no armazenamento de configurações subjacente com a aplicação adequada de privilégios para administradores e usuários controlados.</span><span class="sxs-lookup"><span data-stu-id="0ced0-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="0ced0-117">Os ISVs são solicitados a usar a API de conformidade e a API do WMI, conforme necessário, para controlar as restrições conforme apropriado para a segurança filho com base na funcionalidade do aplicativo ou da solução.</span><span class="sxs-lookup"><span data-stu-id="0ced0-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="0ced0-118">Log</span><span class="sxs-lookup"><span data-stu-id="0ced0-118">Logging</span></span>

-   <span data-ttu-id="0ced0-119">A publicação de eventos padrão do Windows e as APIs de consumo são usadas para monitoramento de atividades de controles dos pais.</span><span class="sxs-lookup"><span data-stu-id="0ced0-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="0ced0-120">O sistema de relatório e rastreamento de eventos do Windows Vista aprimorou o desempenho da funcionalidade ETW (rastreamento de eventos anterior para Windows).</span><span class="sxs-lookup"><span data-stu-id="0ced0-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="0ced0-121">Os controles dos pais definem um canal exclusivo para seus dados no ETW.</span><span class="sxs-lookup"><span data-stu-id="0ced0-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="0ced0-122">Os ISVs são solicitados a usar a API de publicação de eventos para registrar a atividade do usuário, conforme especificado na seção usando APIs de controles pais.</span><span class="sxs-lookup"><span data-stu-id="0ced0-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



