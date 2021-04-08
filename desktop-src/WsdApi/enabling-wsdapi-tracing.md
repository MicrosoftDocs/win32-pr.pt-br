---
description: Os logs de WSDAPI contêm informações de depuração que podem ser usadas para encontrar a causa raiz das falhas do aplicativo WSDAPI.
ms.assetid: 28b4c032-1c9a-4b3a-9a6a-2948456572b2
title: Habilitando o rastreamento WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951f8ddfee6043cc662a456c70960e78ed1a3625
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010812"
---
# <a name="enabling-wsdapi-tracing"></a><span data-ttu-id="ee126-103">Habilitando o rastreamento WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ee126-103">Enabling WSDAPI Tracing</span></span>

<span data-ttu-id="ee126-104">Os logs de WSDAPI contêm informações de depuração que podem ser usadas para encontrar a causa raiz das falhas do aplicativo WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ee126-104">WSDAPI logs contain debugging information that can be used to find the root cause of WSDAPI application failures.</span></span> <span data-ttu-id="ee126-105">Quando o rastreamento está habilitado, as informações de log são armazenadas em um arquivo. etl em um local especificado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ee126-105">When tracing is enabled, logging information is stored in an .etl file in a user-specified location.</span></span> <span data-ttu-id="ee126-106">Esse arquivo. etl pode ser enviado para o suporte do desenvolvedor da Microsoft para análise da causa raiz.</span><span class="sxs-lookup"><span data-stu-id="ee126-106">This .etl file can be sent to Microsoft developer support for root cause analysis.</span></span> <span data-ttu-id="ee126-107">Para obter informações sobre como contatar o suporte, acesse [https://support.microsoft.com](https://support.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="ee126-107">For information about contacting support, go to [https://support.microsoft.com](https://support.microsoft.com).</span></span>

<span data-ttu-id="ee126-108">Esse procedimento deve ser feito duas vezes: uma vez no cliente e uma vez no host.</span><span class="sxs-lookup"><span data-stu-id="ee126-108">This procedure must be done twice: once on the client, and once on the host.</span></span>

<span data-ttu-id="ee126-109">**Para habilitar o rastreamento WSDAPI**</span><span class="sxs-lookup"><span data-stu-id="ee126-109">**To enable WSDAPI tracing**</span></span>

1.  <span data-ttu-id="ee126-110">Usando o bloco de notas ou outro editor de texto, crie um arquivo de texto com o seguinte texto:</span><span class="sxs-lookup"><span data-stu-id="ee126-110">Using Notepad or another text editor, create a text file with the following text:</span></span>

    ``` syntax
    "{480217a9-f824-4bd4-bbe8-f371caaf9a0d}" 0xFF 0xFF
    "{649e3596-2620-4d58-a01f-17aefe8185db}" 0xFF 0xFF
    "{96ab095a-9519-4f5c-81ee-c510b0a45463}" 0xFF 0xFF
    "{f9be9c98-10db-4318-bb61-cb0ddea08bf7}" 0xFF 0xFF
    "{db1d0418-105a-4c77-9a25-8f96a19716a4}" 0xFF 0xFF
    "{7e2dbfc7-41e8-4987-bca7-76cadfad765f}" 0xFF 0xFF
    "{8b20d3e4-581f-4a27-8109-df01643a7a93}" 0xFF 0xFF
    "{6d04bf88-60a5-4d02-bc5c-94a20ba490ec}" 0xFF 0xFF
    "{75454210-b231-4fea-b2b4-2cc66d7ae8aa}" 0xFF 0xFF
    "{e176aa66-5cc8-4321-9624-f9c1d2b7bf06}" 0xFF 0xFF
    "{836767a6-af31-4938-b4c0-ef86749a9aef}" 0xFF 0xFF
    ```

2.  <span data-ttu-id="ee126-111">Salve o arquivo de texto como `C:\temp\traceguids.txt` e feche o arquivo.</span><span class="sxs-lookup"><span data-stu-id="ee126-111">Save the text file as `C:\temp\traceguids.txt` and then close the file.</span></span>
3.  <span data-ttu-id="ee126-112">Abra uma janela de prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="ee126-112">Open an elevated command prompt window.</span></span>
4.  <span data-ttu-id="ee126-113">Execute o seguinte comando: **logman.exe Create Trace wsdlog-o c: \\ temp \\ WSD**</span><span class="sxs-lookup"><span data-stu-id="ee126-113">Run the following command: **logman.exe create trace wsdlog -o c:\\temp\\wsd**</span></span>
5.  <span data-ttu-id="ee126-114">Execute o seguinte comando: **logman.exe Update wsdlog-PF c: \\ temp \\traceguids.txt**</span><span class="sxs-lookup"><span data-stu-id="ee126-114">Run the following command: **logman.exe update wsdlog -pf c:\\temp\\traceguids.txt**</span></span>
6.  <span data-ttu-id="ee126-115">Execute o seguinte comando: **logman.exe Start wsdlog**</span><span class="sxs-lookup"><span data-stu-id="ee126-115">Run the following command: **logman.exe start wsdlog**</span></span>
7.  <span data-ttu-id="ee126-116">Reproduza a falha iniciando o host e o cliente ou pressionando F5 no Gerenciador de rede.</span><span class="sxs-lookup"><span data-stu-id="ee126-116">Reproduce the failure by starting the host and client or by pressing F5 in the Network Explorer.</span></span>

<span data-ttu-id="ee126-117">**Para desabilitar o rastreamento WSDAPI**</span><span class="sxs-lookup"><span data-stu-id="ee126-117">**To disable WSDAPI tracing**</span></span>

1.  <span data-ttu-id="ee126-118">Abra uma janela de prompt de comando elevado.</span><span class="sxs-lookup"><span data-stu-id="ee126-118">Open an elevated command prompt window.</span></span>
2.  <span data-ttu-id="ee126-119">Execute o seguinte comando: **logman.exe parar wsdlog**</span><span class="sxs-lookup"><span data-stu-id="ee126-119">Run the following command: **logman.exe stop wsdlog**</span></span>

<span data-ttu-id="ee126-120">Depois que a falha do aplicativo for capturada, os \* arquivos. etl poderão ser enviados ao suporte da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ee126-120">Once the application failure has been captured, the \*.etl files can be sent to Microsoft support.</span></span> <span data-ttu-id="ee126-121">Esses arquivos estão localizados em `C:\temp\wsd_*.etl` .</span><span class="sxs-lookup"><span data-stu-id="ee126-121">These files are located in `C:\temp\wsd_*.etl`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee126-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee126-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee126-123">Procedimentos de diagnóstico do WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ee126-123">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="ee126-124">Introdução com a solução de problemas de WSDAPI</span><span class="sxs-lookup"><span data-stu-id="ee126-124">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> <dt>

[https://support.microsoft.com](https://support.microsoft.com)
</dt> </dl>

 

 



