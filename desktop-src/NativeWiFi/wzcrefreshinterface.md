---
description: Atualiza informações de interface para uma interface LAN sem fio específica.
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: Função WZCRefreshInterface (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297271"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="8a286-103">Função WZCRefreshInterface</span><span class="sxs-lookup"><span data-stu-id="8a286-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="8a286-104">\[Não há suporte para **WZCRefreshInterface** a partir do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8a286-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8a286-105">Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="8a286-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="8a286-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="8a286-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="8a286-107">A função **WZCRefreshInterface** atualiza informações de interface para uma interface LAN sem fio específica.</span><span class="sxs-lookup"><span data-stu-id="8a286-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a286-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a286-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8a286-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8a286-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a286-110">*pSrvAddr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a286-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a286-111">Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função.</span><span class="sxs-lookup"><span data-stu-id="8a286-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="8a286-112">Se esse parâmetro for **nulo**, o serviço de configuração sem fio será chamado no computador local.</span><span class="sxs-lookup"><span data-stu-id="8a286-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="8a286-113">Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="8a286-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="8a286-114">*dwInFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a286-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a286-115">Um conjunto de campos a ser atualizado junto com as ações de atualização específicas a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="8a286-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="8a286-116">Esse é um bitmask que pode conter qualquer combinação dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a286-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="8a286-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8a286-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="8a286-118">Significado</span><span class="sxs-lookup"><span data-stu-id="8a286-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="8a286-119"><dt>**INTF \_**</dt> <dt>0X00010000</dt> de descr</span><span class="sxs-lookup"><span data-stu-id="8a286-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="8a286-120">Atualize a descrição da interface para uma interface de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="8a286-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="8a286-121">A descrição da interface atualizada pode ser recuperada chamando-se a função [**WZCQueryInterface**](wzcqueryinterface.md) com o bit **\_ descr INTF** definido no parâmetro *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="8a286-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="8a286-122">A descrição da interface é retornada no membro **wszDescr** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *PIntf* que é retornado pela função **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="8a286-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="8a286-123"><dt>**INTF \_ NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="8a286-124">Atualize as informações de mídia do NDIS para uma interface de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="8a286-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="8a286-125">As informações de mídia NDIS atualizadas podem ser recuperadas chamando a função [**WZCQueryInterface**](wzcqueryinterface.md) com o bit **INTF \_ NDISMEDIA** definido no parâmetro *dwInFlags* .</span><span class="sxs-lookup"><span data-stu-id="8a286-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="8a286-126">As informações de mídia do NDIS são retornadas nos membros **ulMediaState**, **ulMediaType** e **UlPhysicalMediaType** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* que é retornado pela função **WZCQueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="8a286-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="8a286-127"><dt>**INTF \_ Todos os \_ OIDs**</dt> <dt>0xFFF00000</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="8a286-128">Atualize todos os OIDs de NDIS para uma interface de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="8a286-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="8a286-129">Esta opção atualiza a maioria dos dados para uma interface de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="8a286-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="8a286-130">As informações atualizadas podem ser recuperadas chamando a função [**WZCQueryInterface**](wzcqueryinterface.md) .</span><span class="sxs-lookup"><span data-stu-id="8a286-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="8a286-131">*pIntf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8a286-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a286-132">Um ponteiro para uma estrutura de [**\_ entrada INTF**](intf-entry.md) que contém a chave da interface a ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="8a286-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="8a286-133">*pdwOutFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="8a286-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a286-134">Um conjunto de campos que foram atualizados com êxito.</span><span class="sxs-lookup"><span data-stu-id="8a286-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a286-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8a286-135">Return value</span></span>

<span data-ttu-id="8a286-136">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="8a286-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8a286-137">Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a286-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="8a286-138">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8a286-138">Return code</span></span>                                                                                              | <span data-ttu-id="8a286-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="8a286-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8a286-140"><dt>**Arena de erro em \_ \_ Trash**</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="8a286-141">Os blocos de controle de armazenamento foram destruídos.</span><span class="sxs-lookup"><span data-stu-id="8a286-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="8a286-142">Esse erro será retornado se o serviço de configuração zero sem fio não tiver inicializado objetos internos.</span><span class="sxs-lookup"><span data-stu-id="8a286-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="8a286-143"><dt>**arquivo de erro \_ \_ não \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="8a286-144">O sistema não pode encontrar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="8a286-144">The system cannot find the file specified.</span></span> <span data-ttu-id="8a286-145">Esse erro será retornado se o GUID no membro **wszGuid** da estrutura de [**\_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* não coincidir com nenhuma das interfaces de LAN sem fio no computador local.</span><span class="sxs-lookup"><span data-stu-id="8a286-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="8a286-146"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="8a286-147">Um parâmetro está incorreto.</span><span class="sxs-lookup"><span data-stu-id="8a286-147">A parameter is incorrect.</span></span> <span data-ttu-id="8a286-148">Esse erro será retornado se o parâmetro *pIntf* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8a286-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="8a286-149">Esse erro será retornado se o membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8a286-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="8a286-150"><dt>**STATUS do RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="8a286-151">Vários códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="8a286-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="8a286-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a286-152">Remarks</span></span>

<span data-ttu-id="8a286-153">O membro **wszGuid** da estrutura [**de \_ entrada INTF**](intf-entry.md) apontada pelo parâmetro *pIntf* deve conter um GUID de interface para uma interface de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="8a286-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="8a286-154">Uma lista de interfaces de LAN sem fio pode ser recuperada chamando a função [**WZCEnumInterfaces**](wzcenuminterfaces.md) .</span><span class="sxs-lookup"><span data-stu-id="8a286-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="8a286-155">O arquivo de cabeçalho *wzcsapi. h* e o arquivo de biblioteca de importação *wzcsapi. lib* não estão disponíveis no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8a286-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8a286-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a286-156">Requirements</span></span>



| <span data-ttu-id="8a286-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a286-157">Requirement</span></span> | <span data-ttu-id="8a286-158">Valor</span><span class="sxs-lookup"><span data-stu-id="8a286-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a286-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a286-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8a286-160">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="8a286-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a286-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a286-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8a286-162">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8a286-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a286-163">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="8a286-163">End of client support</span></span><br/>    | <span data-ttu-id="8a286-164">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="8a286-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="8a286-165">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="8a286-165">End of server support</span></span><br/>    | <span data-ttu-id="8a286-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8a286-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="8a286-167">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8a286-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a286-168"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a286-169">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a286-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a286-170"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8a286-171">DLL</span><span class="sxs-lookup"><span data-stu-id="8a286-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a286-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a286-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a286-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a286-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a286-174">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="8a286-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="8a286-175">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="8a286-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="8a286-176">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="8a286-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="8a286-177">**\_entrada INTF**</span><span class="sxs-lookup"><span data-stu-id="8a286-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




