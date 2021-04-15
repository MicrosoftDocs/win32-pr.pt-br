---
title: Definições de configuração
description: O comportamento da API do ponto de controle e da API de host do dispositivo pode ser modificado alterando as configurações no registro.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105760937"
---
# <a name="configuration-settings"></a><span data-ttu-id="5af99-103">Definições de configuração</span><span class="sxs-lookup"><span data-stu-id="5af99-103">Configuration Settings</span></span>

<span data-ttu-id="5af99-104">O comportamento da [API do ponto de controle](control-point-api.md) e da API de host do [dispositivo](device-host-api.md) pode ser modificado alterando as configurações no registro.</span><span class="sxs-lookup"><span data-stu-id="5af99-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="5af99-105">Há sete valores de registro que afetam o comportamento:</span><span class="sxs-lookup"><span data-stu-id="5af99-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="5af99-106">**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="5af99-106">**DownloadScope**</span></span>
-   <span data-ttu-id="5af99-107">**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="5af99-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="5af99-108">\\Host de dispositivo **UPnP** \\ **Limite de tamanho de arquivo**</span><span class="sxs-lookup"><span data-stu-id="5af99-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="5af99-109">\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de tamanho de arquivo**</span><span class="sxs-lookup"><span data-stu-id="5af99-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="5af99-110">**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="5af99-110">**MaxCache**</span></span>
-   <span data-ttu-id="5af99-111">**TTL**</span><span class="sxs-lookup"><span data-stu-id="5af99-111">**TTL**</span></span>
-   <span data-ttu-id="5af99-112">**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="5af99-112">**ReceiveScope**</span></span>

