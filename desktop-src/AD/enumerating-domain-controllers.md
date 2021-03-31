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
# <a name="enumerating-domain-controllers"></a><span data-ttu-id="00caa-104">Enumerando controladores de domínio</span><span class="sxs-lookup"><span data-stu-id="00caa-104">Enumerating Domain Controllers</span></span>

<span data-ttu-id="00caa-105">Em versões anteriores do Windows, um aplicativo podia obter apenas um único controlador de domínio em um domínio chamando [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span><span class="sxs-lookup"><span data-stu-id="00caa-105">In earlier versions of Windows, an application could only obtain a single domain controller in a domain by calling [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea).</span></span> <span data-ttu-id="00caa-106">Não havia como prever qual controlador de domínio seria recuperado ou para obter uma lista dos controladores de domínio.</span><span class="sxs-lookup"><span data-stu-id="00caa-106">There was no way to predict which domain controller would be retrieved or to obtain a list of the domain controllers.</span></span> <span data-ttu-id="00caa-107">O Windows permite que um aplicativo enumere os controladores de domínio em um domínio usando as funções [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .</span><span class="sxs-lookup"><span data-stu-id="00caa-107">Windows enables an application to enumerate the domain controllers in a domain by using the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta), and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions.</span></span>

<span data-ttu-id="00caa-108">Para enumerar um controlador de domínio, chame [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span><span class="sxs-lookup"><span data-stu-id="00caa-108">To enumerate a domain controller, call [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena).</span></span> <span data-ttu-id="00caa-109">Essa função usa parâmetros que definem o domínio para enumerar e outras opções de enumeração.</span><span class="sxs-lookup"><span data-stu-id="00caa-109">This function takes parameters that define the domain to enumerate and other enumeration options.</span></span> <span data-ttu-id="00caa-110">**DsGetDcOpen** fornece um identificador de contexto de enumeração de domínio que é usado para identificar a operação de enumeração quando [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) e [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) são chamados.</span><span class="sxs-lookup"><span data-stu-id="00caa-110">**DsGetDcOpen** provides a domain enumeration context handle that is used to identify the enumeration operation when [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) and [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) are called.</span></span>

<span data-ttu-id="00caa-111">A função [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) é chamada com o identificador de contexto de enumeração de domínio para recuperar o próximo controlador de domínio na enumeração.</span><span class="sxs-lookup"><span data-stu-id="00caa-111">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function is called with the domain enumeration context handle to retrieve the next domain controller in the enumeration.</span></span> <span data-ttu-id="00caa-112">Na primeira vez que essa função é chamada, o primeiro controlador de domínio na enumeração é recuperado.</span><span class="sxs-lookup"><span data-stu-id="00caa-112">The first time this function is called, the first domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="00caa-113">Na segunda vez que essa função é chamada, o segundo controlador de domínio na enumeração é recuperado.</span><span class="sxs-lookup"><span data-stu-id="00caa-113">The second time this function is called, the second domain controller in the enumeration is retrieved.</span></span> <span data-ttu-id="00caa-114">Esse processo é repetido até que **DsGetDcNext** retorne **\_ um erro sem \_ mais \_ itens**, o que indica o fim da enumeração.</span><span class="sxs-lookup"><span data-stu-id="00caa-114">This process is repeated until **DsGetDcNext** returns **ERROR\_NO\_MORE\_ITEMS**, that indicates the end of the enumeration.</span></span>

<span data-ttu-id="00caa-115">A função [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) irá enumerar os controladores de domínio em dois grupos.</span><span class="sxs-lookup"><span data-stu-id="00caa-115">The [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) function will enumerate the domain controllers in two groups.</span></span> <span data-ttu-id="00caa-116">O primeiro grupo contém os controladores de domínio que abrangem o site do computador em que a função é executada e o segundo grupo contém os controladores de domínio que não abrangem o site do computador em que a função é executada.</span><span class="sxs-lookup"><span data-stu-id="00caa-116">The first group contains the domain controllers that cover the site of the computer where the function is executed and the second group contains the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="00caa-117">Se o sinalizador de **notificação do DS \_ \_ após \_ \_ registros do site** for especificado no parâmetro *OptionFlags* em [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), a função **DsGetDcNext** retornará o erro de marca de caixa de entrada **\_ \_ detectado** depois que todos os controladores de domínio específicos do site forem recuperados.</span><span class="sxs-lookup"><span data-stu-id="00caa-117">If the **DS\_NOTIFY\_AFTER\_SITE\_RECORDS** flag is specified in the *OptionFlags* parameter in [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), the **DsGetDcNext** function will return **ERROR\_FILEMARK\_DETECTED** after all of the site-specific domain controllers have been retrieved.</span></span> <span data-ttu-id="00caa-118">O **DsGetDcNext** começará a enumerar o segundo grupo, que contém todos os controladores de domínio no domínio, incluindo os controladores de domínio específicos do site contidos no primeiro grupo.</span><span class="sxs-lookup"><span data-stu-id="00caa-118">**DsGetDcNext** will then begin enumerating the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.</span></span>

<span data-ttu-id="00caa-119">Os controladores de domínio que manipulam o site do computador em que a função é executada são enumerados primeiro seguidos pelos controladores de domínio que não abrangem o site do computador em que a função é executada.</span><span class="sxs-lookup"><span data-stu-id="00caa-119">Domain controllers that handle the site of the computer where the function is executed are enumerated first followed by the domain controllers that do not cover the site of the computer where the function is executed.</span></span> <span data-ttu-id="00caa-120">Um controlador de domínio é considerado para cobrir um site se o controlador de domínio estiver configurado para residir nesse site ou se o controlador de domínio residir em um site mais próximo do site em questão em termos do custo do link entre sites configurado.</span><span class="sxs-lookup"><span data-stu-id="00caa-120">A domain controller is said to cover a site if the domain controller is configured to reside in that site or if the domain controller resides in a site that is nearest to the site in question in terms of the configured inter-site link cost.</span></span> <span data-ttu-id="00caa-121">Se houver controladores de domínio no grupo de controladores de domínio que abrangem e no grupo de controladores de domínio que não abrangem o site do computador, os controladores de domínio serão retornados dentro do grupo em ordem de suas prioridades e pesos configurados especificados no DNS.</span><span class="sxs-lookup"><span data-stu-id="00caa-121">If there are any domain controllers in both the group of domain controllers that cover and the group of domain controllers that do not cover the computer site, domain controllers are returned within the group in order of their configured priorities and weights that are specified in DNS.</span></span> <span data-ttu-id="00caa-122">Controladores de domínio que têm prioridade numérica mais baixa são retornados primeiro em um grupo.</span><span class="sxs-lookup"><span data-stu-id="00caa-122">Domain controllers that have lower numeric priority are returned within a group first.</span></span> <span data-ttu-id="00caa-123">Se dentro de um grupo relacionado a sites houver um subgrupo de vários controladores de domínio com a mesma prioridade, os controladores de domínio serão retornados em uma ordem aleatória ponderada em que os controladores de domínio com peso mais alto têm mais probabilidade de serem retornados primeiro.</span><span class="sxs-lookup"><span data-stu-id="00caa-123">If within a site-related group there is a subgroup of several domain controllers with the same priority, domain controllers are returned in a weighted random order where domain controllers with higher weight have more probability to be returned first.</span></span> <span data-ttu-id="00caa-124">Os sites, as prioridades e os pesos são configurados pelo administrador de domínio para alcançar o desempenho efetivo e o balanceamento de carga entre vários controladores de domínio disponíveis no domínio.</span><span class="sxs-lookup"><span data-stu-id="00caa-124">The sites, priorities, and weights are configured by the domain administrator to achieve effective performance and load balancing among multiple domain controllers available in the domain.</span></span> <span data-ttu-id="00caa-125">Por isso, os aplicativos que usam as funções [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aproveitam automaticamente essas otimizações.</span><span class="sxs-lookup"><span data-stu-id="00caa-125">Because of this, applications that use the [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)/[**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)/[**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) functions automatically take advantage of these optimizations.</span></span>

<span data-ttu-id="00caa-126">Quando a enumeração é concluída ou não é mais necessária, a enumeração deve ser fechada chamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) com o identificador de contexto de enumeração de domínio.</span><span class="sxs-lookup"><span data-stu-id="00caa-126">When the enumeration is complete or is no longer required, the enumeration must be closed by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) with the domain enumeration context handle.</span></span>

<span data-ttu-id="00caa-127">Para redefinir a enumeração, é necessário fechar a enumeração atual chamando [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) e, em seguida, reabrir a enumeração chamando [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) novamente.</span><span class="sxs-lookup"><span data-stu-id="00caa-127">To reset the enumeration, it is necessary to close the current enumeration by calling [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) and then reopen the enumeration by calling [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) again.</span></span>

## <a name="example"></a><span data-ttu-id="00caa-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="00caa-128">Example</span></span>

<span data-ttu-id="00caa-129">O exemplo de código a seguir mostra como usar essas funções para enumerar os controladores de domínio no domínio local.</span><span class="sxs-lookup"><span data-stu-id="00caa-129">The following code example shows how to use these functions to enumerate the domain controllers in the local domain.</span></span>


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



 

 




