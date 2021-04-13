---
description: Emitindo comandos AV/C brutos
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emitindo comandos AV/C brutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370147"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="8f112-103">Emitindo comandos AV/C brutos</span><span class="sxs-lookup"><span data-stu-id="8f112-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="8f112-104">As interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funcionam convertendo as chamadas de método em comandos para o driver e, em seguida, interpretando a resposta do driver e retornando-a por meio de um parâmetro **HRESULT** ou output.</span><span class="sxs-lookup"><span data-stu-id="8f112-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="8f112-105">No entanto, algumas funções de dispositivo podem não estar acessíveis por meio desses métodos.</span><span class="sxs-lookup"><span data-stu-id="8f112-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="8f112-106">Portanto, o MSDV dá suporte ao envio de comandos AV/C brutos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f112-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="8f112-107">Você deve ter os seguintes pontos em mente ao usar esse recurso:</span><span class="sxs-lookup"><span data-stu-id="8f112-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="8f112-108">O comando é passado diretamente para o dispositivo, sem verificação de erro ou validação de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8f112-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="8f112-109">Por esse motivo, você deve emitir comandos AV/C brutos somente quando as interfaces do DirectShow não implementam a funcionalidade de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="8f112-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="8f112-110">Todos os comandos AV/C brutos são síncronos.</span><span class="sxs-lookup"><span data-stu-id="8f112-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="8f112-111">O thread que emite os blocos de comando até que o comando retorne.</span><span class="sxs-lookup"><span data-stu-id="8f112-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="8f112-112">Apenas um comando pode ser fornecido por vez.</span><span class="sxs-lookup"><span data-stu-id="8f112-112">Only one command can be given at a time.</span></span> <span data-ttu-id="8f112-113">Enquanto o comando estiver sendo processado, o dispositivo rejeitará todos os comandos adicionais.</span><span class="sxs-lookup"><span data-stu-id="8f112-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="8f112-114">O driver UVC não dá suporte a comandos brutos AV/C.</span><span class="sxs-lookup"><span data-stu-id="8f112-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="8f112-115">Para enviar um comando AV/C, formate o comando como uma matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="8f112-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="8f112-116">Em seguida, chame [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span><span class="sxs-lookup"><span data-stu-id="8f112-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="8f112-117">Passe o sinalizador de \_ cmd de dev ext brutos Ed \_ \_ \_ , o tamanho da matriz e a matriz.</span><span class="sxs-lookup"><span data-stu-id="8f112-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="8f112-118">Você deve converter o endereço da matriz em um tipo \**LPOLESTR \** _, pois a finalidade original desse parâmetro era retornar um valor de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8f112-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="8f112-119">O conteúdo da matriz é passado diretamente para o dispositivo, portanto, você deve ter cuidado para formatá-lo corretamente.</span><span class="sxs-lookup"><span data-stu-id="8f112-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="8f112-120">Um comando pode direcionar a unidade (camcorder) ou uma subunidade (fita ou câmera).</span><span class="sxs-lookup"><span data-stu-id="8f112-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="8f112-121">Os padrões relevantes estão disponíveis no [site da associação comercial 1394](https://1394ta.org).</span><span class="sxs-lookup"><span data-stu-id="8f112-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="8f112-122">Especificação geral do comando de interface digital AV/C</span><span class="sxs-lookup"><span data-stu-id="8f112-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="8f112-123">Especificação de subunidade do gravador de fita AV/C/Player</span><span class="sxs-lookup"><span data-stu-id="8f112-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="8f112-124">A primeira descreve como formatar comandos AV/C e lista os comandos de unidade.</span><span class="sxs-lookup"><span data-stu-id="8f112-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="8f112-125">A segunda especificação lista os comandos de subunidade.</span><span class="sxs-lookup"><span data-stu-id="8f112-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="8f112-126">O método **GetTransportBasicParameters** pode retornar um dos seguintes códigos de erro:</span><span class="sxs-lookup"><span data-stu-id="8f112-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="8f112-127">Código do Erro</span><span class="sxs-lookup"><span data-stu-id="8f112-127">Error Code</span></span>              | <span data-ttu-id="8f112-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f112-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8f112-129">\_tempo limite do erro</span><span class="sxs-lookup"><span data-stu-id="8f112-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="8f112-130">O tempo limite do comando foi atingido.</span><span class="sxs-lookup"><span data-stu-id="8f112-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="8f112-131">Req. de erro \_ \_ não \_ ACCEP</span><span class="sxs-lookup"><span data-stu-id="8f112-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="8f112-132">O dispositivo não aceitou o comando.</span><span class="sxs-lookup"><span data-stu-id="8f112-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="8f112-133">ERRO \_ sem \_ suporte</span><span class="sxs-lookup"><span data-stu-id="8f112-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="8f112-134">O dispositivo não oferece suporte ao comando.</span><span class="sxs-lookup"><span data-stu-id="8f112-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="8f112-135">solicitação de erro \_ \_ anulada</span><span class="sxs-lookup"><span data-stu-id="8f112-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="8f112-136">O comando foi anulado.</span><span class="sxs-lookup"><span data-stu-id="8f112-136">The command was aborted.</span></span> <span data-ttu-id="8f112-137">Possbly o dispositivo foi removido ou uma redefinição de barramento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="8f112-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8f112-138">Esses erros são retornados como códigos de erro do Win32, não HRESULTs, portanto, você deve testar esses valores diretamente, em vez de usar as macros com **êxito** e **com falha** .</span><span class="sxs-lookup"><span data-stu-id="8f112-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="8f112-139">Se o método retornar S \_ OK, a resposta do dispositivo será copiada para a matriz.</span><span class="sxs-lookup"><span data-stu-id="8f112-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="8f112-140">A carga de resposta pode ser maior que o comando, portanto, você deve alocar um buffer grande o suficiente para contê-lo.</span><span class="sxs-lookup"><span data-stu-id="8f112-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="8f112-141">O tamanho máximo da carga é de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="8f112-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="8f112-142">Observe que um valor de retorno de S \_ OK nem sempre significa que o dispositivo realizou o comando com êxito.</span><span class="sxs-lookup"><span data-stu-id="8f112-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="8f112-143">O aplicativo deve examinar a carga de resposta para determinar o status.</span><span class="sxs-lookup"><span data-stu-id="8f112-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="8f112-144">O exemplo a seguir mostra o comando para procurar uma pesquisa de número de faixa absoluta:</span><span class="sxs-lookup"><span data-stu-id="8f112-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="8f112-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f112-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f112-146">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="8f112-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



