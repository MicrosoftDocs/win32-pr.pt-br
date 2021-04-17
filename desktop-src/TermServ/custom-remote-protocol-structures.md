---
title: Estruturas de provedor de protocolo RDP
description: A API de protocolo remoto personalizada oferece suporte às seguintes estruturas.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783344"
---
# <a name="remote-desktop-protocol-provider-structures"></a><span data-ttu-id="8e216-103">Estruturas de provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="8e216-103">Remote Desktop Protocol Provider Structures</span></span>

<span data-ttu-id="8e216-104">A API de protocolo remoto personalizada oferece suporte às seguintes estruturas.</span><span class="sxs-lookup"><span data-stu-id="8e216-104">The custom remote protocol API supports the following structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8e216-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8e216-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="8e216-106">**\_ \_ dados de suporte \_ do TSMF em**</span><span class="sxs-lookup"><span data-stu-id="8e216-106">**TSMF\_SUPPORT\_DATA\_IN**</span></span>](tsmf-support-data-in.md)
</dt> <dd>

<span data-ttu-id="8e216-107">Contém informações sobre formatos de mídia.</span><span class="sxs-lookup"><span data-stu-id="8e216-107">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-108">**\_saída de \_ dados de suporte do TSMF \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-108">**TSMF\_SUPPORT\_DATA\_OUT**</span></span>](tsmf-support-data-out.md)
</dt> <dd>

<span data-ttu-id="8e216-109">Contém informações sobre formatos de mídia.</span><span class="sxs-lookup"><span data-stu-id="8e216-109">Contains information about media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-110">**TSMF \_ suportam \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-110">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> <dd>

