---
description: Comandos
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandos (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164419"
---
# <a name="commands-wpd-api"></a><span data-ttu-id="aa0a5-103">Comandos (API WPD)</span><span class="sxs-lookup"><span data-stu-id="aa0a5-103">Commands (WPD API)</span></span>

<span data-ttu-id="aa0a5-104">O aplicativo cliente e o driver se comunicam por meio de comandos que são enviados do cliente (por meio da API de dispositivo portátil do Windows) para o driver (por meio da estrutura de driver do User-Mode).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-104">The client application and the driver communicate by means of commands that are sent from the client (via the Windows Portable Device API) to the driver (via the User-Mode Driver Framework).</span></span> <span data-ttu-id="aa0a5-105">Um comando pode ou não incluir um parâmetro e pode ou não retornar um resultado.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-105">A command may or may not include a parameter, and may or may not return a result.</span></span> <span data-ttu-id="aa0a5-106">Um cliente pode enviar um comando explicitamente, chamando o método [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) ou o método **IPortableDeviceService: SendCommand** , ou implicitamente, chamando qualquer um dos métodos das interfaces de cliente.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-106">A client can send a command explicitly, by calling either the [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) method or the **IPortableDeviceService:SendCommand** method, or implicitly, by calling any of the methods of the client interfaces.</span></span> <span data-ttu-id="aa0a5-107">Alguns comandos só podem ser enviados explicitamente; Eles são indicados na documentação do comando.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-107">A few commands can only be sent explicitly; these are noted in the command's documentation.</span></span> <span data-ttu-id="aa0a5-108">As páginas de referência de comando descrevem a finalidade de um comando, bem como os parâmetros que espera receber e quais parâmetros devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-108">The command reference pages describe the purpose of a command, as well as what parameters it expects to receive, and what parameters it is expected to return.</span></span>

<span data-ttu-id="aa0a5-109">Um comando é identificado por uma estrutura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="aa0a5-109">A command is identified by a **PROPERTYKEY** structure.</span></span> <span data-ttu-id="aa0a5-110">Isso é composto de duas partes: uma parte de GUID (o membro *fmtid* ) e uma parte DWORD (o membro *pid* ).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-110">This is made up of two parts: a GUID part (the *fmtid* member) and a DWORD part (the *pid* member).</span></span> <span data-ttu-id="aa0a5-111">A parte GUID é usada para indicar a categoria à qual o comando pertence (comandos relacionados pertencem à mesma categoria e, portanto, terão o mesmo *fmtid*).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-111">The GUID part is used to indicate the category the command belongs to (related commands belong to the same category, and therefore will have the same *fmtid*).</span></span> <span data-ttu-id="aa0a5-112">A parte DWORD indica a ID de comando e é usada para distinguir os comandos individuais dentro de uma categoria de comando (os valores de *pid* para comandos na mesma categoria serão diferentes).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-112">The DWORD part indicates the command ID, and is used to distinguish the individual commands within a command category (the *pid* values for commands in the same category will be different).</span></span>

<span data-ttu-id="aa0a5-113">A tabela a seguir lista as categorias de comandos que os dispositivos portáteis do Windows definem.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-113">The following table lists the categories of commands that Windows Portable Devices defines.</span></span> <span data-ttu-id="aa0a5-114">Os fabricantes de dispositivos podem definir seus próprios comandos criando suas próprias categorias de comando e IDs de comando.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-114">Device manufacturers can define their own commands by creating their own command categories and command IDs.</span></span> <span data-ttu-id="aa0a5-115">No entanto, um fabricante não deve adicionar comandos às categorias listadas abaixo, pois elas são reservadas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-115">However, a manufacturer should not add commands to the categories listed below, since these are reserved by Microsoft.</span></span>

<span data-ttu-id="aa0a5-116">**Categorias de comando**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-116">**Command Categories**</span></span>



| <span data-ttu-id="aa0a5-117">Categoria de comando</span><span class="sxs-lookup"><span data-stu-id="aa0a5-117">Command category</span></span>                         | <span data-ttu-id="aa0a5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0a5-118">Description</span></span>                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0a5-119">**Categoria de WPD \_ \_ comum**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-119">**WPD\_CATEGORY\_COMMON**</span></span>                | <span data-ttu-id="aa0a5-120">Comandos que são comuns a todos os objetos e dispositivos.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-120">Commands that are common to all objects and devices.</span></span>                                                                                    |
| <span data-ttu-id="aa0a5-121">**\_dicas de \_ dispositivo de categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-121">**WPD\_CATEGORY\_DEVICE\_HINTS**</span></span>         | <span data-ttu-id="aa0a5-122">Comandos que são usados para recuperar informações opcionais do dispositivo que podem ser usadas para melhorar a experiência do usuário final.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-122">Commands that are used to retrieve optional device information that can be used to improve end-user experience.</span></span>                         |
| <span data-ttu-id="aa0a5-123">**Categoria de WPD do \_ \_ SMS**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-123">**WPD\_CATEGORY\_SMS**</span></span>                   | <span data-ttu-id="aa0a5-124">Comandos que são usados para dispositivos que oferecem suporte à funcionalidade SMS, que normalmente é exposta em telefones celulares.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-124">Commands that are used for devices that support short message service (SMS) functionality, which is typically exposed on mobile phones.</span></span> |
| <span data-ttu-id="aa0a5-125">**a \_ categoria \_ WPD \_ ainda \_ captura de imagem**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-125">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE**</span></span> | <span data-ttu-id="aa0a5-126">Comandos que são usados para dispositivos que dão suporte à captura de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-126">Commands that are used for devices that support still image capture.</span></span>                                                                    |
| <span data-ttu-id="aa0a5-127">**\_armazenamento de categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-127">**WPD\_CATEGORY\_STORAGE**</span></span>               | <span data-ttu-id="aa0a5-128">Comandos que são usados para objetos funcionais de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-128">Commands that are used for storage functional objects.</span></span>                                                                                  |



 

<span data-ttu-id="aa0a5-129">Os comandos específicos definidos para cada um desses tipos são fornecidos nas tabelas a seguir, organizadas por tipo de comando.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-129">The specific commands that are defined for each of these types are given in the following tables, organized by command type.</span></span>

<span data-ttu-id="aa0a5-130">**Categoria \_ comum da categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-130">**WPD\_CATEGORY\_COMMON Category**</span></span>



| <span data-ttu-id="aa0a5-131">Comando</span><span class="sxs-lookup"><span data-stu-id="aa0a5-131">Command</span></span>                                                                                | <span data-ttu-id="aa0a5-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0a5-132">Description</span></span>        |
|----------------------------------------------------------------------------------------|--------------------|
| [<span data-ttu-id="aa0a5-133">**\_comando de \_ \_ redefinição comum de comandos WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-133">**WPD\_COMMAND\_COMMON\_RESET\_DEVICE**</span></span>](wpd-command-common-reset-device-command.md) | <span data-ttu-id="aa0a5-134">Redefine o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-134">Resets the device.</span></span> |



 

<span data-ttu-id="aa0a5-135">**Categoria \_ de \_ dicas de dispositivo de categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-135">**WPD\_CATEGORY\_DEVICE\_HINTS Category**</span></span>



| <span data-ttu-id="aa0a5-136">Comando</span><span class="sxs-lookup"><span data-stu-id="aa0a5-136">Command</span></span>                                                                                                              | <span data-ttu-id="aa0a5-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0a5-137">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="aa0a5-138">**\_dicas de dispositivo de comando WPD \_ \_ \_ obter \_ local do conteúdo \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-138">**WPD\_COMMAND\_DEVICE\_HINTS\_GET\_CONTENT\_LOCATION**</span></span>](wpd-command-device-hints-get-content-location-command.md) | <span data-ttu-id="aa0a5-139">Recupera as IDs de objeto das pastas que podem conter um objeto de um tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-139">Retrieves the object IDs of folders that can hold an object of a specified type.</span></span> |



 

<span data-ttu-id="aa0a5-140">**Categoria de armazenamento de \_ categoria WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-140">**WPD\_CATEGORY\_STORAGE Category**</span></span>



| <span data-ttu-id="aa0a5-141">Comando</span><span class="sxs-lookup"><span data-stu-id="aa0a5-141">Command</span></span>                                                                     | <span data-ttu-id="aa0a5-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0a5-142">Description</span></span>                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="aa0a5-143">**\_ejeção de \_ armazenamento de comando WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-143">**WPD\_COMMAND\_STORAGE\_EJECT**</span></span>](wpd-command-storage-eject-command.md)   | <span data-ttu-id="aa0a5-144">Ejeta um meio de armazenamento que pode ser ejetado remotamente pelo driver.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-144">Ejects a storage medium that can be ejected remotely by the driver.</span></span> |
| [<span data-ttu-id="aa0a5-145">**\_formato de \_ armazenamento de comando WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-145">**WPD\_COMMAND\_STORAGE\_FORMAT**</span></span>](wpd-command-storage-format-command.md) | <span data-ttu-id="aa0a5-146">Formata um objeto funcional de armazenamento no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-146">Formats a storage functional object on the device.</span></span>                  |



 

<span data-ttu-id="aa0a5-147">**Categoria da \_ categoria de SMS de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-147">**WPD\_CATEGORY\_SMS Category**</span></span>



| <span data-ttu-id="aa0a5-148">Comando</span><span class="sxs-lookup"><span data-stu-id="aa0a5-148">Command</span></span>                                                         | <span data-ttu-id="aa0a5-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0a5-149">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="aa0a5-150">**\_comando de \_ envio de SMS para o WPD \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-150">**WPD\_COMMAND\_SMS\_SEND**</span></span>](wpd-command-sms-send-command.md) | <span data-ttu-id="aa0a5-151">Inicia o envio de uma mensagem SMS por um objeto funcional do SMS.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-151">Initiates the sending of an SMS message by an SMS functional object.</span></span> |



 

<span data-ttu-id="aa0a5-152">**Categoria de WPD de \_ \_ \_ imagem ainda categoria \_**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-152">**WPD\_CATEGORY\_STILL\_IMAGE\_CAPTURE Category**</span></span>



| <span data-ttu-id="aa0a5-153">Comando</span><span class="sxs-lookup"><span data-stu-id="aa0a5-153">Command</span></span>                                                                                                   | <span data-ttu-id="aa0a5-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0a5-154">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="aa0a5-155">**comando WPD- \_ \_ captura de \_ imagem ainda \_ \_ iniciada**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-155">**WPD\_COMMAND\_STILL\_IMAGE\_CAPTURE\_INITIATE**</span></span>](wpd-command-still-image-capture-initiate-command.md) | <span data-ttu-id="aa0a5-156">Inicia uma captura de imagem ainda por um objeto funcional de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-156">Initiates a still image capture by a still image functional object.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="aa0a5-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa0a5-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa0a5-158">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="aa0a5-158">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



