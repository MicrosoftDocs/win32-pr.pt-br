---
description: A função GetInterfaceInfo preenche um ponteiro para uma estrutura IP INTERFACE INFO com informações sobre \_ \_ as interfaces associadas ao sistema.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Gerenciando interfaces usando GetInterfaceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2afa6fe0b520e1cc5f952b44bc94052b630f4335bd739b4d7c3582d16e277
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146739"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a>Gerenciando interfaces usando GetInterfaceInfo

A [**função GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) preenche um ponteiro para uma estrutura [**IP INTERFACE \_ \_ INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) com informações sobre as interfaces associadas ao sistema.

**Para usar GetInterfaceInfo**

1.  Declare um ponteiro para um [**objeto IP \_ INTERFACE \_ INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) chamado `pInfo` e um objeto **ULONG** chamado `ulOutBufLen` . Declare também um **objeto DWORD** chamado `dwRetVal` (usado para verificação de erros).
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  Alocar memória para as estruturas.
    > [!Note]  
    > O tamanho de `ulOutBufLen` não é suficiente para manter as informações. Consulte a próxima etapa.

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  Faça uma chamada inicial para [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) para obter o tamanho necessário para a `ulOutBufLen` variável.
    > [!Note]  
    > Essa chamada para a função deve falhar e é usada para garantir que a variável especifique um tamanho suficiente para manter todas as `ulOutBufLen` informações retornadas para `pInfo` . Esse é um modelo de programação comum no Auxiliar de IP para estruturas de dados e funções desse tipo.

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  Faça uma segunda chamada para [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) com verificação de erro geral e retorne seu valor para a variável **DWORD** (para verificação de `dwRetVal` erro mais avançada).
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  Se a chamada foi bem-sucedida, acesse os dados da estrutura `pInfo` de dados.

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
    > O %ws na primeira linha denota uma cadeia de caracteres larga. Isso é usado porque o **atributo Name** da estrutura IP ADAPTER [**INDEX \_ \_ \_ MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) é um `Adapter` **WCHAR**, que é uma cadeia de caracteres Unicode.

     

6.  Liberar qualquer memória alocada para a estrutura *pInfo.*
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

Próxima etapa: [gerenciando endereços IP usando GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)

Etapa anterior: [gerenciando adaptadores de rede usando GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)

 

 



