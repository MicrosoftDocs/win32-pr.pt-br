---
description: Fornece informações detalhadas para uma interface de LAN sem fio gerenciada pelo serviço de configuração zero sem fio.
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: Função WZCQueryInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829781"
---
# <a name="wzcqueryinterface-function"></a><span data-ttu-id="a8597-103">Função WZCQueryInterface</span><span class="sxs-lookup"><span data-stu-id="a8597-103">WZCQueryInterface function</span></span>

<span data-ttu-id="a8597-104">\[O **WZCQueryInterface** não é mais suportado a partir do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a8597-104">\[**WZCQueryInterface** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a8597-105">Em vez disso, use a função [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) .</span><span class="sxs-lookup"><span data-stu-id="a8597-105">Use the [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) function instead.</span></span> <span data-ttu-id="a8597-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).</span><span class="sxs-lookup"><span data-stu-id="a8597-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).</span></span> <span data-ttu-id="a8597-107">\]</span><span class="sxs-lookup"><span data-stu-id="a8597-107">\]</span></span>

<span data-ttu-id="a8597-108">A função **WZCQueryInterface** fornece informações detalhadas para uma interface de LAN sem fio gerenciada pelo serviço de configuração zero sem fio.</span><span class="sxs-lookup"><span data-stu-id="a8597-108">The **WZCQueryInterface** function provides detailed information for a wireless LAN interface managed by the Wireless Zero Configuration service.</span></span>

<span data-ttu-id="a8597-109">Fornece informações detalhadas para uma determinada interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-109">Provides detailed information for a given interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8597-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8597-110">Syntax</span></span>


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a8597-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8597-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8597-112">*pSrvAddr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8597-112">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8597-113">Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função.</span><span class="sxs-lookup"><span data-stu-id="a8597-113">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="a8597-114">Se esse parâmetro for **nulo**, o serviço de configuração sem fio não será consultado no computador local.</span><span class="sxs-lookup"><span data-stu-id="a8597-114">If this parameter is **NULL**, then the Wireless Zero Configuration service is queried on the local computer.</span></span>

