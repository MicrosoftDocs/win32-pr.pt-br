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
# <a name="wzcenuminterfaces-function"></a>Função WZCEnumInterfaces

\[O **WZCEnumInterfaces** não é mais suportado a partir do Windows Vista e do windows Server 2008. Em vez disso, use a função [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) . Para obter mais informações, consulte [sobre a API Wi-Fi nativa](about-the-native-wifi-api.md).\]

A função **WZCEnumInterfaces** enumera todas as interfaces de LAN sem fio gerenciadas pelo serviço de configuração zero sem fio.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSrvAddr* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do computador no qual executar essa função. Se esse parâmetro for **nulo**, o serviço de configuração zero sem fio será enumerado no computador local.

Se o parâmetro *pSrvAddr* especificado for um computador remoto, o computador remoto deverá dar suporte a chamadas RPC remotas.

</dd> <dt>

*pIntfs* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ \_ tabela de chave INTFS**](intfs-key-table.md) que contém uma tabela de informações de chave para todas as interfaces.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

Se a função falhar, o valor de retorno poderá ser um dos códigos de retorno a seguir.



| Código de retorno                                                                                               | Descrição                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Arena de erro em \_ \_ Trash**</dt> </dl>      | Os blocos de controle de armazenamento foram destruídos. Esse erro será retornado se o serviço de configuração zero sem fio não tiver inicializado objetos internos.<br/> |
| <dl> <dt>**RPC \_ S \_ desconhecido \_ se**</dt> </dl>        | A interface é desconhecida.<br/> Esse erro será retornado se o serviço de configuração zero sem fio não for iniciado.<br/>                             |
| <dl> <dt>**ponteiro de referência de RPC \_ X \_ nulo \_ \_**</dt> </dl> | Um ponteiro de referência nulo foi passado para o stub.<br/> Esse erro será retornado se o parâmetro *pIntfs* for **nulo**.<br/>                          |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl> | Não há memória suficiente disponível para processar essa solicitação e alocar memória para os resultados da consulta.<br/>                                                  |
| <dl> <dt>**STATUS do RPC \_**</dt> </dl>                | Vários códigos de erro.<br/>                                                                                                                               |



 

## <a name="remarks"></a>Comentários

O membro **dwNumIntfs** da estrutura [**da \_ \_ tabela de chave INTFS**](intfs-key-table.md) apontada por *pIntf* deve ser definido como 0 antes de chamar a função **WZCEnumInterfaces** . Além disso, o membro **pIntfs** deve ser definido como **nulo**.

Para chamadas subsequentes para outras funções de configuração sem fio zero, um aplicativo deve identificar a interface na qual está operando fornecendo informações de chave relevantes retornadas pela função **WZCEnumInterfaces** .

Se o **WZCEnumInterfaces** retornar o \_ êxito do erro, o chamador deverá chamar [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar os buffers internos alocados para os dados retornados quando essas informações não forem mais necessárias.

> [!Note]  
> O arquivo de cabeçalho *wzcsapi. h* e o arquivo de biblioteca de importação *wzcsapi. lib* não estão disponíveis no SDK do Windows.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir enumera as interfaces de LAN sem fio no computador local gerenciado pelo serviço de configuração zero sem fio e imprime o valor de GUID de interface para cada interface.

> [!Note]  
> Este exemplo falhará no Windows Vista e posterior.

 


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows XP com SP2\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| Fim do suporte do cliente<br/>    | Windows XP com SP3<br/>                                                         |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_tabela de chave INTFS \_**](intfs-key-table.md)
</dt> <dt>

[**\_entrada de chave INTF \_**](intf-key-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
