---
description: Descreve como usar a ferramenta de pesquisa de erros da Microsoft para localizar explicações de texto de códigos de erro hexadecimais no Windows.
title: A ferramenta de pesquisa de erros da Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812135"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="5d6a9-103">A ferramenta de pesquisa de erros da Microsoft</span><span class="sxs-lookup"><span data-stu-id="5d6a9-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="5d6a9-104">A ferramenta pesquisa de erros da Microsoft exibe o texto da mensagem que está associado a um código de status hexadecimal (ou outro código).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="5d6a9-105">Esse texto é definido em vários arquivos de cabeçalho de código-fonte da Microsoft, como Winerror. h, Setupapi. h e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="5d6a9-106">A ferramenta é assinada digitalmente pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="5d6a9-107">A seguir estão as informações de SHA256 para o download do arquivo:</span><span class="sxs-lookup"><span data-stu-id="5d6a9-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="5d6a9-108">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="5d6a9-108">Algorithm</span></span> |<span data-ttu-id="5d6a9-109">Hash</span><span class="sxs-lookup"><span data-stu-id="5d6a9-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="5d6a9-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="5d6a9-110">SHA256</span></span> |<span data-ttu-id="5d6a9-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span><span class="sxs-lookup"><span data-stu-id="5d6a9-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="5d6a9-112">Os ambientes de negócios podem restringir quais arquivos podem ser executados e de onde.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="5d6a9-113">Antes de baixar e executar essa ferramenta, verifique os seguintes detalhes:</span><span class="sxs-lookup"><span data-stu-id="5d6a9-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="5d6a9-114">Você precisa ter permissão ou uma exceção de segurança para poder baixar ou executar a ferramenta?</span><span class="sxs-lookup"><span data-stu-id="5d6a9-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="5d6a9-115">Você pode armazenar e executar essa ferramenta em seu computador (por exemplo, na pasta documentos)?</span><span class="sxs-lookup"><span data-stu-id="5d6a9-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="5d6a9-116">Ou você precisa armazenar e executar a ferramenta em um computador especializado, como um servidor de arquivos central?</span><span class="sxs-lookup"><span data-stu-id="5d6a9-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="5d6a9-117">Uso</span><span class="sxs-lookup"><span data-stu-id="5d6a9-117">Usage</span></span>

1. <span data-ttu-id="5d6a9-118">Baixe a ferramenta selecionando [este link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="5d6a9-119">Se você não especificou um local na etapa 1, vá para a pasta de download e copie ou mova o arquivo baixado (Err_6.4.5.exe) para a pasta na qual você armazenará a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="5d6a9-120">Você não precisa expandir ou instalar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="5d6a9-121">Se você copiar ou mover o arquivo para uma pasta que está listada na variável de ambiente **path** do seu sistema operacional, ela funcionará em qualquer prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="5d6a9-122">Abra uma janela de Prompt de Comando.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-122">Open a Command Prompt window.</span></span> <span data-ttu-id="5d6a9-123">Se necessário, altere o diretório para o local da ferramenta de pesquisa de erros.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="5d6a9-124">Execute o comando a seguir:</span><span class="sxs-lookup"><span data-stu-id="5d6a9-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="5d6a9-125">Neste comando, \<*error code*> representa o código hexadecimal que você deseja pesquisar.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="5d6a9-126">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5d6a9-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="5d6a9-127">Mais informações</span><span class="sxs-lookup"><span data-stu-id="5d6a9-127">More information</span></span>

<span data-ttu-id="5d6a9-128">Tenha em mente que essa é uma ferramenta "pontual".</span><span class="sxs-lookup"><span data-stu-id="5d6a9-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="5d6a9-129">A ferramenta de pesquisa de erros da Microsoft decodifica a maioria dos códigos de erro da Microsoft a partir da data em que a ferramenta foi compilada.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="5d6a9-130">À medida que novas versões do Windows adicionam novos eventos e códigos de erro, talvez seja necessário baixar uma nova versão da ferramenta de pesquisa de erros.</span><span class="sxs-lookup"><span data-stu-id="5d6a9-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="5d6a9-131">Verifique o centro de download da Microsoft para obter uma nova versão ou veja os [códigos de erro](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5d6a9-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
