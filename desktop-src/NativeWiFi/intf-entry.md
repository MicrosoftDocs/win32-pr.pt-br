---
description: Contém informações detalhadas sobre uma interface exigida por um cliente RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: Estrutura de INTF_ENTRY (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502188"
---
# <a name="intf_entry-structure"></a><span data-ttu-id="e0e95-103">\_Estrutura de entrada INTF</span><span class="sxs-lookup"><span data-stu-id="e0e95-103">INTF\_ENTRY structure</span></span>

<span data-ttu-id="e0e95-104">\[**INTF \_ A entrada** não tem mais suporte do Windows Vista e do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="e0e95-104">\[**INTF\_ENTRY** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="e0e95-105">Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="e0e95-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="e0e95-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="e0e95-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="e0e95-107">Contém informações detalhadas sobre uma interface exigida por um cliente RPC.</span><span class="sxs-lookup"><span data-stu-id="e0e95-107">Contains detailed information about an interface that is required by an RPC client.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e95-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0e95-108">Syntax</span></span>


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a><span data-ttu-id="e0e95-109">Membros</span><span class="sxs-lookup"><span data-stu-id="e0e95-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="e0e95-110">**wszGuid**</span><span class="sxs-lookup"><span data-stu-id="e0e95-110">**wszGuid**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-111">Um ponteiro para o GUID da interface representado como uma cadeia de caracteres Unicode no seguinte formato: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span><span class="sxs-lookup"><span data-stu-id="e0e95-111">A pointer to the interface GUID represented as a Unicode string in the following format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-112">**wszDescr**</span><span class="sxs-lookup"><span data-stu-id="e0e95-112">**wszDescr**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-113">Um ponteiro para uma cadeia de caracteres que contém a descrição da interface que é recuperada pelo serviço de configuração zero sem fio (WZCSVC).</span><span class="sxs-lookup"><span data-stu-id="e0e95-113">A pointer to a string that contains the interface description that is retrieved by the Wireless Zero Configuration service (WZCSVC).</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-114">**dwContext**</span><span class="sxs-lookup"><span data-stu-id="e0e95-114">**dwContext**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-115">Reservado para uso interno.</span><span class="sxs-lookup"><span data-stu-id="e0e95-115">Reserved for internal use.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-116">**ulMediaState**</span><span class="sxs-lookup"><span data-stu-id="e0e95-116">**ulMediaState**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-117">O estado atual de conexão de mídia NDIS para a interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-117">The current NDIS media connect state for the interface.</span></span> <span data-ttu-id="e0e95-118">A tabela a seguir mostra os valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="e0e95-118">The following table shows the possible values.</span></span>



| <span data-ttu-id="e0e95-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e95-119">Value</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="e0e95-120">Significado</span><span class="sxs-lookup"><span data-stu-id="e0e95-120">Meaning</span></span>                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <span data-ttu-id="e0e95-121"><dt> **Estado da mídia \_ \_ conectado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-121"><dt>**MEDIA\_STATE\_CONNECTED** </dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="e0e95-122">A mídia está conectada.</span><span class="sxs-lookup"><span data-stu-id="e0e95-122">The media is connected.</span></span><br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <span data-ttu-id="e0e95-123"><dt>**Mídia \_ ESTADO \_ desconectado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-123"><dt>**MEDIA\_STATE\_DISCONNECTED**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="e0e95-124">A mídia está desconectada.</span><span class="sxs-lookup"><span data-stu-id="e0e95-124">The media is disconnected.</span></span><br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <span data-ttu-id="e0e95-125"><dt>**Mídia \_ ESTADO \_ desconhecido**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-125"><dt>**MEDIA\_STATE\_UNKNOWN**</dt> <dt>-1</dt></span></span> </dl>               | <span data-ttu-id="e0e95-126">O estado da mídia é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="e0e95-126">The media state is unknown.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0e95-127">**ulMediaType**</span><span class="sxs-lookup"><span data-stu-id="e0e95-127">**ulMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-128">Os tipos de mídia NDIS que a NIC usa atualmente.</span><span class="sxs-lookup"><span data-stu-id="e0e95-128">The NDIS media types that the NIC currently uses.</span></span> <span data-ttu-id="e0e95-129">Quando consultado, o valor desse membro é **NdisMedium802 \_ 3** , conforme definido no arquivo de cabeçalho *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-129">When queried, the value of this member is **NdisMedium802\_3** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-130">**ulPhysicalMediaType**</span><span class="sxs-lookup"><span data-stu-id="e0e95-130">**ulPhysicalMediaType**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-131">O tipo de mídia NDIS da interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-131">The NDIS media type for the interface.</span></span> <span data-ttu-id="e0e95-132">Quando consultado, o valor desse membro é **NdisPhysicalMediumWirelessLan** conforme definido no arquivo de cabeçalho *Ndispnp. h* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-132">When queried, the value of this member is **NdisPhysicalMediumWirelessLan** as defined in the *Ndispnp.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-133">**nInfraMode**</span><span class="sxs-lookup"><span data-stu-id="e0e95-133">**nInfraMode**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-134">O modo de infraestrutura atual 802,11 definido na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-134">The current 802.11 Infrastructure Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-135">**nAuthMode**</span><span class="sxs-lookup"><span data-stu-id="e0e95-135">**nAuthMode**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-136">O modo de autenticação 802,11 atual definido na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-136">The current 802.11 Authentication Mode set on the interface.</span></span>

<span data-ttu-id="e0e95-137">A tabela a seguir mostra os valores possíveis para o parâmetro com base na enumeração do **modo de autenticação do NDIS \_ 802 \_ 11 \_ \_** definido no arquivo de cabeçalho *NtDDNdis. h* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-137">The following table shows the possible values for the parameter based on the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration defined in the *NtDDNdis.h* header file.</span></span>



| <span data-ttu-id="e0e95-138">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e95-138">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="e0e95-139">Significado</span><span class="sxs-lookup"><span data-stu-id="e0e95-139">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <span data-ttu-id="e0e95-140"><dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-140"><dt>**Ndis802\_11AuthModeOpen**</dt> <dt>1</dt></span></span> </dl>                         | <span data-ttu-id="e0e95-141">Autenticação de sistema aberto IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="e0e95-141">IEEE 802.11 Open System authentication.</span></span><br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <span data-ttu-id="e0e95-142"><dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-142"><dt>**Ndis802\_11AuthModeShared**</dt> <dt>2</dt></span></span> </dl>                 | <span data-ttu-id="e0e95-143">A autenticação compartilhada IEEE 802,11 que usa uma chave de privacidade equivalente com fio (WEP) pré-compartilhada.</span><span class="sxs-lookup"><span data-stu-id="e0e95-143">IEEE 802.11 shared authentication that uses a pre-shared wired equivalent privacy (WEP) key.</span></span> <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <span data-ttu-id="e0e95-144"><dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-144"><dt>**Ndis802\_11AuthModeAutoSwitch**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="e0e95-145">Modo de comutador automático.</span><span class="sxs-lookup"><span data-stu-id="e0e95-145">Auto-switch mode.</span></span> <span data-ttu-id="e0e95-146">Ao usar o modo de comutador automático, a NIC (placa de interface de rede) sem fio tenta o modo de autenticação compartilhado primeiro.</span><span class="sxs-lookup"><span data-stu-id="e0e95-146">When using auto-switch mode, the wireless network interface card (NIC) tries shared authentication mode first.</span></span> <span data-ttu-id="e0e95-147">Se o modo compartilhado falhar, a NIC tentará usar o modo de autenticação aberta.</span><span class="sxs-lookup"><span data-stu-id="e0e95-147">If shared mode fails, the NIC attempts to use open authentication mode.</span></span> <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <span data-ttu-id="e0e95-148"><dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-148"><dt>**Ndis802\_11AuthModeWPA**</dt> <dt>4</dt></span></span> </dl>                             | <span data-ttu-id="e0e95-149">Segurança de WPA (acesso protegido sem fio).</span><span class="sxs-lookup"><span data-stu-id="e0e95-149">Wireless Protected Access(WPA) security.</span></span> <span data-ttu-id="e0e95-150">A autenticação é executada entre o suplicante, o autenticador e o servidor de autenticação sobre IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e0e95-150">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="e0e95-151">As chaves de criptografia são dinâmicas e são derivadas por meio do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e0e95-151">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <span data-ttu-id="e0e95-152"><dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-152"><dt>**Ndis802\_11AuthModeWPAPSK**</dt> <dt>5</dt></span></span> </dl>                 | <span data-ttu-id="e0e95-153">Segurança WPA usando uma chave pré-compartilhada.</span><span class="sxs-lookup"><span data-stu-id="e0e95-153">WPA security using a pre-shared key.</span></span> <span data-ttu-id="e0e95-154">A autenticação é executada entre o suplicante e o autenticador sobre IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e0e95-154">Authentication is performed between the supplicant and authenticator over IEEE 802.1X.</span></span> <span data-ttu-id="e0e95-155">As chaves de criptografia são dinâmicas e são derivadas por meio da chave pré-compartilhada usada pelo suplicante e pelo autenticador.</span><span class="sxs-lookup"><span data-stu-id="e0e95-155">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <span data-ttu-id="e0e95-156"><dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-156"><dt>**Ndis802\_11AuthModeWPANone**</dt> <dt>6</dt></span></span> </dl>             | <span data-ttu-id="e0e95-157">Segurança WPA.</span><span class="sxs-lookup"><span data-stu-id="e0e95-157">WPA security.</span></span> <span data-ttu-id="e0e95-158">A autenticação é executada usando uma chave pré-compartilhada sem autenticação IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e0e95-158">Authentication is performed using a preshared key without IEEE 802.1X authentication.</span></span> <span data-ttu-id="e0e95-159">As chaves de criptografia são estáticas e são derivadas por meio da chave pré-compartilhada.</span><span class="sxs-lookup"><span data-stu-id="e0e95-159">Encryption keys are static and are derived through the preshared key.</span></span> <span data-ttu-id="e0e95-160">Esse modo é aplicável somente a tipos de rede ad hoc.</span><span class="sxs-lookup"><span data-stu-id="e0e95-160">This mode is applicable only to ad hoc network types.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <span data-ttu-id="e0e95-161"><dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-161"><dt>**Ndis802\_11AuthModeWPA2**</dt> <dt>7</dt></span></span> </dl>                         | <span data-ttu-id="e0e95-162">Segurança WPA2.</span><span class="sxs-lookup"><span data-stu-id="e0e95-162">WPA2 security.</span></span> <span data-ttu-id="e0e95-163">A autenticação é executada entre o suplicante, o autenticador e o servidor de autenticação sobre IEEE 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="e0e95-163">Authentication is performed between the supplicant, authenticator, and authentication server over IEEE 802.1X.</span></span> <span data-ttu-id="e0e95-164">As chaves de criptografia são dinâmicas e são derivadas por meio do processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e0e95-164">Encryption keys are dynamic and are derived through the authentication process.</span></span> <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <span data-ttu-id="e0e95-165"><dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-165"><dt>**Ndis802\_11AuthModeWPA2PSK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="e0e95-166">Especifica a segurança WPA2.</span><span class="sxs-lookup"><span data-stu-id="e0e95-166">Specifies WPA2 security.</span></span> <span data-ttu-id="e0e95-167">A autenticação é executada entre o suplicante e o autenticador sobre IEEE 802 1X.</span><span class="sxs-lookup"><span data-stu-id="e0e95-167">Authentication is performed between the supplicant and authenticator over IEEE 802 1X.</span></span> <span data-ttu-id="e0e95-168">As chaves de criptografia são dinâmicas e são derivadas por meio da chave pré-compartilhada usada pelo suplicante e pelo autenticador.</span><span class="sxs-lookup"><span data-stu-id="e0e95-168">Encryption keys are dynamic and are derived through the preshared key used by the supplicant and authenticator.</span></span> <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <span data-ttu-id="e0e95-169"><dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-169"><dt>**Ndis802\_11AuthModeMax**</dt> <dt>9</dt></span></span> </dl>                             | <span data-ttu-id="e0e95-170">O valor máximo possível para o valor de enumeração do **\_ modo de autenticação NDIS 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="e0e95-170">The maximum possible value for the **NDIS\_802\_11\_AUTHENTICATION\_MODE** enumeration value.</span></span> <span data-ttu-id="e0e95-171">Esse não é um valor válido para o modo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="e0e95-171">This is not a legal value for the authentication mode.</span></span> <br/>                                                                                        |



 

</dd> <dt>

<span data-ttu-id="e0e95-172">**nWepStatus**</span><span class="sxs-lookup"><span data-stu-id="e0e95-172">**nWepStatus**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-173">O modo de criptografia 802,11 atual definido na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-173">The current 802.11 Encryption Mode set on the interface.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-174">**dwCtlFlags**</span><span class="sxs-lookup"><span data-stu-id="e0e95-174">**dwCtlFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-175">Um valor de bitmask de sinalizadores de controle que indicam como o WZCSVC está operando na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-175">A bitmask value of control flags that indicate how WZCSVC is operating on the interface.</span></span>

<span data-ttu-id="e0e95-176">A tabela a seguir mostra os valores de bit possíveis.</span><span class="sxs-lookup"><span data-stu-id="e0e95-176">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="e0e95-177">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e95-177">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="e0e95-178">Significado</span><span class="sxs-lookup"><span data-stu-id="e0e95-178">Meaning</span></span>                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <span data-ttu-id="e0e95-179"><dt>**INTFCTL \_ 0x0007 de \_ máscara cm**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-179"><dt>**INTFCTL\_CM\_MASK**</dt> <dt>0x0007</dt></span></span> </dl>      | <span data-ttu-id="e0e95-180">Um bitmask para o modo de filtro de rede.</span><span class="sxs-lookup"><span data-stu-id="e0e95-180">A bitmask for the network filter mode.</span></span> <span data-ttu-id="e0e95-181">\_ \_ A máscara INTFCTL cm & dwCtlFlags resultar em um valor da infraestrutura de rede do tipo NDIS \_ 802 \_ 11 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e0e95-181">INTFCTL\_CM\_MASK & dwCtlFlags result in a value of the type NDIS\_802\_11\_NETWORK\_INFRASTRUCTURE.</span></span> <span data-ttu-id="e0e95-182">O valor resultante indica se o WZCSVC se conecta somente a redes de infraestrutura, redes Adhoc ou a ambos os tipos de redes.</span><span class="sxs-lookup"><span data-stu-id="e0e95-182">The resulting value indicates whether WZCSVC connects only to infrastructure networks, adhoc networks, or to both types of networks.</span></span><br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <span data-ttu-id="e0e95-183"><dt>**INTFCTL \_**</dt> <dt>0x8000</dt> habilitado</span><span class="sxs-lookup"><span data-stu-id="e0e95-183"><dt>**INTFCTL\_ENABLED**</dt> <dt>0x8000</dt></span></span> </dl>       | <span data-ttu-id="e0e95-184">Indica se WZCSVC deve configurar a interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-184">Indicates whether WZCSVC should configure the interface.</span></span><br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <span data-ttu-id="e0e95-185"><dt>**INTFCTL \_**</dt> <dt>0X4000</dt> de FALLBACK</span><span class="sxs-lookup"><span data-stu-id="e0e95-185"><dt>**INTFCTL\_FALLBACK**</dt> <dt>0x4000</dt></span></span> </dl>    | <span data-ttu-id="e0e95-186">Se uma rede preferencial não estiver disponível, esse valor indicará se o WZCSVC deve configurar automaticamente a NIC para associar a qualquer rede disponível.</span><span class="sxs-lookup"><span data-stu-id="e0e95-186">If a preferred network is not available, this value indicates whether WZCSVC should automatically configure the NIC to associate to any available network.</span></span><br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <span data-ttu-id="e0e95-187"><dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-187"><dt>**INTFCTL\_OIDSSUPP** </dt> <dt>0x2000</dt></span></span> </dl> | <span data-ttu-id="e0e95-188">Indica se o driver NIC dá suporte a todos os OIDs 802,11 exigidos pelo WZCSVC para funcionar.</span><span class="sxs-lookup"><span data-stu-id="e0e95-188">Indicates whether the NIC driver supports all the 802.11 OIDs required by WZCSVC to function.</span></span><br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <span data-ttu-id="e0e95-189"><dt> **INTFCTL \_ volatile**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-189"><dt>**INTFCTL\_VOLATILE** </dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="e0e95-190">Indica se os parâmetros de serviço para esta interface devem ser mantidos no registro.</span><span class="sxs-lookup"><span data-stu-id="e0e95-190">Indicates whether the service parameters for this interface should be retained in the registry.</span></span> <br/> <span data-ttu-id="e0e95-191">Se esse valor for definido, esses parâmetros serão voláteis e não deverão ser mantidos no registro.</span><span class="sxs-lookup"><span data-stu-id="e0e95-191">If this value is set, then these parameters are volatile and should not be retained in the registry.</span></span><br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <span data-ttu-id="e0e95-192"><dt> **\_ Política de INTFCTL**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-192"><dt>**INTFCTL\_POLICY** </dt> <dt>0x0800</dt></span></span> </dl>       | <span data-ttu-id="e0e95-193">Indica se os parâmetros de serviço para essa interface são enviados por Push por uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="e0e95-193">Indicates whether the service parameters for this interface are pushed by a group policy.</span></span><br/> <span data-ttu-id="e0e95-194">Se esse valor for definido, os parâmetros de serviço serão enviados por push para o computador local pela diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="e0e95-194">If this value is set, then the service parameters are pushed to the local computer by group policy.</span></span><br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <span data-ttu-id="e0e95-195"><dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-195"><dt>**INTFCTL\_8021XSUPP**</dt> <dt>0x1000</dt></span></span> </dl> | <span data-ttu-id="e0e95-196">Indica se o suporte a 802.1 X está habilitado.</span><span class="sxs-lookup"><span data-stu-id="e0e95-196">Indicates whether 802.1X support is enabled.</span></span><br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="e0e95-197">**dwDynFlags**</span><span class="sxs-lookup"><span data-stu-id="e0e95-197">**dwDynFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-198">Um bitmask de sinalizadores dinâmicos que controlam o comportamento dinâmico (não persistente e não-estático) na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-198">A bitmask of dynamic flags that control the dynamic (non-persistent and non-static) behavior on the interface.</span></span>

<span data-ttu-id="e0e95-199">Esses bits são úteis para disparar alterações dinâmicas e temporárias no modo como o WZCSVC atua na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-199">These bits are useful to trigger dynamic, temporary changes in the way the WZCSVC acts on the interface.</span></span> <span data-ttu-id="e0e95-200">Nenhum desses bits é mantido no registro, de modo que as configurações não sobreviverão a uma reinicialização do sistema ou a uma sequência de habilitação e ativação do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e0e95-200">None of these bits are persisted in the registry, so the settings won't survive a system restart or a device disable and enable sequence.</span></span>

<span data-ttu-id="e0e95-201">A tabela a seguir mostra os valores de bit possíveis.</span><span class="sxs-lookup"><span data-stu-id="e0e95-201">The following table shows the possible bit values.</span></span>



| <span data-ttu-id="e0e95-202">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e95-202">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="e0e95-203">Significado</span><span class="sxs-lookup"><span data-stu-id="e0e95-203">Meaning</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <span data-ttu-id="e0e95-204"><dt>**INTFDYN \_ NOSCAN**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-204"><dt>**INTFDYN\_NOSCAN**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="e0e95-205">Indica que o WZCSVC não deve solicitar que a interface execute uma verificação ativa, mas em vez disso, use os valores armazenados em cache no driver NIC.</span><span class="sxs-lookup"><span data-stu-id="e0e95-205">Indicates that the WZCSVC should not request the interface conduct an active scan, but instead use the cached values in the NIC driver.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e0e95-206">**dwCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e0e95-206">**dwCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-207">Especifica os recursos do driver.</span><span class="sxs-lookup"><span data-stu-id="e0e95-207">Specifies the driver capabilities.</span></span>



| <span data-ttu-id="e0e95-208">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e95-208">Value</span></span>                                                                                                                                                                                                                                                         | <span data-ttu-id="e0e95-209">Significado</span><span class="sxs-lookup"><span data-stu-id="e0e95-209">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <span data-ttu-id="e0e95-210"><dt>**INTFCAP \_ \_ \_ Máscara de codificação máxima**</dt> <dt>0x000000FF</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-210"><dt>**INTFCAP\_MAX\_CIPHER\_MASK**</dt> <dt>0x000000ff</dt></span></span> </dl> | <span data-ttu-id="e0e95-211">Os bits de ordem inferior desse membro são usados para indicar a criptografia máxima com suporte.</span><span class="sxs-lookup"><span data-stu-id="e0e95-211">The lower order bits of this member are used to indicate the maximum encryption that is supported.</span></span> <span data-ttu-id="e0e95-212">Os valores possíveis são alguns dos valores de enumeração definidos na estrutura **de \_ \_ \_ \_ status WEP do NDIS 802 11** no arquivo de cabeçalho *NtDDNdis. h* incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="e0e95-212">The possible values are some of the enumeration values defined in the **NDIS\_802\_11\_WEP\_STATUS** structure in the *NtDDNdis.h* header file included in the Windows SDK.</span></span><br/> <span data-ttu-id="e0e95-213">O \_ valor de 11Encryption1Enabled Ndis802 (2) indica que há suporte para o WEP.</span><span class="sxs-lookup"><span data-stu-id="e0e95-213">The Ndis802\_11Encryption1Enabled value (2) indicates that WEP is supported.</span></span> <span data-ttu-id="e0e95-214">Não há suporte para TKIP e AES, e uma chave de transmissão pode ou não estar disponível.</span><span class="sxs-lookup"><span data-stu-id="e0e95-214">TKIP and AES are not supported, and a transmit key may or may not be available.</span></span> <br/> <span data-ttu-id="e0e95-215">O valor de Ndis802 \_ 11Encryption2Enabled (9) indica que há suporte para TKIP e WEP.</span><span class="sxs-lookup"><span data-stu-id="e0e95-215">The Ndis802\_11Encryption2Enabled value (9) indicates that TKIP and WEP are supported.</span></span> <span data-ttu-id="e0e95-216">Não há suporte para AES e uma chave de transmissão está disponível.</span><span class="sxs-lookup"><span data-stu-id="e0e95-216">AES is not supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="e0e95-217">O valor de Ndis802 \_ 11Encryption3Enabled (11) indica que AES, TKIP e WEP têm suporte e uma chave de transmissão está disponível.</span><span class="sxs-lookup"><span data-stu-id="e0e95-217">The Ndis802\_11Encryption3Enabled value (11) indicates that AES, TKIP, and WEP are supported, and a transmit key is available.</span></span> <br/> <span data-ttu-id="e0e95-218">O Ndis802 \_ 11EncryptionNotSupported (8) indica que a chave WEP não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="e0e95-218">The Ndis802\_11EncryptionNotSupported (8) indicates Indicates that the WEP key is not supported.</span></span> <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <span data-ttu-id="e0e95-219"><dt>**INTFCAP \_**</dt> <dt>0x00000100</dt> SSN</span><span class="sxs-lookup"><span data-stu-id="e0e95-219"><dt>**INTFCAP\_SSN**</dt> <dt>0x00000100</dt></span></span> </dl>                                       | <span data-ttu-id="e0e95-220">Indica suporte para rede segura simples (SSN), que é um subconjunto do 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="e0e95-220">Indicates support for Simple Secure Network (SSN) which is a subset of 802.11i.</span></span> <br/> <span data-ttu-id="e0e95-221">O SSN altera a chave de criptografia periodicamente, em oposição ao padrão WEP (Wired Equivaled Privacy), que usa uma chave estática.</span><span class="sxs-lookup"><span data-stu-id="e0e95-221">SSN changes the encryption key periodically, as opposed to the WEP (Wired Equivalent Privacy) standard, which uses a static key.</span></span> <span data-ttu-id="e0e95-222">Para que o SSN funcione, a codificação máxima com suporte deve ser pelo menos TKIP.</span><span class="sxs-lookup"><span data-stu-id="e0e95-222">In order for SSN to work, the maximum supported cipher should be at least TKIP.</span></span> <span data-ttu-id="e0e95-223">O SSN foi desenvolvido por um consórcio de fornecedores em 2002 como uma abordagem provisória para melhorar a segurança da LAN sem fio enquanto o padrão IEEE 802.11 i estava sendo concluído.</span><span class="sxs-lookup"><span data-stu-id="e0e95-223">SSN was developed by a consortium of vendors in 2002 as an interim approach to improve wireless LAN security while the IEEE 802.11i standard was being completed.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <span data-ttu-id="e0e95-224"><dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-224"><dt>**INTFCAP\_80211I**</dt> <dt>0x00000200</dt></span></span> </dl>                              | <span data-ttu-id="e0e95-225">Indica suporte para o padrão IEEE 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="e0e95-225">Indicates support for the IEEE 802.11i standard.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="e0e95-226">**rdNicCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e0e95-226">**rdNicCapabilities**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-227">Um conjunto de recursos para 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="e0e95-227">A set of capabilities for 802.11i.</span></span>

<span data-ttu-id="e0e95-228">A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdNicCapabilities** quando chamado com o sinalizador de **\_ recursos de INTF** passado no parâmetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-228">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdNicCapabilities** data when called with the **INTF\_CAPABILITIES** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="e0e95-229">Se a chamada de função for bem-sucedida, o membro **pData** da estrutura de **\_ dados brutos** conterá uma estrutura de **\_ \_ recursos INTF 80211** .</span><span class="sxs-lookup"><span data-stu-id="e0e95-229">If the function call is successful, the **pData** member of the **RAW\_DATA** structure contains an **INTF\_80211\_CAPABILITY** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-230">**rdSSID**</span><span class="sxs-lookup"><span data-stu-id="e0e95-230">**rdSSID**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-231">Dados binários que contêm o SSID 802,11 atualmente configurado na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-231">Binary data containing the 802.11 SSID currently configured on the interface.</span></span>

<span data-ttu-id="e0e95-232">A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdSSID** quando chamado com o sinalizador **\_ SSID INTF** passado no parâmetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-232">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdSSID** data when called with the **INTF\_SSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="e0e95-233">Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o membro **SsidLength** de uma estrutura de **SSID do NDIS \_ 802 \_ 11 \_** e o membro **pData** da estrutura de **\_ dados brutos** conterá o membro **SSID** de uma estrutura de **SSID da NDIS \_ 802 \_ 11 \_** .</span><span class="sxs-lookup"><span data-stu-id="e0e95-233">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the **SsidLength** member of a **NDIS\_802\_11\_SSID** structure and the **pData** member of the **RAW\_DATA** structure contains the **Ssid** member of a **NDIS\_802\_11\_SSID** structure.</span></span>

<span data-ttu-id="e0e95-234">A estrutura de **SSID do NDIS \_ 802 \_ 11 \_** é definida no arquivo de cabeçalho *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-234">The **NDIS\_802\_11\_SSID** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-235">**rdBSSID**</span><span class="sxs-lookup"><span data-stu-id="e0e95-235">**rdBSSID**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-236">Dados binários que contêm o BSSID 802,11 configurado na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-236">Binary data containing the 802.11 BSSID configured on the interface.</span></span>

<span data-ttu-id="e0e95-237">A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdBSSID** quando chamado com o sinalizador de **\_ bssid de INTF** passado no parâmetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-237">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSID** data when called with the **INTF\_BSSID** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="e0e95-238">Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o tamanho de uma estrutura de **\_ \_ \_ \_ endereços MAC de NDIS 802 11** e o membro **pData** da estrutura de **\_ dados brutos** conterá a estrutura de **\_ \_ \_ \_ endereço MAC de 802** .</span><span class="sxs-lookup"><span data-stu-id="e0e95-238">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the size of an **NDIS\_802\_11\_MAC\_ADDRESS** structure and the **pData** member of the **RAW\_DATA** structure contains the **NDIS\_802\_11\_MAC\_ADDRESS** structure.</span></span>

<span data-ttu-id="e0e95-239">A estrutura de **\_ \_ \_ \_ endereços MAC do NDIS 802 11** é definida no arquivo de cabeçalho *Ntddndis. h* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-239">The **NDIS\_802\_11\_MAC\_ADDRESS** structure is defined in the *Ntddndis.h* header file.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-240">**rdBSSIDList**</span><span class="sxs-lookup"><span data-stu-id="e0e95-240">**rdBSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-241">Dados binários que contêm a lista de BSSIDs que foram recuperados pela última vez por WZCSVC.</span><span class="sxs-lookup"><span data-stu-id="e0e95-241">Binary data that contains the list of BSSIDs that was last retrieved by WZCSVC.</span></span>

<span data-ttu-id="e0e95-242">A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdBSSIDList** quando chamado com o sinalizador **INTF \_ BSSIDLIST** passado no parâmetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-242">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdBSSIDList** data when called with the **INTF\_BSSIDLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="e0e95-243">Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o comprimento do buffer com os dados retornados e o membro **pData** da estrutura de **\_ dados brutos** conterá a estrutura da **lista de configuração do WZC \_ 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="e0e95-243">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-244">**rdStSSIDList**</span><span class="sxs-lookup"><span data-stu-id="e0e95-244">**rdStSSIDList**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-245">Dados binários que contêm a lista de redes preferenciais configuradas para esta interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-245">Binary data that contains the list of preferred networks configured for this interface.</span></span>

<span data-ttu-id="e0e95-246">A função [**WZCQueryInterface**](wzcqueryinterface.md) retorna dados de **rdStSSIDList** quando chamado com o sinalizador de **INTF \_ preflist** passado no parâmetro *dwInflags* .</span><span class="sxs-lookup"><span data-stu-id="e0e95-246">The [**WZCQueryInterface**](wzcqueryinterface.md) function returns **rdStSSIDList** data when called with the **INTF\_PREFLIST** flag passed in the *dwInflags* parameter.</span></span> <span data-ttu-id="e0e95-247">Se a chamada de função for bem-sucedida, o membro **dwDataLen** da estrutura de **\_ dados brutos** conterá o comprimento do buffer com os dados retornados e o membro **pData** da estrutura de **\_ dados brutos** conterá a estrutura da **lista de configuração do WZC \_ 802 \_ 11 \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="e0e95-247">If the function call is successful, the **dwDataLen** member of the **RAW\_DATA** structure contains the length of the buffer with the returned data and the **pData** member of the **RAW\_DATA** structure contains the **WZC\_802\_11\_CONFIG\_LIST** structure.</span></span>

<span data-ttu-id="e0e95-248">Se uma das redes preferenciais estiver conectada no momento, o membro **dwCtlFlags** da estrutura de **configuração de \_ WLAN \_ do WZC** para a rede terá o conjunto de bits 0x0400 ( **\_ mídia \_ conectada WZCCTL** ).</span><span class="sxs-lookup"><span data-stu-id="e0e95-248">If one of the preferred networks is currently connected, the **dwCtlFlags** member of the **WZC\_WLAN\_CONFIG** structure for the network will have the **WZCCTL\_MEDIA\_CONNECTED** (0x0400) bit set.</span></span>

</dd> <dt>

<span data-ttu-id="e0e95-249">**rdCtrlData**</span><span class="sxs-lookup"><span data-stu-id="e0e95-249">**rdCtrlData**</span></span>
</dt> <dd>

<span data-ttu-id="e0e95-250">Dados binários usados com outros sinalizadores de controle, ao definir parâmetros adicionais na interface.</span><span class="sxs-lookup"><span data-stu-id="e0e95-250">Binary data used with other control flags, when setting additional parameters on the interface.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0e95-251">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0e95-251">Remarks</span></span>

<span data-ttu-id="e0e95-252">A estrutura de **\_ entrada INTF** é usada pelas funções [**WZCQueryInterface**](wzcqueryinterface.md) e [**WZCRefreshInterface**](wzcrefreshinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="e0e95-252">The **INTF\_ENTRY** structure is used by the [**WZCQueryInterface**](wzcqueryinterface.md) and [**WZCRefreshInterface**](wzcrefreshinterface.md) functions.</span></span>

<span data-ttu-id="e0e95-253">A estrutura de **\_ dados brutos** é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e0e95-253">The **RAW\_DATA** structure is defined as follows:</span></span>


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



<span data-ttu-id="e0e95-254">O membro *pData* aponta para dados binários.</span><span class="sxs-lookup"><span data-stu-id="e0e95-254">The *pData* member points to binary data.</span></span> <span data-ttu-id="e0e95-255">O *dwDataLen* indica o número de bytes apontados por *pData*.</span><span class="sxs-lookup"><span data-stu-id="e0e95-255">The *dwDataLen* indicates the number of bytes pointed by *pData*.</span></span>

> [!Note]  
> <span data-ttu-id="e0e95-256">O arquivo de cabeçalho *wzcsapi. h* não está disponível no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="e0e95-256">The *Wzcsapi.h* header file is not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e0e95-257">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e95-257">Requirements</span></span>



| <span data-ttu-id="e0e95-258">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e95-258">Requirement</span></span> | <span data-ttu-id="e0e95-259">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e95-259">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e95-260">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0e95-260">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e95-261">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="e0e95-261">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0e95-262">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0e95-262">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e95-263">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0e95-263">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0e95-264">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e0e95-264">End of client support</span></span><br/>    | <span data-ttu-id="e0e95-265">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="e0e95-265">Windows XP with SP3</span></span><br/>                                                       |
| <span data-ttu-id="e0e95-266">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e0e95-266">End of server support</span></span><br/>    | <span data-ttu-id="e0e95-267">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e0e95-267">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="e0e95-268">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0e95-268">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0e95-269"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e95-269"><dt>Wzcsapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e95-270">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0e95-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e95-271">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="e0e95-271">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="e0e95-272">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="e0e95-272">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="e0e95-273">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="e0e95-273">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 




