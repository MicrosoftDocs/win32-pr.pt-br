---
description: A classe de dispositivo comm/DataModel/PortName consiste nos nomes dos dispositivos aos quais os modems estão anexados.
ms.assetid: 174519f6-3e73-4f05-9718-9e38680a0fb7
title: comm/datamodeling/PortName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5f926dc87a093f49d41256b003e47c048caa5ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829290"
---
# <a name="commdatamodemportname"></a><span data-ttu-id="6a8a8-103">comm/datamodeling/PortName</span><span class="sxs-lookup"><span data-stu-id="6a8a8-103">comm/datamodem/portname</span></span>

<span data-ttu-id="6a8a8-104">A classe de dispositivo comm/DataModel/PortName consiste nos nomes dos dispositivos aos quais os modems estão anexados.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-104">The comm/datamodem/portname device class consists of the device names to which modems are attached.</span></span> <span data-ttu-id="6a8a8-105">Quando esse nome de dispositivo é especificado em uma chamada para a função [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) , a função preenche a estrutura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) com uma cadeia de caracteres ANSI (não Unicode) terminada em nulo, especificando o nome da porta à qual o modem especificado está anexado, como "COM1 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="6a8a8-105">When this device name is specified in a call to the [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) function, the function fills the [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure with a null-terminated ANSI (not Unicode) string specifying the name of the port to which the specified modem is attached, such as "COM1\\0".</span></span> <span data-ttu-id="6a8a8-106">Isso é destinado principalmente para fins de identificação na interface do usuário, mas pode ser usado em algumas circunstâncias para abrir o dispositivo diretamente, ignorando o provedor de serviços (se o provedor de serviços ainda não tiver o dispositivo aberto).</span><span class="sxs-lookup"><span data-stu-id="6a8a8-106">This is intended primarily for identification purposes in the user interface, but could be used under some circumstances to open the device directly, bypassing the service provider (if the service provider does not already have the device open itself).</span></span> <span data-ttu-id="6a8a8-107">Se não houver nenhuma porta associada ao dispositivo, uma cadeia de caracteres nula (" \\ 0") será retornada na estrutura **VARSTRING** (com um comprimento de cadeia de caracteres de 1).</span><span class="sxs-lookup"><span data-stu-id="6a8a8-107">If there is no port associated with the device, a null string ("\\0") is returned in the **VARSTRING** structure (with a string length of 1).</span></span>

 

 