<span data-ttu-id="8e216-111">Usado dentro dos [**dados de suporte do TSMF \_ \_ \_ na**](tsmf-support-data-in.md) estrutura para conter informações sobre formatos de mídia com suporte.</span><span class="sxs-lookup"><span data-stu-id="8e216-111">Used inside the [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-112">**TSMF \_ suporte \_ NODEDATA \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-112">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> <dd>

<span data-ttu-id="8e216-113">Usado na estrutura [**de \_ \_ \_ saída de dados de suporte do TSMF**](tsmf-support-data-out.md) para conter informações sobre formatos de mídia com suporte.</span><span class="sxs-lookup"><span data-stu-id="8e216-113">Used inside the [**TSMF\_SUPPORT\_DATA\_OUT**](tsmf-support-data-out.md) structure to contain information about supported media formats.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-114">**\_configurações de conexão do WRDS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-114">**WRDS\_CONNECTION\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

<span data-ttu-id="8e216-115">Contém informações de configuração de conexão para uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-115">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-116">**Configurações de conexão do WRDS \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8e216-116">**WRDS\_CONNECTION\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

<span data-ttu-id="8e216-117">Contém informações de configuração de conexão para uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-117">Contains connection setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-118">**\_informações de \_ \_ fuso horário dinâmico do \_ WRDS**</span><span class="sxs-lookup"><span data-stu-id="8e216-118">**WRDS\_DYNAMIC\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

<span data-ttu-id="8e216-119">Contém informações de fuso horário dinâmico.</span><span class="sxs-lookup"><span data-stu-id="8e216-119">Contains dynamic time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-120">**\_configurações do ouvinte WRDS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-120">**WRDS\_LISTENER\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

<span data-ttu-id="8e216-121">Contém informações de configuração de ouvinte para uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-121">Contains listener setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-122">**\_Configurações do ouvinte WRDS \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8e216-122">**WRDS\_LISTENER\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

<span data-ttu-id="8e216-123">Contém configurações de ouvinte para uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-123">Contains listener settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-124">**configurações de WRDS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-124">**WRDS\_SETTINGS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

<span data-ttu-id="8e216-125">Contém informações de configuração relacionadas à política para uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-125">Contains policy-related setting information for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-126">**Configurações de WRDS \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="8e216-126">**WRDS\_SETTINGS\_1**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

<span data-ttu-id="8e216-127">Contém configurações relacionadas à política para uma sessão remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-127">Contains policy-related settings for a remote session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-128">**\_Estatísticas de cache WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-128">**WTS\_CACHE\_STATS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

<span data-ttu-id="8e216-129">Contém estatísticas de cache de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e216-129">Contains protocol cache statistics.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-130">**WTS \_ Exibir \_ IOCTL**</span><span class="sxs-lookup"><span data-stu-id="8e216-130">**WTS\_DISPLAY\_IOCTL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

<span data-ttu-id="8e216-131">Contém informações sobre a exibição do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e216-131">Contains information about the client display.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-132">**\_dados do cliente WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-132">**WTS\_CLIENT\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

<span data-ttu-id="8e216-133">Contém informações sobre a conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e216-133">Contains information about the client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-134">**\_recursos de licença do WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-134">**WTS\_LICENSE\_CAPABILITIES**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

<span data-ttu-id="8e216-135">Contém informações sobre os recursos de licenciamento do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e216-135">Contains information about the licensing capabilities of the client.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-136">**\_dados de política WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-136">**WTS\_POLICY\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

<span data-ttu-id="8e216-137">Contém informações de política que são passadas pelo serviço de Serviços de Área de Trabalho Remota para o protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e216-137">Contains policy information that is passed by the Remote Desktop Services service to the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-138">**\_valor da propriedade WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-138">**WTS\_PROPERTY\_VALUE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

<span data-ttu-id="8e216-139">Contém informações sobre um valor de propriedade a ser recuperado do protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e216-139">Contains information about a property value to retrieve from the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-140">**\_cache de protocolo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-140">**WTS\_PROTOCOL\_CACHE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

<span data-ttu-id="8e216-141">Contém o número de leituras de cache e acertos de cache.</span><span class="sxs-lookup"><span data-stu-id="8e216-141">Contains the number of cache reads and cache hits.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-142">**\_contadores de protocolo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-142">**WTS\_PROTOCOL\_COUNTERS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

<span data-ttu-id="8e216-143">Contém contadores de desempenho de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e216-143">Contains protocol performance counters.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-144">**\_status do protocolo WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-144">**WTS\_PROTOCOL\_STATUS**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

<span data-ttu-id="8e216-145">Contém informações sobre o status do protocolo.</span><span class="sxs-lookup"><span data-stu-id="8e216-145">Contains information about the status of the protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-146">**\_estado do serviço WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-146">**WTS\_SERVICE\_STATE**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

<span data-ttu-id="8e216-147">Contém informações sobre as alterações no estado do serviço de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="8e216-147">Contains information about changes in the state of the Remote Desktop Services service.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-148">**\_ID da sessão WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-148">**WTS\_SESSION\_ID**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

<span data-ttu-id="8e216-149">Contém um **GUID** que identifica exclusivamente uma sessão.</span><span class="sxs-lookup"><span data-stu-id="8e216-149">Contains a **GUID** that uniquely identifies a session.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-150">**\_Rect WTS pequeno \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-150">**WTS\_SMALL\_RECT**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

<span data-ttu-id="8e216-151">Contém coordenadas da janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e216-151">Contains client window coordinates.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-152">**WTS \_ SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="8e216-152">**WTS\_SOCKADDR**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

<span data-ttu-id="8e216-153">Contém um endereço de soquete.</span><span class="sxs-lookup"><span data-stu-id="8e216-153">Contains a socket address.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-154">**WTS \_ SYSTEMTIME**</span><span class="sxs-lookup"><span data-stu-id="8e216-154">**WTS\_SYSTEMTIME**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

<span data-ttu-id="8e216-155">Especifica informações de data e hora para transições entre hora padrão e horário de verão.</span><span class="sxs-lookup"><span data-stu-id="8e216-155">Specifies date and time information for transitions between standard time and daylight saving time.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-156">**\_informações de \_ fuso \_ horário do WTS**</span><span class="sxs-lookup"><span data-stu-id="8e216-156">**WTS\_TIME\_ZONE\_INFORMATION**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

<span data-ttu-id="8e216-157">Contém informações de fuso horário do cliente.</span><span class="sxs-lookup"><span data-stu-id="8e216-157">Contains client time zone information.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-158">**\_credencial de usuário WTS \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-158">**WTS\_USER\_CREDENTIAL**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

<span data-ttu-id="8e216-159">Contém informações de credenciais para um usuário.</span><span class="sxs-lookup"><span data-stu-id="8e216-159">Contains credential information for a user.</span></span>

</dd> <dt>

[<span data-ttu-id="8e216-160">**WTS \_ dados do usuário \_**</span><span class="sxs-lookup"><span data-stu-id="8e216-160">**WTS\_USER\_DATA**</span></span>](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

<span data-ttu-id="8e216-161">Contém os valores de propriedade de cliente SELECT.</span><span class="sxs-lookup"><span data-stu-id="8e216-161">Contains select client property values.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8e216-162">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e216-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e216-163">Referência do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="8e216-163">Remote Desktop Protocol Provider Reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dt>

[<span data-ttu-id="8e216-164">Enumerações de provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="8e216-164">Remote Desktop Protocol Provider Enumerations</span></span>](custom-remote-protocol-enumerations.md)
</dt> <dt>

[<span data-ttu-id="8e216-165">Interfaces do provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="8e216-165">Remote Desktop Protocol Provider Interfaces</span></span>](custom-remote-protocol-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8e216-166">Uniões de provedor de protocolo RDP</span><span class="sxs-lookup"><span data-stu-id="8e216-166">Remote Desktop Protocol Provider Unions</span></span>](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




