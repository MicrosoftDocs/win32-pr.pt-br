---
description: Usando APIs de controles dos pais
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Usando APIs de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812106"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="75353-103">Usando APIs de controles dos pais</span><span class="sxs-lookup"><span data-stu-id="75353-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="75353-104">Seleção de API</span><span class="sxs-lookup"><span data-stu-id="75353-104">API Selection</span></span>

<span data-ttu-id="75353-105">Conforme observado na seção de visão geral, o desenvolvimento envolve o uso de até três APIs:</span><span class="sxs-lookup"><span data-stu-id="75353-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="75353-106">Acesso às configurações básicas: a API de COM de conformidade mínima do controla os pais (API de conformidade) definida em Wpcapi. h para acesso simples a um subconjunto de chaves do estado dos controles dos pais.</span><span class="sxs-lookup"><span data-stu-id="75353-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="75353-107">Configurações completas acesso de gravação/leitura: o uso de um pequeno subconjunto da API COM do WMI para acesso completo só será necessário se o ISV precisar modificar as configurações.</span><span class="sxs-lookup"><span data-stu-id="75353-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="75353-108">A adição de um link de extensibilidade da interface do usuário, a substituição do filtro de conteúdo da Web ou adições ao aplicativo HTTP em todo o computador ou às listas de isenção de filtragem de URL são as principais razões para usar a API.</span><span class="sxs-lookup"><span data-stu-id="75353-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="75353-109">Como o uso do namespace de controles pai do WMI fornece acesso bruto ao armazenamento de configurações subjacentes, os ISVs devem prosseguir com cuidado ao interpretar o estado de configurações individuais que, de fato, podem ter dependências em outras configurações.</span><span class="sxs-lookup"><span data-stu-id="75353-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="75353-110">Portanto, é recomendável usar a API de conformidade para o estado de leitura de todos os valores expostos por essa API.</span><span class="sxs-lookup"><span data-stu-id="75353-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="75353-111">Registro em log: o rastreamento de eventos do Windows Vista e a API do sistema de relatórios (também conhecida como ETW) para publicar eventos de atividade nos logs de controles dos pais, em conjunto com descritores de eventos e enumerações de matriz definidas em WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="75353-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="75353-112">Todas as APIs são chamáveis como usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="75353-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="75353-113">Para registro em log, qualquer usuário pode registrar eventos de log.</span><span class="sxs-lookup"><span data-stu-id="75353-113">For logging, any user may source log events.</span></span> <span data-ttu-id="75353-114">A chamada para recuperar ou alterar as configurações de outro usuário falhará se o chamador não tiver privilégios de administrador.</span><span class="sxs-lookup"><span data-stu-id="75353-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="75353-115">Em outras palavras, um usuário padrão pode acessar suas próprias configurações apenas e apenas para leitura.</span><span class="sxs-lookup"><span data-stu-id="75353-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="75353-116">As configurações e o uso de API de registro em log são discutidos mais detalhadamente nestas seções</span><span class="sxs-lookup"><span data-stu-id="75353-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="75353-117">Usando APIs de configurações de controles pais</span><span class="sxs-lookup"><span data-stu-id="75353-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="75353-118">Usando APIs de log para controles dos pais</span><span class="sxs-lookup"><span data-stu-id="75353-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="75353-119">Ambiente de desenvolvimento</span><span class="sxs-lookup"><span data-stu-id="75353-119">Development Environment</span></span>

<span data-ttu-id="75353-120">O desenvolvimento para controles dos pais requer acesso a três arquivos de cabeçalho: WPC. h, WpcApi. h e WpcEvent. h.</span><span class="sxs-lookup"><span data-stu-id="75353-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="75353-121">WPC. h é um coletor que inclui as configurações de API de conformidade pública e cabeçalhos de eventos, portanto, é suficiente incluir WPC. h no código do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="75353-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="75353-122">Permissões de leitura/gravação para a API do WMI são especificadas pelo arquivo Wpcsprov. mof.</span><span class="sxs-lookup"><span data-stu-id="75353-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="75353-123">Esse arquivo é instalado no subdiretório WBEM no diretório system32 do Windows.</span><span class="sxs-lookup"><span data-stu-id="75353-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="75353-124">O SDK (Software Development Kit) do Microsoft Windows contém um código de exemplo para reforçar o código de exemplo mostrado aqui e fornecer ferramentas simples orientadas por linha de comando para exploração de API ou testes de integração.</span><span class="sxs-lookup"><span data-stu-id="75353-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 



