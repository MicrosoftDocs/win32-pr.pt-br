---
title: Códigos de controle de e/s de dispositivo
description: Códigos de controle de e/s de dispositivo
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player, códigos de controle de e/s de dispositivo
- Windows Media Player, códigos de controle
- Gerenciador de Dispositivos de mídia do Windows
- códigos de controle de e/s de dispositivo
- códigos de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105770508"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="c851c-108">Códigos de controle de e/s de dispositivo</span><span class="sxs-lookup"><span data-stu-id="c851c-108">Device I/O Control Codes</span></span>

<span data-ttu-id="c851c-109">O Windows Media Player 10 ou posterior define códigos de controle de e/s de dispositivo do Windows Media Gerenciador de Dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c851c-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="c851c-110">A tabela a seguir contém os códigos de controle e suas descrições.</span><span class="sxs-lookup"><span data-stu-id="c851c-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="c851c-111">Código de controle de e/s</span><span class="sxs-lookup"><span data-stu-id="c851c-111">I/O control code</span></span>                      | <span data-ttu-id="c851c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c851c-112">Value</span></span>      | <span data-ttu-id="c851c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c851c-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c851c-114">**viagem de ida e volta de metadados do WMP do IOCTL \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c851c-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="c851c-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="c851c-115">0x31504d57</span></span> | <span data-ttu-id="c851c-116">Gerencia a transferência de informações sobre as alterações ocorridas nos valores de metadados.</span><span class="sxs-lookup"><span data-stu-id="c851c-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="c851c-117">Consulte [extensões de dispositivo para transferência de metadados acelerada](device-extensions-for-accelerated-metadata-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="c851c-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="c851c-118">**o \_ dispositivo WMP do IOCTL \_ \_ pode ser \_ sincronizado**</span><span class="sxs-lookup"><span data-stu-id="c851c-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="c851c-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="c851c-119">0x32504d57</span></span> | <span data-ttu-id="c851c-120">Indica se um dispositivo portátil dá suporte à sincronização automática.</span><span class="sxs-lookup"><span data-stu-id="c851c-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="c851c-121">O Windows Media Player 10 ou posterior não fornece nenhum buffer de entrada. O buffer de saída deve retornar um valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c851c-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="c851c-122">Um valor de 1 significa que o dispositivo dá suporte à sincronização.</span><span class="sxs-lookup"><span data-stu-id="c851c-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="c851c-123">Um valor de 0 significa que o dispositivo não oferece suporte à sincronização automática.</span><span class="sxs-lookup"><span data-stu-id="c851c-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="c851c-124">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c851c-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c851c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c851c-125">Remarks</span></span>

<span data-ttu-id="c851c-126">Esses códigos de controle são definidos em wmpdevices. h.</span><span class="sxs-lookup"><span data-stu-id="c851c-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="c851c-127">Se o dispositivo não der suporte ao **IOCTL WMP, o \_ \_ dispositivo \_ pode ser \_ sincronizado**, o Windows Media Player 10 ou posterior pressupõe que o dispositivo oferece suporte à sincronização automática.</span><span class="sxs-lookup"><span data-stu-id="c851c-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="c851c-128">Observe que embora esse valor possa não permitir a sincronização automática, há critérios adicionais usados para determinar se o dispositivo dá suporte à sincronização automática.</span><span class="sxs-lookup"><span data-stu-id="c851c-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c851c-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c851c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c851c-130">**Extensões de dispositivo para transferência de metadados acelerada**</span><span class="sxs-lookup"><span data-stu-id="c851c-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="c851c-131">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="c851c-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 





