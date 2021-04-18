---
description: A função GetInterfaceInfo preenche um ponteiro para uma \_ estrutura de informações de interface IP \_ com informações sobre as interfaces associadas ao sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gerenciando interfaces usando o GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811024"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Gerenciando interfaces usando o GetInterfaceInfo

A função [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) preenche um ponteiro para uma estrutura de [**\_ \_ informações de interface IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) com informações sobre as interfaces associadas ao sistema.

**Para usar o GetInterfaceInfo**

1.  Declare um ponteiro para um objeto de [**\_ \_ informações de interface IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) chamado `pInfo` e um objeto **ULONG** chamado `ulOutBufLen` . Declare também um objeto **DWORD** chamado `dwRetVal` (usado para verificação de erro).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Aloque memória para as estruturas.
    > [!Note]  
    > O tamanho de `ulOutBufLen` não é suficiente para manter as informações. Consulte a próxima etapa.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Faça uma chamada inicial para [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) para obter o tamanho necessário na `ulOutBufLen` variável.
    > [!Note]  
    > Essa chamada para a função é destinada a falhar e é usada para garantir que a `ulOutBufLen` variável especifique um tamanho suficiente para manter todas as informações retornadas para `pInfo` . Este é um modelo de programação comum no auxiliar de IP para estruturas de dados e funções desse tipo.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Faça uma segunda chamada para [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) com verificação de erro geral e retorne seu valor para a variável **DWORD** `dwRetVal` (para verificação de erros mais avançada).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Se a chamada foi bem-sucedida, acesse os dados da `pInfo` estrutura de dados.

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > O% WS na primeira linha denota uma cadeia de caracteres larga. Isso é usado porque o atributo **Name** da estrutura [**do \_ \_ \_ mapa do índice do adaptador IP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) `Adapter` é um **WCHAR**, que é uma cadeia de caracteres Unicode.

     

6.  Libere qualquer memória alocada para a estrutura *pInfo* .
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Próxima etapa: [Gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Etapa anterior: [Gerenciando adaptadores de rede usando GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



