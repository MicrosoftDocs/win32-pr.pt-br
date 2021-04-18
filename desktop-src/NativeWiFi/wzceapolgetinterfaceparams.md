---
description: Obtém parâmetros de configuração EAPOL para a interface LAN sem fio especificada.
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: Função WZCEapolGetInterfaceParams (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: bc89fd2defb75662fa90b5ed00c7969d483da590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785406"
---
# <a name="wzceapolgetinterfaceparams-function"></a><span data-ttu-id="c784d-103">Função WZCEapolGetInterfaceParams</span><span class="sxs-lookup"><span data-stu-id="c784d-103">WZCEapolGetInterfaceParams function</span></span>

<span data-ttu-id="c784d-104">\[O **WZCEapolGetInterfaceParams** não é mais suportado a partir do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c784d-104">\[**WZCEapolGetInterfaceParams** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="c784d-105">Em vez disso, use a [API Wi-Fi nativa](native-wifi-reference.md), que fornece funcionalidade semelhante.</span><span class="sxs-lookup"><span data-stu-id="c784d-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="c784d-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="c784d-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="c784d-107">A função **WZCEapolGetInterfaceParams** Obtém parâmetros de configuração EAPOL para a interface LAN sem fio especificada.</span><span class="sxs-lookup"><span data-stu-id="c784d-107">The **WZCEapolGetInterfaceParams** function gets EAPOL configuration parameters for the specified wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c784d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c784d-108">Syntax</span></span>


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a><span data-ttu-id="c784d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c784d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c784d-110">*pSrvAddr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c784d-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c784d-111">Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função.</span><span class="sxs-lookup"><span data-stu-id="c784d-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="c784d-112">Se esse parâmetro for **nulo**, o serviço de configuração sem fio será chamado no computador local.</span><span class="sxs-lookup"><span data-stu-id="c784d-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="c784d-113">Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="c784d-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="c784d-114">*pwszGuid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c784d-114">*pwszGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c784d-115">O GUID da interface para a qual os dados serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="c784d-115">The GUID of the interface for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c784d-116">*dwSizeOfSSID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c784d-116">*dwSizeOfSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c784d-117">O tamanho do identificador de rede para o qual os dados serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="c784d-117">The size of the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c784d-118">*pbSSID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c784d-118">*pbSSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c784d-119">Um ponteiro para o identificador de rede para o qual os dados serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="c784d-119">A pointer to the network identifier for which data is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c784d-120">*pIntfParams* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="c784d-120">*pIntfParams* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c784d-121">Um ponteiro para uma estrutura de [**\_ \_ parâmetros de INTF de EAPOL**](eapol-intf-params.md) que contém parâmetros de interface.</span><span class="sxs-lookup"><span data-stu-id="c784d-121">A pointer to a [**EAPOL\_INTF\_PARAMS**](eapol-intf-params.md) structure that contains interface parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c784d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c784d-122">Return value</span></span>

<span data-ttu-id="c784d-123">Retorna o \_ êxito do erro se a operação for concluída com êxito; caso contrário, retorna um dos códigos de erro do sistema do Windows.</span><span class="sxs-lookup"><span data-stu-id="c784d-123">Returns ERROR\_SUCCESS if the operation completes successfully; otherwise, returns one of the Windows system error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="c784d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c784d-124">Remarks</span></span>

<span data-ttu-id="c784d-125">Se o **WZCEapolGetInterfaceParams** retornar o \_ êxito do erro, o chamador deverá chamar [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar os buffers internos alocados para os dados retornados quando essas informações não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="c784d-125">If the **WZCEapolGetInterfaceParams** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="c784d-126">O arquivo de cabeçalho *wzcsapi. h* e o arquivo de biblioteca de importação *wzcsapi. lib* não estão disponíveis no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c784d-126">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c784d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c784d-127">Requirements</span></span>



| <span data-ttu-id="c784d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c784d-128">Requirement</span></span> | <span data-ttu-id="c784d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="c784d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c784d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c784d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c784d-131">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="c784d-131">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c784d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c784d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c784d-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c784d-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c784d-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="c784d-134">End of client support</span></span><br/>    | <span data-ttu-id="c784d-135">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="c784d-135">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="c784d-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c784d-136">End of server support</span></span><br/>    | <span data-ttu-id="c784d-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c784d-137">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="c784d-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c784d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c784d-139"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c784d-139"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="c784d-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c784d-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="c784d-141"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c784d-141"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c784d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c784d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c784d-143"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c784d-143"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c784d-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="c784d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c784d-145">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="c784d-145">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="c784d-146">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="c784d-146">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="c784d-147">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="c784d-147">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
