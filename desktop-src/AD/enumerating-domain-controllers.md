---
title: Enumerando controladores de domínio
description: Em versões anteriores do Windows, um aplicativo podia obter apenas um único controlador de domínio em um domínio chamando DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory exemplos Active Directory, enumerando os controladores de domínio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634967"
---
# <a name="enumerating-domain-controllers"></a>Enumerando controladores de domínio

Em versões anteriores do Windows, um aplicativo podia obter apenas um único controlador de domínio em um domínio chamando [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). Não havia como prever qual controlador de domínio seria recuperado ou para obter uma lista dos controladores de domínio. O Windows permite que um aplicativo enumere os controladores de domínio em um domínio usando as funções [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Para enumerar um controlador de domínio, chame [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena). Essa função usa parâmetros que definem o domínio para enumerar e outras opções de enumeração. **DsGetDcOpen** fornece um identificador de contexto de enumeração de domínio que é usado para identificar a operação de enumeração quando [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) são chamados.

A função [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) é chamada com o identificador de contexto de enumeração de domínio para recuperar o próximo controlador de domínio na enumeração. Na primeira vez que essa função é chamada, o primeiro controlador de domínio na enumeração é recuperado. Na segunda vez que essa função é chamada, o segundo controlador de domínio na enumeração é recuperado. Esse processo é repetido até que **DsGetDcNext** retorne **\_ um erro sem \_ mais \_ itens**, o que indica o fim da enumeração.

A função [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) irá enumerar os controladores de domínio em dois grupos. O primeiro grupo contém os controladores de domínio que abrangem o site do computador em que a função é executada e o segundo grupo contém os controladores de domínio que não abrangem o site do computador em que a função é executada. Se o sinalizador de **notificação do DS \_ \_ após \_ \_ registros do site** for especificado no parâmetro *OptionFlags* em [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), a função **DsGetDcNext** retornará o erro de marca de caixa de entrada **\_ \_ detectado** depois que todos os controladores de domínio específicos do site forem recuperados. O **DsGetDcNext** começará a enumerar o segundo grupo, que contém todos os controladores de domínio no domínio, incluindo os controladores de domínio específicos do site contidos no primeiro grupo.

Os controladores de domínio que manipulam o site do computador em que a função é executada são enumerados primeiro seguidos pelos controladores de domínio que não abrangem o site do computador em que a função é executada. Um controlador de domínio é considerado para cobrir um site se o controlador de domínio estiver configurado para residir nesse site ou se o controlador de domínio residir em um site mais próximo do site em questão em termos do custo do link entre sites configurado. Se houver controladores de domínio no grupo de controladores de domínio que abrangem e no grupo de controladores de domínio que não abrangem o site do computador, os controladores de domínio serão retornados dentro do grupo em ordem de suas prioridades e pesos configurados especificados no DNS. Controladores de domínio que têm prioridade numérica mais baixa são retornados primeiro em um grupo. Se dentro de um grupo relacionado a sites houver um subgrupo de vários controladores de domínio com a mesma prioridade, os controladores de domínio serão retornados em uma ordem aleatória ponderada em que os controladores de domínio com peso mais alto têm mais probabilidade de serem retornados primeiro. Os sites, as prioridades e os pesos são configurados pelo administrador de domínio para alcançar o desempenho efetivo e o balanceamento de carga entre vários controladores de domínio disponíveis no domínio. Por isso, os aplicativos que usam as funções [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aproveitam automaticamente essas otimizações.

Quando a enumeração é concluída ou não é mais necessária, a enumeração deve ser fechada chamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) com o identificador de contexto de enumeração de domínio.

Para redefinir a enumeração, é necessário fechar a enumeração atual chamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) e, em seguida, reabrir a enumeração chamando [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) novamente.

## <a name="example"></a>Exemplo

O exemplo de código a seguir mostra como usar essas funções para enumerar os controladores de domínio no domínio local.


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




