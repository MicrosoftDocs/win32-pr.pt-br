---
title: Atalhos de comando e variações
description: Atalhos de comando e variações
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636578"
---
# <a name="command-shortcuts-and-variations"></a><span data-ttu-id="399cf-103">Atalhos de comando e variações</span><span class="sxs-lookup"><span data-stu-id="399cf-103">Command Shortcuts and Variations</span></span>

<span data-ttu-id="399cf-104">Você pode usar vários atalhos ao trabalhar com comandos MCI.</span><span class="sxs-lookup"><span data-stu-id="399cf-104">You can use several shortcuts when working with MCI commands.</span></span> <span data-ttu-id="399cf-105">Esses atalhos permitem que você use um único identificador para se referir a todos os dispositivos que seu aplicativo abriu ou para abrir um dispositivo sem emitir explicitamente um comando [**aberto**](open.md) ([**MCI \_ Open**](mci-open.md)).</span><span class="sxs-lookup"><span data-stu-id="399cf-105">These shortcuts enable you to use a single identifier to refer to all the devices your application has opened, or to open a device without explicitly issuing an [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) command.</span></span>

<span data-ttu-id="399cf-106">Você pode especificar "todos" (MCI \_ todos \_ os \_ ID do dispositivo) como um identificador de dispositivo para qualquer comando que não retorna informações.</span><span class="sxs-lookup"><span data-stu-id="399cf-106">You can specify "all" (MCI\_ALL\_DEVICE\_ID) as a device identifier for any command that does not return information.</span></span> <span data-ttu-id="399cf-107">Quando você especifica "All", o MCI envia o comando sequencialmente para todos os dispositivos abertos pelo aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="399cf-107">When you specify "all", MCI sends the command sequentially to all devices opened by the current application.</span></span>

<span data-ttu-id="399cf-108">Por exemplo, o comando [**fechar**](close.md) "todos" fecha todos os dispositivos abertos e o comando [**reproduzir**](play.md) "todos" começa a reproduzir todos os dispositivos abertos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="399cf-108">For example, the [**close**](close.md) "all" command closes all open devices and the [**play**](play.md) "all" command starts playing all devices opened by the application.</span></span> <span data-ttu-id="399cf-109">Como o MCI envia seqüencialmente os comandos para os dispositivos MCI, há um intervalo entre quando o primeiro e último dispositivos recebem o comando.</span><span class="sxs-lookup"><span data-stu-id="399cf-109">Because MCI sequentially sends the commands to the MCI devices, there is an interval between when the first and last devices receive the command.</span></span>

<span data-ttu-id="399cf-110">Usar "All" é uma maneira conveniente de transmitir um comando para todos os seus dispositivos, mas você não deve confiar nele para sincronizar dispositivos; o intervalo entre as mensagens pode variar.</span><span class="sxs-lookup"><span data-stu-id="399cf-110">Using "all" is a convenient way to broadcast a command to all your devices, but you should not rely on it to synchronize devices; the timing between messages can vary.</span></span>

<span data-ttu-id="399cf-111">Quando você emite um comando e especifica um dispositivo que não está aberto, o MCI tenta abrir o dispositivo antes de implementar o comando.</span><span class="sxs-lookup"><span data-stu-id="399cf-111">When you issue a command and specify a device that is not open, MCI tries to open the device before implementing the command.</span></span> <span data-ttu-id="399cf-112">As regras a seguir se aplicam para abrir dispositivos automaticamente:</span><span class="sxs-lookup"><span data-stu-id="399cf-112">The following rules apply to automatically opening devices:</span></span>

-   <span data-ttu-id="399cf-113">O recurso abrir automático funciona apenas com a interface de cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="399cf-113">The automatic open feature works only with the command-string interface.</span></span>
-   <span data-ttu-id="399cf-114">O recurso aberto automático falha para comandos específicos de drivers de dispositivo personalizados.</span><span class="sxs-lookup"><span data-stu-id="399cf-114">The automatic open feature fails for commands that are specific to custom device drivers.</span></span>
-   <span data-ttu-id="399cf-115">Os dispositivos abertos automaticamente não respondem a comandos que usam "todos" como um nome de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="399cf-115">Automatically opened devices do not respond to commands that use "all" as a device name.</span></span>
-   <span data-ttu-id="399cf-116">O recurso aberto automático não permite que seu aplicativo especifique o sinalizador "tipo".</span><span class="sxs-lookup"><span data-stu-id="399cf-116">The automatic open feature does not let your application specify the "type" flag.</span></span> <span data-ttu-id="399cf-117">Sem o nome do dispositivo, o MCI determina o nome do dispositivo nas entradas no registro.</span><span class="sxs-lookup"><span data-stu-id="399cf-117">Without the device name, MCI determines the device name from the entries in the registry.</span></span> <span data-ttu-id="399cf-118">Para usar um dispositivo específico, você pode combinar o nome do dispositivo com o nome do arquivo usando o ponto de exclamação, conforme descrito no material de referência do comando [**abrir**](open.md) .</span><span class="sxs-lookup"><span data-stu-id="399cf-118">To use a specific device, you can combine the device name with the filename by using the exclamation point, as described in the reference material for the [**open**](open.md) command.</span></span>

<span data-ttu-id="399cf-119">Se um aplicativo usar o recurso abrir automaticamente para abrir um dispositivo, o aplicativo deverá verificar o valor de retorno de cada comando Open subsequente para verificar se o dispositivo ainda está aberto.</span><span class="sxs-lookup"><span data-stu-id="399cf-119">If an application uses the automatic open feature to open a device, the application should check the return value of every subsequent open command to verify that the device is still open.</span></span> <span data-ttu-id="399cf-120">O MCI também fecha automaticamente qualquer dispositivo que abrir automaticamente.</span><span class="sxs-lookup"><span data-stu-id="399cf-120">MCI also automatically closes any device that it automatically opens.</span></span> <span data-ttu-id="399cf-121">O MCI normalmente fecha um dispositivo nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="399cf-121">MCI typically closes a device in the following situations:</span></span>

-   <span data-ttu-id="399cf-122">O comando está concluído.</span><span class="sxs-lookup"><span data-stu-id="399cf-122">The command is completed.</span></span>
-   <span data-ttu-id="399cf-123">Você anula o comando.</span><span class="sxs-lookup"><span data-stu-id="399cf-123">You abort the command.</span></span>
-   <span data-ttu-id="399cf-124">Você solicita uma notificação em um comando subsequente.</span><span class="sxs-lookup"><span data-stu-id="399cf-124">You request notification in a subsequent command.</span></span>
-   <span data-ttu-id="399cf-125">O MCI detecta uma falha.</span><span class="sxs-lookup"><span data-stu-id="399cf-125">MCI detects a failure.</span></span>

 

 




