---
title: Nova API permite que os aplicativos enviem dicas de "corte e desmapeamento" para mídia de armazenamento
description: Nova API permite que os aplicativos enviem \ 0034; APARAr e desmapear \ 0034; Dicas para mídia de armazenamento
ms.assetid: DDBC3592-BD4D-4826-83FE-387564DA07E8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e043c1188bda790b4ed151e8a79e1f7b4c6f0f9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "105797542"
---
# <a name="new-api-allows-apps-to-send-trim-and-unmap-hints-to-storage-media"></a><span data-ttu-id="10b5e-103">Nova API permite que os aplicativos enviem dicas de "corte e desmapeamento" para mídia de armazenamento</span><span class="sxs-lookup"><span data-stu-id="10b5e-103">New API allows apps to send "TRIM and Unmap" hints to storage media</span></span>

## <a name="platforms"></a><span data-ttu-id="10b5e-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="10b5e-104">Platforms</span></span>

<span data-ttu-id="10b5e-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="10b5e-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="10b5e-106">**Servidores** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="10b5e-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="10b5e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="10b5e-107">Description</span></span>

<span data-ttu-id="10b5e-108">As dicas de corte notificam a unidade de que determinados setores que foram alocados anteriormente não são mais necessários para o aplicativo e podem ser limpos.</span><span class="sxs-lookup"><span data-stu-id="10b5e-108">TRIM hints notify the drive that certain sectors that previously were allocated are no longer needed by the app and can be purged.</span></span> <span data-ttu-id="10b5e-109">Normalmente, isso é usado quando um aplicativo faz alocações de espaço grandes por meio de um arquivo e, em seguida, gerencia automaticamente as alocações para o arquivo (por exemplo, arquivos de disco rígido virtual).</span><span class="sxs-lookup"><span data-stu-id="10b5e-109">This is typically used when an app makes large space allocations via a file and then self-manages the allocations to the file (for example, Virtual Hard Disk files).</span></span>

<span data-ttu-id="10b5e-110">**O que é TRIM?**</span><span class="sxs-lookup"><span data-stu-id="10b5e-110">**What is TRIM?**</span></span>

