---
description: Enumera todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração zero sem fio.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: Função WZCEnumInterfaces (wzcsapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829780"
---
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="90c6f-103">Função WZCEnumInterfaces</span><span class="sxs-lookup"><span data-stu-id="90c6f-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="90c6f-104">\[O **WZCEnumInterfaces** não é mais suportado a partir do Windows Vista e do windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="90c6f-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="90c6f-105">Em vez disso, use a função [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) .</span><span class="sxs-lookup"><span data-stu-id="90c6f-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="90c6f-106">Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="90c6f-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="90c6f-107">A função **WZCEnumInterfaces** enumera todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração zero sem fio.</span><span class="sxs-lookup"><span data-stu-id="90c6f-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="90c6f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90c6f-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="90c6f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90c6f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90c6f-110">*pSrvAddr* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="90c6f-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90c6f-111">Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função.</span><span class="sxs-lookup"><span data-stu-id="90c6f-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="90c6f-112">Se esse parâmetro for **nulo**, o serviço de configuração zero sem fio será enumerado no computador local.</span><span class="sxs-lookup"><span data-stu-id="90c6f-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="90c6f-113">Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="90c6f-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="90c6f-114">*pIntfs* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="90c6f-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90c6f-115">Um ponteiro para uma estrutura de [**\_ \_ tabela de chave INTFS**](intfs-key-table.md) que contém uma tabela de informações de chave para todas as interfaces.</span><span class="sxs-lookup"><span data-stu-id="90c6f-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90c6f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90c6f-116">Return value</span></span>

<span data-ttu-id="90c6f-117">Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.</span><span class="sxs-lookup"><span data-stu-id="90c6f-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="90c6f-118">Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.</span><span class="sxs-lookup"><span data-stu-id="90c6f-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="90c6f-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="90c6f-119">Return code</span></span>                                                                                               | <span data-ttu-id="90c6f-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="90c6f-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="90c6f-121"><dt>**Arena de erro em \_ \_ Trash**</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="90c6f-122">Os blocos de controle de armazenamento foram destruídos.</span><span class="sxs-lookup"><span data-stu-id="90c6f-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="90c6f-123">Esse erro será retornado se o serviço de configuração zero sem fio não tiver inicializado objetos internos.</span><span class="sxs-lookup"><span data-stu-id="90c6f-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="90c6f-124"><dt>**RPC \_ S \_ desconhecido \_ se**</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="90c6f-125">A interface é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="90c6f-125">The interface is unknown.</span></span><br/> <span data-ttu-id="90c6f-126">Esse erro será retornado se o serviço de configuração zero sem fio não for iniciado.</span><span class="sxs-lookup"><span data-stu-id="90c6f-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="90c6f-127"><dt>**ponteiro de referência de RPC \_ X \_ nulo \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="90c6f-128">Um ponteiro de referência nulo foi passado para o stub.</span><span class="sxs-lookup"><span data-stu-id="90c6f-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="90c6f-129">Esse erro será retornado se o parâmetro *pIntfs* for **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90c6f-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="90c6f-130"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="90c6f-131">Não há memória suficiente disponível para processar essa solicitação e alocar memória para os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="90c6f-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="90c6f-132"><dt>**STATUS do RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="90c6f-133">Vários códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="90c6f-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="90c6f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="90c6f-134">Remarks</span></span>

<span data-ttu-id="90c6f-135">O membro **dwNumIntfs** da estrutura [**da \_ \_ tabela de chave INTFS**](intfs-key-table.md) apontada por *pIntf* deve ser definido como 0 antes de chamar a função **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="90c6f-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="90c6f-136">Além disso, o membro **pIntfs** deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="90c6f-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="90c6f-137">Para chamadas subsequentes para outras funções de configuração sem fio zero, um aplicativo deve identificar a interface na qual está operando fornecendo informações de chave relevantes retornadas pela função **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="90c6f-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="90c6f-138">Se o **WZCEnumInterfaces** retornar o \_ êxito do erro, o chamador deverá chamar [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar os buffers internos alocados para os dados retornados quando essas informações não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="90c6f-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="90c6f-139">O arquivo de cabeçalho *wzcsapi. h* e o arquivo de biblioteca de importação *wzcsapi. lib* não estão disponíveis no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="90c6f-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="90c6f-140">Exemplos</span><span class="sxs-lookup"><span data-stu-id="90c6f-140">Examples</span></span>

<span data-ttu-id="90c6f-141">O exemplo a seguir enumera as interfaces de LAN sem fio no computador local gerenciado pelo serviço de configuração zero sem fio e imprime o valor de GUID de interface para cada interface.</span><span class="sxs-lookup"><span data-stu-id="90c6f-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="90c6f-142">Este exemplo falhará no Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="90c6f-142">This example will fail on Windows Vista and later .</span></span>

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="90c6f-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90c6f-143">Requirements</span></span>



| <span data-ttu-id="90c6f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="90c6f-144">Requirement</span></span> | <span data-ttu-id="90c6f-145">Valor</span><span class="sxs-lookup"><span data-stu-id="90c6f-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90c6f-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90c6f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="90c6f-147">\[Somente aplicativos de área de trabalho do Windows XP com SP2\]</span><span class="sxs-lookup"><span data-stu-id="90c6f-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90c6f-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90c6f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="90c6f-149">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90c6f-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90c6f-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="90c6f-150">End of client support</span></span><br/>    | <span data-ttu-id="90c6f-151">Windows XP com SP3</span><span class="sxs-lookup"><span data-stu-id="90c6f-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="90c6f-152">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="90c6f-152">End of server support</span></span><br/>    | <span data-ttu-id="90c6f-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="90c6f-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="90c6f-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90c6f-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="90c6f-155"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="90c6f-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90c6f-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="90c6f-157"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="90c6f-158">DLL</span><span class="sxs-lookup"><span data-stu-id="90c6f-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90c6f-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90c6f-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90c6f-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="90c6f-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90c6f-161">**\_tabela de chave INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="90c6f-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="90c6f-162">**\_entrada de chave INTF \_**</span><span class="sxs-lookup"><span data-stu-id="90c6f-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="90c6f-163">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="90c6f-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="90c6f-164">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="90c6f-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="90c6f-165">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="90c6f-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