<span data-ttu-id="a8597-115">Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="a8597-115">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="a8597-116">*dwInFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a8597-116">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8597-117">Os campos a serem consultados.</span><span class="sxs-lookup"><span data-stu-id="a8597-117">The fields to be queried.</span></span> <span data-ttu-id="a8597-118">Esse é um bitmask que pode conter qualquer combinação dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8597-118">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="a8597-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-119">Value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="a8597-120">Significado</span><span class="sxs-lookup"><span data-stu-id="a8597-120">Meaning</span></span>                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <span data-ttu-id="a8597-121"><dt>**INTF \_ DYNFLAGS**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-121"><dt>**INTF\_DYNFLAGS**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="a8597-122">Retorne o valor para o membro **dwDynFlags** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-122">Return the value for the **dwDynFlags** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="a8597-123"><dt>**INTF \_**</dt> <dt>0X00010000</dt> de descr</span><span class="sxs-lookup"><span data-stu-id="a8597-123"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>                      | <span data-ttu-id="a8597-124">Retorne o valor para o membro **wszDescr** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-124">Return the value for the **wszDescr** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="a8597-125"><dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-125"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="a8597-126">Retorne os valores para os membros **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** na estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-126">Return the values for the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <span data-ttu-id="a8597-127"><dt>**INTF \_ PREFlist**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-127"><dt>**INTF\_PREFLIST**</dt> <dt>0x00040000</dt></span></span> </dl>             | <span data-ttu-id="a8597-128">Retorne a lista preferencial de redes no membro **rdStSSIDList** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-128">Return the preferred list of networks in the **rdStSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <span data-ttu-id="a8597-129"><dt>**INTF \_ RECURSOS**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-129"><dt>**INTF\_CAPABILITIES**</dt> <dt>0x00080000</dt></span></span> </dl> | <span data-ttu-id="a8597-130">Retorne os valores para **dwCapabilities** e os membros **rdNicCapabilities** na estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-130">Return the values for the **dwCapabilities** and the **rdNicCapabilities** members in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <span data-ttu-id="a8597-131"><dt>**INTF \_**</dt> <dt>0X00200000</dt> de infravermelho</span><span class="sxs-lookup"><span data-stu-id="a8597-131"><dt>**INTF\_INFRAMODE**</dt> <dt>0x00200000</dt></span></span> </dl>          | <span data-ttu-id="a8597-132">Retorne o valor para o membro **nInfraMode** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-132">Return the value for the **nInfraMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="a8597-133">O membro **nInfraMode** é válido somente em alguns Estados de contexto de interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-133">The **nInfraMode** member is valid only in some interface context states.</span></span><br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <span data-ttu-id="a8597-134"><dt>**INTF \_ 0x00400000 AUTHmode**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a8597-134"><dt>**INTF\_AUTHMODE**</dt> <dt>0x00400000</dt></span></span> </dl>             | <span data-ttu-id="a8597-135">Retorne o valor para o membro **nAuthMode** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-135">Return the value for the **nAuthMode** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="a8597-136">O membro **nAuthMode** é válido somente em alguns Estados de contexto de interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-136">The **nAuthMode** member is valid only in some interface context states.</span></span><br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <span data-ttu-id="a8597-137"><dt>**INTF \_ WEPSTATUS**</dt> <dt>0x00800000</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-137"><dt>**INTF\_WEPSTATUS**</dt> <dt>0x00800000</dt></span></span> </dl>          | <span data-ttu-id="a8597-138">Retorne o valor para o membro **nWepStatus** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-138">Return the value for the **nWepStatus** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span> <br/> <span data-ttu-id="a8597-139">O membro **nWepStatus** é válido somente em alguns Estados de contexto de interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-139">The **nWepStatus** member is valid only in some interface context states.</span></span><br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <span data-ttu-id="a8597-140"><dt>**INTF \_**</dt> <dt>0x01000000</dt> SSID</span><span class="sxs-lookup"><span data-stu-id="a8597-140"><dt>**INTF\_SSID**</dt> <dt>0x01000000</dt></span></span> </dl>                         | <span data-ttu-id="a8597-141">Retorne o valor para o membro **rdSSID** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-141">Return the value for the **rdSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="a8597-142">O membro **rdSSID** é válido somente em alguns Estados de contexto de interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-142">The **rdSSID** member is valid only in some interface context states.</span></span><br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <span data-ttu-id="a8597-143"><dt>**INTF \_ BSSID**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-143"><dt>**INTF\_BSSID**</dt> <dt>0x02000000</dt></span></span> </dl>                      | <span data-ttu-id="a8597-144">Retorne o valor para o membro **rdBSSID** na estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-144">Return the value for the **rdBSSID** member in the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="a8597-145">O membro **rdBSSID** é válido somente em alguns Estados de contexto de interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-145">The **rdBSSID** member is valid only in some interface context states.</span></span><br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <span data-ttu-id="a8597-146"><dt>**INTF \_ BSSIDLIST**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-146"><dt>**INTF\_BSSIDLIST**</dt> <dt>0x04000000</dt></span></span> </dl>          | <span data-ttu-id="a8597-147">Retorne a lista visível de redes no membro **rdBSSIDList** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* .</span><span class="sxs-lookup"><span data-stu-id="a8597-147">Return the visible list of networks in the **rdBSSIDList** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter.</span></span><br/> <span data-ttu-id="a8597-148">O membro **rdBSSIDList** é válido somente em alguns Estados de contexto de interface.</span><span class="sxs-lookup"><span data-stu-id="a8597-148">The **rdBSSIDList** member is valid only in some interface context states.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a8597-149">*pIntf* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="a8597-149">*pIntf* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8597-150">Na entrada, um ponteiro para a chave da interface a ser consultada.</span><span class="sxs-lookup"><span data-stu-id="a8597-150">On input, a pointer to the key of the interface to query.</span></span> <span data-ttu-id="a8597-151">Na saída, um ponteiro para os dados de interface solicitados.</span><span class="sxs-lookup"><span data-stu-id="a8597-151">On output, a pointer to the requested interface data.</span></span> <span data-ttu-id="a8597-152">Esse parâmetro é um ponteiro para uma estrutura de [**\_ entrada INTF**](intf-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="a8597-152">This parameter is a pointer to an [**INTF\_ENTRY**](intf-entry.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a8597-153">*pdwOutFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a8597-153">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8597-154">Um conjunto de campos recuperados com êxito.</span><span class="sxs-lookup"><span data-stu-id="a8597-154">A set of fields successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8597-155">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8597-155">Return value</span></span>

<span data-ttu-id="a8597-156">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="a8597-156">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a8597-157">Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8597-157">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="a8597-158">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a8597-158">Return code</span></span>                                                                                               | <span data-ttu-id="a8597-159">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8597-159">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a8597-160"><dt>**Arena de erro em \_ \_ Trash**</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-160"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="a8597-161">Os blocos de controle de armazenamento foram destruídos.</span><span class="sxs-lookup"><span data-stu-id="a8597-161">The storage control blocks were destroyed.</span></span> <span data-ttu-id="a8597-162">Esse erro será retornado se o serviço de configuração zero sem fio não tiver inicializado objetos internos.</span><span class="sxs-lookup"><span data-stu-id="a8597-162">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="a8597-163"><dt>**arquivo de erro \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-163"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>    | <span data-ttu-id="a8597-164">O sistema não pode encontrar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a8597-164">The system cannot find the file specified.</span></span> <span data-ttu-id="a8597-165">Esse erro será retornado se o GUID no membro **wszGuid** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* não coincidir com nenhuma das interfaces de LAN sem fio no computador local.</span><span class="sxs-lookup"><span data-stu-id="a8597-165">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="a8597-166"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-166"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="a8597-167">Um parâmetro está incorreto.</span><span class="sxs-lookup"><span data-stu-id="a8597-167">A parameter is incorrect.</span></span> <span data-ttu-id="a8597-168">Esse erro será retornado se o parâmetro *pIntf* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a8597-168">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="a8597-169">Esse erro será retornado se o membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a8597-169">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="a8597-170"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-170"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="a8597-171">Não há memória suficiente disponível para processar essa solicitação e alocar memória para os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="a8597-171">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="a8597-172"><dt>**STATUS do RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-172"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="a8597-173">Vários códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="a8597-173">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a8597-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8597-174">Remarks</span></span>

<span data-ttu-id="a8597-175">O membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* deve conter um GUID de interface para uma interface de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="a8597-175">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="a8597-176">Uma lista de interfaces de LAN sem fio pode ser recuperada chamando a função [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="a8597-176">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

<span data-ttu-id="a8597-177">Os seguintes membros da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada por *pIntf* devem ser definidos como 0 antes de uma chamada para a função **WZCQueryInterface** : **RdSSID**, **rdBSSID** **, rdBSSIDList,** **rdStSSIDList** e **rdCtrlData**.</span><span class="sxs-lookup"><span data-stu-id="a8597-177">The following members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* must be set to 0 before a call to the **WZCQueryInterface** function: **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData**.</span></span>

<span data-ttu-id="a8597-178">O serviço de configuração zero sem fio não automotically atualizar o estado da mídia, mesmo quando a mídia conectada e os eventos desconectados são recebidos.</span><span class="sxs-lookup"><span data-stu-id="a8597-178">The Wireless Zero Configuration service does not automotically update media state, even when media connected and disconnected events are received.</span></span> <span data-ttu-id="a8597-179">Um aplicativo deve forçar uma atualização de estado de mídia chamando a função [**WZCRefreshInterface**](wzcrefreshinterface.md) antes de chamar a função **WZCQueryInterface** se o estado de mídia NDIS for solicitado (o \_ bit INTF NDISMEDIA será definido no parâmetro *dwInFlags* ).</span><span class="sxs-lookup"><span data-stu-id="a8597-179">An application should force a media state refresh by calling the [**WZCRefreshInterface**](wzcrefreshinterface.md) function before calling the **WZCQueryInterface** function if the NDIS media state is to be requested (the INTF\_NDISMEDIA bit will be set in the *dwInFlags* parameter).</span></span>

<span data-ttu-id="a8597-180">Quando o parâmetro *dwInFlags* contiver **INTF \_ BSSIDLIST**, a função **WZCQueryInterface** não definirá *dwOutFlags* com **INTF \_** BSSIDLIST se a lista de redes visível estiver vazia.</span><span class="sxs-lookup"><span data-stu-id="a8597-180">When the *dwInFlags* parameter contains **INTF\_BSSIDLIST**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_BSSIDLIST** if the visible list of networks is empty.</span></span> <span data-ttu-id="a8597-181">Quando o parâmetro *dwInFlags* contiver **INTF \_ SSID**, a função **WZCQueryInterface** não definirá o *dwOutFlags* com **INTF \_ SSID** se nenhum SSID estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="a8597-181">When the *dwInFlags* parameter contains **INTF\_SSID**, the **WZCQueryInterface** function does not set the *dwOutFlags* with **INTF\_SSID** if no SSID is available.</span></span>

<span data-ttu-id="a8597-182">Se a função **WZCQueryInterface** retornar o \_ êxito do erro, o chamador deverá chamar a função [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) com o parâmetro *pIntf* para liberar os buffers internos alocados para os dados retornados quando essas informações não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="a8597-182">If the **WZCQueryInterface** function returns ERROR\_SUCCESS, the caller should call the [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) function with the *pIntf* parameter to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span> <span data-ttu-id="a8597-183">Isso libera os buffers usados pelos membros **rdSSID**, **rdBSSID**, **rdBSSIDList**, **RdStSSIDList** e **RdCtrlData** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada por *pIntf* parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a8597-183">This releases the buffers used by the **rdSSID**, **rdBSSID**, **rdBSSIDList**, **rdStSSIDList**, and **rdCtrlData** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by *pIntf* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="a8597-184">O arquivo de cabeçalho *wzcsapi. h* e o arquivo de biblioteca de importação *wzcsapi. lib* não estão disponíveis no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="a8597-184">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a8597-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8597-185">Requirements</span></span>



| <span data-ttu-id="a8597-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8597-186">Requirement</span></span> | <span data-ttu-id="a8597-187">Valor</span><span class="sxs-lookup"><span data-stu-id="a8597-187">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8597-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8597-188">Minimum supported client</span></span><br/> | <span data-ttu-id="a8597-189">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="a8597-189">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8597-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8597-190">Minimum supported server</span></span><br/> | <span data-ttu-id="a8597-191">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a8597-191">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a8597-192">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a8597-192">End of client support</span></span><br/>    | <span data-ttu-id="a8597-193">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="a8597-193">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="a8597-194">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a8597-194">End of server support</span></span><br/>    | <span data-ttu-id="a8597-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a8597-195">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a8597-196">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8597-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8597-197"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-197"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8597-198">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8597-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8597-199"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-199"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8597-200">DLL</span><span class="sxs-lookup"><span data-stu-id="a8597-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8597-201"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8597-201"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8597-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8597-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8597-203">**\_entrada INTF**</span><span class="sxs-lookup"><span data-stu-id="a8597-203">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> <dt>

[<span data-ttu-id="a8597-204">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="a8597-204">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="a8597-205">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="a8597-205">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="a8597-206">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="a8597-206">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