<span data-ttu-id="10b5e-111">Os SSDs (unidades de estado sólido) geralmente são dispositivos flash com base em memória em bloco. Isso significa que, quando os dados são gravados no SSD, eles não podem ser substituídos em lugar algum e devem ser gravados em outro lugar até que o bloco possa ser coletado pelo lixo.</span><span class="sxs-lookup"><span data-stu-id="10b5e-111">Solid state drives (SSDs) are typically flash memory based block-erased devices; this means that when data is written to the SSD, it cannot be over-written in place and must be written elsewhere until the block can be garbage collected.</span></span> <span data-ttu-id="10b5e-112">Como o SSD não tem nenhum mecanismo interno para determinar se determinados blocos foram removidos e outros são necessários.</span><span class="sxs-lookup"><span data-stu-id="10b5e-112">Since the SSD has no internal mechanism for determining that certain blocks are removed and others are needed.</span></span> <span data-ttu-id="10b5e-113">A única vez em que o SSD pode marcar um setor "sujo" é quando ele é sobrescrito.</span><span class="sxs-lookup"><span data-stu-id="10b5e-113">The only time the SSD can mark a sector ‘dirty’ is when it is over-written.</span></span> <span data-ttu-id="10b5e-114">Em outros casos, como quando um arquivo é excluído, o SSD retém esses setores porque a exclusão é executada apenas como uma alteração de MFT (tabela de arquivos mestre) e não como uma operação para todos os setores do arquivo.</span><span class="sxs-lookup"><span data-stu-id="10b5e-114">In other cases, such as when a file is deleted, the SSD retains these sectors because the deletion is performed as a master file table (MFT) change only, and not as an operation to all the sectors of the file.</span></span> <span data-ttu-id="10b5e-115">No Windows 7, apresentamos uma maneira padrão de se comunicar com SSDs sobre setores que não são mais necessários.</span><span class="sxs-lookup"><span data-stu-id="10b5e-115">In Windows 7, we introduced a standard way of communicating with SSDs about sectors that are not needed any more.</span></span> <span data-ttu-id="10b5e-116">Esse comando é definido na [especificação T13](https://www.t13.org/Standards/Default.aspx?DocumentType=3) como o comando Trim; O NTFS envia o comando TRIM para algumas operações internas normais, como "DeleteFile".</span><span class="sxs-lookup"><span data-stu-id="10b5e-116">This command is defined in the [T13 specification](https://www.t13.org/Standards/Default.aspx?DocumentType=3) as the TRIM command; NTFS sends the TRIM command for some normal inline operations such as “deletefile.”</span></span>

<span data-ttu-id="10b5e-117">**Outros usos de TRIM no mundo de armazenamento**</span><span class="sxs-lookup"><span data-stu-id="10b5e-117">**Other uses of TRIM in the storage world**</span></span>

<span data-ttu-id="10b5e-118">Como SSDs, redes de área de armazenamento (SANs) e as novas implementações de espaços de software de recurso do Windows 8 consomem dicas de comando de corte para gerenciar seus espaços em ambientes com provisionamento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="10b5e-118">Like SSDs, storage area networks (SANs) and the new Windows 8 feature Software Spaces implementations consume TRIM command hints to manage their spaces in thinly provisioned environments.</span></span> <span data-ttu-id="10b5e-119">Os espaços de software e SANs alocam regiões de armazenamento em tamanhos maiores que setores ou clusters (em qualquer lugar, de 1 MB a 1GB).</span><span class="sxs-lookup"><span data-stu-id="10b5e-119">SANs and Software Spaces allocate regions of storage in sizes that are greater than sectors or clusters (anywhere from 1MB to 1GB).</span></span> <span data-ttu-id="10b5e-120">Quando eles recebem dicas de corte para seu tamanho de alocação (ou maior que o tamanho de alocação), o SAN/SSD pode desalocar uma região para liberar espaço para outros arquivos.</span><span class="sxs-lookup"><span data-stu-id="10b5e-120">When they receive TRIM hints for its allocation size (or greater than the allocation size), the SAN/SSD can de-allocate a region to free up the space for other files.</span></span> <span data-ttu-id="10b5e-121">Normalmente, eles passam por todas as dicas de corte para a mídia subjacente (SSD ou HDD) para que possam consumir o espaço liberado conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="10b5e-121">They typically pass through all TRIM hints to the underlying media (SSD or HDD) so that they can consume the freed up space as appropriate.</span></span> <span data-ttu-id="10b5e-122">Normalmente, eles não movem dados para regiões desalocadas, nem controlam áreas de corte em regiões desalocadas (quando a região está vazia).</span><span class="sxs-lookup"><span data-stu-id="10b5e-122">They do not typically move data around to de-allocate regions, nor do they keep track of TRIM areas to de-allocated regions (when the region is empty).</span></span>

<span data-ttu-id="10b5e-123">SANs com provisionamento dinâmico usam as dicas de corte que são passadas a elas para ajudar a reduzir o espaço geral do armazenamento físico, reduzindo assim o custo.</span><span class="sxs-lookup"><span data-stu-id="10b5e-123">Thinly provisioned SANs use the TRIM hints that are passed to them to help reduce the overall physical storage footprint, hence reducing cost.</span></span> <span data-ttu-id="10b5e-124">A [especificação de SCSI T10](https://www.t10.org) define o comando ' remapeamento ' (semelhante ao comando Trim); aqui, o comando é aplicável a todos os tipos de armazenamento, incluindo HDDs, SSDs e outros.</span><span class="sxs-lookup"><span data-stu-id="10b5e-124">The [T10 SCSI specification](https://www.t10.org) defines the ‘Unmap’ command (similar to the TRIM command); here the command is applicable to all kinds of storage including HDDs, SSDs, and others.</span></span> <span data-ttu-id="10b5e-125">O comando de desmapeamento ajuda a remover blocos físicos da alocação de SAN.</span><span class="sxs-lookup"><span data-stu-id="10b5e-125">The UnMap command helps to remove physical blocks from the SAN’s allocation.</span></span>

## <a name="how-to-use-the-new-api"></a><span data-ttu-id="10b5e-126">Como usar a nova API</span><span class="sxs-lookup"><span data-stu-id="10b5e-126">How to use the new API</span></span>


```
#define FSCTL_FILE_LEVEL_TRIM CTL_CODE(FILE_DEVICE_FILE_SYSTEM, 130, METHOD_BUFFERED, FILE_WRITE_DATA)

Where 
typedef struct _EXTENT_PAIR {
    ULONGLONG Offset;
    ULONGLONG Length;
} EXTENT_PAIR, *PEXTENT_PAIR;

typedef struct _FILE_LEVEL_TRIM {
    //
    // A count of how many Offset:Length pairs are given
    //
    DWORD PairCount;
    //
    // All the pairs.
    //
    EXTENT_PAIR Pairs[1];
} FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM;
```



<span data-ttu-id="10b5e-127">O arquivo de corte é passado por meio do buffer, se possível ou de forma assíncrona (sem buffer) para o comando de DSM do IOCTL do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10b5e-127">File TRIM is passed via the buffer if possible or asynchronously (non-buffered) to the Device IOCTL DSM command TRIM.</span></span> <span data-ttu-id="10b5e-128">Isso é mapeado para o comando TRIM para dispositivos ATA e comando de desmapeamento para dispositivos SCSI.</span><span class="sxs-lookup"><span data-stu-id="10b5e-128">This is mapped to the TRIM command for ATA devices and UnMap command for SCSI devices.</span></span> <span data-ttu-id="10b5e-129">O código de corte do arquivo envia as regiões uma a uma conforme especificado pelas extensões acima.</span><span class="sxs-lookup"><span data-stu-id="10b5e-129">The file TRIM code sends the regions one-by-one as specified by the extents above.</span></span>

<span data-ttu-id="10b5e-130">O arquivo TRIM não espera por retornos do dispositivo, porque os comandos TRIM e removem são definidos como dicas para a mídia de armazenamento subjacente e os códigos de retorno não são esperados.</span><span class="sxs-lookup"><span data-stu-id="10b5e-130">File TRIM does not wait for returns from the device, because the TRIM and Unmap commands are defined as hints to the underlying storage media and return codes are not expected.</span></span>

<span data-ttu-id="10b5e-131">**Fluxo de trabalho de ponta a ponta:**</span><span class="sxs-lookup"><span data-stu-id="10b5e-131">**End-to-end workflow:**</span></span>

1.  <span data-ttu-id="10b5e-132">Recortar arquivo de chamada</span><span class="sxs-lookup"><span data-stu-id="10b5e-132">Call File Trim</span></span>
    1.  <span data-ttu-id="10b5e-133">O arquivo de corte examina as entradas de erros</span><span class="sxs-lookup"><span data-stu-id="10b5e-133">File TRIM examines inputs for errors</span></span>
    2.  <span data-ttu-id="10b5e-134">O corte de arquivo divide as extensões em regiões de LCN</span><span class="sxs-lookup"><span data-stu-id="10b5e-134">File TRIM breaks up the extents into LCN regions</span></span>
    3.  <span data-ttu-id="10b5e-135">O corte de arquivo é arredondado para cima e para baixo para regiões desalinhadas que são passadas para o corte</span><span class="sxs-lookup"><span data-stu-id="10b5e-135">File TRIM rounds up and down for mis-aligned regions that are passed into TRIM</span></span>
    4.  <span data-ttu-id="10b5e-136">O corte de arquivo limpa as entradas no cache relacionadas às áreas de corte</span><span class="sxs-lookup"><span data-stu-id="10b5e-136">File TRIM purges entries in the cache that relate to the TRIM areas</span></span>
    5.  <span data-ttu-id="10b5e-137">O arquivo de corte passa \_ por IOCTL DSM (trim) por região</span><span class="sxs-lookup"><span data-stu-id="10b5e-137">File TRIM passes IOCTL\_DSM (Trim) per region</span></span>
2.  <span data-ttu-id="10b5e-138">Recorte de arquivo retorna ou erros</span><span class="sxs-lookup"><span data-stu-id="10b5e-138">File TRIM returns or errors</span></span>
    1.  <span data-ttu-id="10b5e-139">A verificação de erros é feita na validade de entrada</span><span class="sxs-lookup"><span data-stu-id="10b5e-139">Error checking is done on input validity</span></span>
    2.  <span data-ttu-id="10b5e-140">Se apenas algumas das extensões forem válidas, um erro será retornado para a chamada de API completa</span><span class="sxs-lookup"><span data-stu-id="10b5e-140">If only some of the extents are valid, one error is returned for the complete API call</span></span>

<span data-ttu-id="10b5e-141">**Casos de uso**</span><span class="sxs-lookup"><span data-stu-id="10b5e-141">**Use cases**</span></span>

<span data-ttu-id="10b5e-142">**VHD (disco rígido virtual) do consumidor montado em um SSD:**</span><span class="sxs-lookup"><span data-stu-id="10b5e-142">**Consumer virtual hard disk (VHD) mounted on an SSD:**</span></span>

<span data-ttu-id="10b5e-143">Inicialmente, o VHD é montado em mídia não utilizada "limpa".</span><span class="sxs-lookup"><span data-stu-id="10b5e-143">The VHD is initially mounted on ‘clean’ unused media.</span></span> <span data-ttu-id="10b5e-144">Como o VHD é usado, o VHD consome partes da mídia de armazenamento para arquivos, etc. Quando ele exclui arquivos na mídia de armazenamento, esses arquivos não são removidos do SSD, pois o VHD completo é armazenado como um arquivo no SSD.</span><span class="sxs-lookup"><span data-stu-id="10b5e-144">As the VHD is used, the VHD consumes parts of the storage media for files, etc. When it deletes files in the storage media, these files are not removed from the SSD since the complete VHD is stored as one file on the SSD.</span></span> <span data-ttu-id="10b5e-145">O ambiente Hyper-V chama o corte de arquivo para todas as regiões que são excluídas quando Delete-File ocorre no ambiente VHD.</span><span class="sxs-lookup"><span data-stu-id="10b5e-145">The Hyper-V environment calls File TRIM for all regions that are deleted when delete-file occurs in the VHD environment.</span></span> <span data-ttu-id="10b5e-146">As \_ aparas de arquivo são convertidas no SSD para que o desempenho do SSD possa ser otimizado.</span><span class="sxs-lookup"><span data-stu-id="10b5e-146">The File\_TRIMs are translated to the SSD so that the SSD performance can be optimized.</span></span>

<span data-ttu-id="10b5e-147">**VHD de consumidor montado em uma SAN com provisionamento dinâmico:**</span><span class="sxs-lookup"><span data-stu-id="10b5e-147">**Consumer VHD mounted on a thinly provisioned SAN:**</span></span>

<span data-ttu-id="10b5e-148">Inicialmente, o VHD é montado em uma laje mínima de um ambiente com provisionamento dinâmico.</span><span class="sxs-lookup"><span data-stu-id="10b5e-148">The VHD is initially mounted on one minimum slab of a thinly provisioned environment.</span></span> <span data-ttu-id="10b5e-149">À medida que os arquivos são armazenados no VHD, a superfície de armazenamento do VHD cresce em múltiplos de Slabs.</span><span class="sxs-lookup"><span data-stu-id="10b5e-149">As files are stored in the VHD, the storage footprint of the VHD grows in multiples of slabs.</span></span> <span data-ttu-id="10b5e-150">Quando os arquivos são removidos no VHD, o Hyper-V chama o arquivo de \_ corte para a San provisionada subjacente.</span><span class="sxs-lookup"><span data-stu-id="10b5e-150">When files are removed in the VHD, the Hyper-V calls File\_TRIM to the underlying thinly provisioned SAN.</span></span> <span data-ttu-id="10b5e-151">Se os cortes forem maiores que a granularidade da laje, a SAN agora poderá remover uma laje e, portanto, reduzir a superfície do VHD nessa SAN.</span><span class="sxs-lookup"><span data-stu-id="10b5e-151">If the TRIMs are bigger than the SLAB granularity, the SAN can now remove a SLAB and hence reduce the footprint of the VHD on that SAN.</span></span>

<span data-ttu-id="10b5e-152">Se o VHD for residente em um servidor baseado no Windows 8, o otimizador de armazenamento também enviará cortes para reduzir a superfície do Slab do VHD de dentro do VHD montado.</span><span class="sxs-lookup"><span data-stu-id="10b5e-152">If the VHD is resident on a Windows 8 based server, the Storage Optimizer will also send TRIMs to reduce the slab footprint of the VHD from within the mounted VHD.</span></span>

## <a name="tests"></a><span data-ttu-id="10b5e-153">Testes</span><span class="sxs-lookup"><span data-stu-id="10b5e-153">Tests</span></span>

<span data-ttu-id="10b5e-154">Não há APIs comparáveis em versões anteriores do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="10b5e-154">There are no comparable APIs in earlier operating system releases.</span></span> <span data-ttu-id="10b5e-155">Não deve haver impacto no desempenho da própria API propriamente dita, embora a mídia de armazenamento (se implementada corretamente) possa mostrar um melhor desempenho de gravação.</span><span class="sxs-lookup"><span data-stu-id="10b5e-155">There should be no performance impact from the actual API itself, though the storage media (if implemented correctly) can show better write performance.</span></span> <span data-ttu-id="10b5e-156">A API deve ser usada com muito cuidado; somente as extensões que não forem mais necessárias devem ser passadas, pois essas extensões serão removidas permanentemente da mídia de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="10b5e-156">The API should be used very carefully; only extents that are no longer needed should be passed down as those extents will be permanently removed from the storage media.</span></span>

## <a name="resources"></a><span data-ttu-id="10b5e-157">Recursos</span><span class="sxs-lookup"><span data-stu-id="10b5e-157">Resources</span></span>

-   [<span data-ttu-id="10b5e-158">Especificação de T13</span><span class="sxs-lookup"><span data-stu-id="10b5e-158">T13 specification</span></span>](http://www.t13.org/Standards/Default.aspx?DocumentType=3)
-   [<span data-ttu-id="10b5e-159">Especificação de SCSI T10</span><span class="sxs-lookup"><span data-stu-id="10b5e-159">T10 SCSI specification</span></span>](https://www.t10.org/)

 

 