<span data-ttu-id="5af99-113">Há dois valores de registro chamados **limite de tamanho de arquivo**, um para documentos de descrição e o outro para respostas que usam SOAP (Simple Object Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="5af99-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="5af99-114">O local de cada um dos sete valores no registro é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5af99-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="5af99-115">Descrições de valor do registro</span><span class="sxs-lookup"><span data-stu-id="5af99-115">Registry Value Descriptions</span></span>

<span data-ttu-id="5af99-116">Os valores do registro são explicados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="5af99-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="5af99-117">Cada valor de registro é um **reg \_ DWORD** (um número inteiro de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="5af99-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="5af99-118">O efeito de cada valor é global.</span><span class="sxs-lookup"><span data-stu-id="5af99-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="5af99-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="5af99-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-120">Especifica quais endereços IP são válidos para a URL do documento de descrição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5af99-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="5af99-121">Se o endereço IP do host especificado na URL do documento de descrição não estiver dentro do escopo especificado por **DownloadScope**, esse endereço IP não será válido e o objeto do dispositivo não será criado.</span><span class="sxs-lookup"><span data-stu-id="5af99-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="5af99-122">Os valores válidos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5af99-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="5af99-123">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="5af99-123">The default value is 1.</span></span>



| <span data-ttu-id="5af99-124">Valor de **DownloadScope**</span><span class="sxs-lookup"><span data-stu-id="5af99-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="5af99-125">Significado</span><span class="sxs-lookup"><span data-stu-id="5af99-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af99-126">0</span><span class="sxs-lookup"><span data-stu-id="5af99-126">0</span></span>                          | <span data-ttu-id="5af99-127">O endereço IP do host deve ser um endereço de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5af99-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="5af99-128">1</span><span class="sxs-lookup"><span data-stu-id="5af99-128">1</span></span>                          | <span data-ttu-id="5af99-129">O endereço IP do host deve ser um endereço de sub-rede ou um endereço privado que seja um de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (conforme especificado pela RFC 1918) ou 169,254. *x*. *x* (conforme especificado pela RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="5af99-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="5af99-130">2</span><span class="sxs-lookup"><span data-stu-id="5af99-130">2</span></span>                          | <span data-ttu-id="5af99-131">O endereço IP do host deve ser um endereço de sub-rede, um endereço privado ou um endereço que esteja dentro dos saltos de tempo de vida (TTL) do ponto de controle.</span><span class="sxs-lookup"><span data-stu-id="5af99-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="5af99-132">3</span><span class="sxs-lookup"><span data-stu-id="5af99-132">3</span></span>                          | <span data-ttu-id="5af99-133">O endereço IP do host pode ser qualquer endereço.</span><span class="sxs-lookup"><span data-stu-id="5af99-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="5af99-134">>3</span><span class="sxs-lookup"><span data-stu-id="5af99-134">>3</span></span>                      | <span data-ttu-id="5af99-135">O mesmo que para o valor 0.</span><span class="sxs-lookup"><span data-stu-id="5af99-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="5af99-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span><span class="sxs-lookup"><span data-stu-id="5af99-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5af99-137">Optional.</span></span> <span data-ttu-id="5af99-138">Especifica o tempo de vida de um dispositivo, em segundos, que substitui o valor fornecido na mensagem de anúncio do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5af99-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="5af99-139">Se **DeviceLifeTime** estiver presente, o valor especificado no anúncio do dispositivo será ignorado e o valor do registro será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="5af99-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="5af99-140">Isso se aplica a todos os dispositivos.</span><span class="sxs-lookup"><span data-stu-id="5af99-140">This applies to all devices.</span></span>

<span data-ttu-id="5af99-141">Os valores válidos variam de 900 a **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5af99-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="5af99-142">O valor padrão é 1800.</span><span class="sxs-lookup"><span data-stu-id="5af99-142">The default value is 1800.</span></span> <span data-ttu-id="5af99-143">Se **DeviceLifeTime** for definido como 0, o valor padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="5af99-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="5af99-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\Host de dispositivo **UPnP** \\ **Limite de tamanho de arquivo**</span><span class="sxs-lookup"><span data-stu-id="5af99-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-145">Especifica o tamanho máximo, em bytes, de cada documento de descrição.</span><span class="sxs-lookup"><span data-stu-id="5af99-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="5af99-146">Essa configuração não é configurável em versões do Windows anteriores ao Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="5af99-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="5af99-147">Nas versões anteriores, essa configuração é embutida em código como 102400.</span><span class="sxs-lookup"><span data-stu-id="5af99-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="5af99-148">Os valores válidos variam de 10240 a **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5af99-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="5af99-149">O valor padrão é 102400.</span><span class="sxs-lookup"><span data-stu-id="5af99-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="5af99-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Limite de tamanho de arquivo**</span><span class="sxs-lookup"><span data-stu-id="5af99-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-151">Especifica o tamanho máximo, em bytes, da resposta SOAP aceitável.</span><span class="sxs-lookup"><span data-stu-id="5af99-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="5af99-152">Essa configuração não é configurável em versões do Windows anteriores ao Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="5af99-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="5af99-153">Nas versões anteriores, essa configuração é embutida em código como 102400.</span><span class="sxs-lookup"><span data-stu-id="5af99-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="5af99-154">Os valores válidos variam de 10240 a **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="5af99-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="5af99-155">O valor padrão é 102400.</span><span class="sxs-lookup"><span data-stu-id="5af99-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="5af99-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span><span class="sxs-lookup"><span data-stu-id="5af99-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-157">Especifica o número máximo de entradas permitidas no cache SSDP (Simple Service Discovery Protocol).</span><span class="sxs-lookup"><span data-stu-id="5af99-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="5af99-158">Os valores válidos variam de 10 a 30000.</span><span class="sxs-lookup"><span data-stu-id="5af99-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="5af99-159">O valor padrão é 1000.</span><span class="sxs-lookup"><span data-stu-id="5af99-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="5af99-160"><span id="TTL"></span><span id="ttl"></span>**IGUAL**</span><span class="sxs-lookup"><span data-stu-id="5af99-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-161">Especifica a vida útil para um pacote SSDP.</span><span class="sxs-lookup"><span data-stu-id="5af99-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="5af99-162">Ou seja, **TTL** especifica o número de saltos permitidos para um pacote.</span><span class="sxs-lookup"><span data-stu-id="5af99-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="5af99-163">Os valores válidos variam de 1 a 255.</span><span class="sxs-lookup"><span data-stu-id="5af99-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="5af99-164">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="5af99-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="5af99-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="5af99-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="5af99-166">Especifica quais endereços IP são fontes válidas de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="5af99-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="5af99-167">Se uma mensagem de entrada se originar de um endereço que não está dentro do escopo especificado por **ReceiveScope**, a mensagem será ignorada.</span><span class="sxs-lookup"><span data-stu-id="5af99-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="5af99-168">Essa configuração não é configurável em versões do Windows anteriores ao Windows XP Service Pack 2.</span><span class="sxs-lookup"><span data-stu-id="5af99-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="5af99-169">Nas versões anteriores, uma mensagem é aceita sem considerar sua origem.</span><span class="sxs-lookup"><span data-stu-id="5af99-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="5af99-170">Os valores válidos são mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5af99-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="5af99-171">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="5af99-171">The default value is 1.</span></span>



| <span data-ttu-id="5af99-172">Valor de **ReceiveScope**</span><span class="sxs-lookup"><span data-stu-id="5af99-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="5af99-173">Significado</span><span class="sxs-lookup"><span data-stu-id="5af99-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af99-174">0</span><span class="sxs-lookup"><span data-stu-id="5af99-174">0</span></span>                         | <span data-ttu-id="5af99-175">O endereço IP do remetente deve ser um endereço de sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5af99-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="5af99-176">1</span><span class="sxs-lookup"><span data-stu-id="5af99-176">1</span></span>                         | <span data-ttu-id="5af99-177">O endereço IP do remetente deve ser um endereço de sub-rede ou um endereço privado que seja um de 10. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (conforme especificado pela RFC 1918) ou 169,254. *x*. *x* (conforme especificado pela RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="5af99-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="5af99-178">2</span><span class="sxs-lookup"><span data-stu-id="5af99-178">2</span></span>                         | <span data-ttu-id="5af99-179">Não usado.</span><span class="sxs-lookup"><span data-stu-id="5af99-179">Not used.</span></span> <span data-ttu-id="5af99-180">Se **ReceiveScope** for definido como 2, o valor padrão será usado.</span><span class="sxs-lookup"><span data-stu-id="5af99-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="5af99-181">3</span><span class="sxs-lookup"><span data-stu-id="5af99-181">3</span></span>                         | <span data-ttu-id="5af99-182">O endereço IP do remetente pode ser qualquer endereço.</span><span class="sxs-lookup"><span data-stu-id="5af99-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5af99-183">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5af99-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5af99-184">Visão geral da arquitetura UPnP</span><span class="sxs-lookup"><span data-stu-id="5af99-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




